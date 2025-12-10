<script lang="ts">
  import { ModeWatcher, toggleMode } from "mode-watcher";
  import { page } from "$app/state";
  import { get } from "svelte/store";
  import './layout.css'
  let { children } = $props();
  import { Button } from "$lib/components/ui/button/index.js";
  import { Sheet, SheetContent, SheetTrigger } from "$lib/components/ui/sheet/index.js";

  import Sun from "@lucide/svelte/icons/sun";
  import Moon from "@lucide/svelte/icons/moon";
  import Menu from "@lucide/svelte/icons/menu";
  import MessageCircle from "@lucide/svelte/icons/message-circle";
  import Sparkles from "@lucide/svelte/icons/sparkles";

  let open = false;

  const navLinks = [
    { name: "Home", path: "/" },
    { name: "Internships", path: "/internships" },
    { name: "Courses", path: "/courses" },
    { name: "Workshops", path: "/workshops" }
  ];

  const isActive = (path: string) => {
    const current = page.url.pathname;
    return current === path || (current.startsWith(path) && path !== "/");
  };
</script>

<ModeWatcher />

<div class="min-h-screen bg-background text-foreground relative">
	<!-- Navbar -->
	<header
		class="fixed top-0 left-0 right-0 z-50 border-b border-border/50 bg-background/80 backdrop-blur-xl shadow-lg"
	>
		<div class="container mx-auto px-4 flex h-16 items-center justify-between">
			<!-- Logo -->
			<a href="/" class="flex items-center gap-3 font-bold text-2xl">
				<div
					class="w-11 h-11 rounded-xl bg-gradient-to-br from-primary to-orange-600 flex items-center justify-center text-white font-black text-2xl"
				>
					M
				</div>
				<span>MazeMaxx</span>
			</a>

			<!-- Desktop Nav -->
			<nav class="hidden md:flex items-center gap-8">
				{#each navLinks as link}
					<a
						href={link.path}
						class="relative py-2 text-sm font-medium transition-colors {isActive(link.path)
							? 'text-primary font-bold'
							: 'text-muted-foreground hover:text-foreground'}"
					>
						{link.name}
						{#if isActive(link.path)}
							<span
								class="absolute inset-x-0 bottom-0 h-0.5 bg-gradient-to-r from-primary to-orange-600"
							></span>
						{/if}
					</a>
				{/each}
			</nav>

			<!-- Right Actions -->
			<div class="flex items-center gap-3">
				<Button
					variant="outline"
					size="icon"
					onclick={toggleMode}
					class="rounded-full border-2 border-border hover:border-primary transition"
				>
					<Sun class="h-5 w-5 rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0" />
					<Moon
						class="absolute h-5 w-5 rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"
					/>
					<span class="sr-only">Toggle theme</span>
				</Button>

				<Button
					class="hidden sm:flex items-center gap-2 bg-primary hover:bg-primary/90 text-white font-semibold shadow-lg"
				>
					<Sparkles class="h-4 w-4" />
					Enroll Now
				</Button>

				<!-- Mobile Menu -->
				<Sheet bind:open>
					<SheetTrigger>
						<Button variant="outline" size="icon" class="md:hidden">
							<Menu class="h-6 w-6" />
						</Button>
					</SheetTrigger>
					<SheetContent side="right" class="w-80 bg-background/95 backdrop-blur-xl">
						<div class="flex flex-col gap-6 mt-10">
							{#each navLinks as link}
								<a
									href={link.path}
									class="text-xl py-3 border-b border-border/30 {isActive(link.path)
										? 'text-primary font-bold'
										: 'text-muted-foreground'}"
									onclick={() => (open = false)}
								>
									{link.name}
								</a>
							{/each}
							<Button class="mt-6 w-full" href="https://wa.me/919876543210">
								Enroll via WhatsApp
							</Button>
						</div>
					</SheetContent>
				</Sheet>
			</div>
		</div>
	</header>

	<!-- Main Content -->
	<main>
	     {@render children()}
		<!-- Use default slot instead of {@render children()} -->
	</main>

	<!-- Floating WhatsApp Button -->
	<a
		href="https://wa.me/919876543210?text=Hi%20MazeMaxx%2C%20I%20want%20to%20know%20more!"
		target="_blank"
		class="fixed bottom-6 right-6 z-50 group"
	>
		<div class="relative">
			<div class="absolute -inset-2 bg-green-500/20 rounded-full blur-xl animate-pulse"></div>
			<Button
				size="lg"
				class="relative rounded-full bg-green-600 hover:bg-green-700 text-white shadow-2xl hover:shadow-green-500/50 hover:scale-110 transition-all duration-300 pl-5 pr-6"
			>
				<MessageCircle class="h-7 w-7" />
				<span class="ml-3 font-bold">Chat on WhatsApp</span>
			</Button>
		</div>
	</a>

	<!-- Footer -->
	<footer class="border-t border-border/50 bg-muted/30 py-12">
		<div class="container text-center">
			<p class="text-sm text-muted-foreground">
				© 2025 <span class="font-bold text-foreground">MazeMaxx</span>. Building strong IT
				foundations for students.
			</p>
			<p class="mt-3 text-primary font-semibold text-lg">
				“We don’t overload. We build confidence.”
			</p>
		</div>
	</footer>
</div>
