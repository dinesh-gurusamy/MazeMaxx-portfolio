<script lang="ts">
  import { Button } from "$lib/components/ui/button/index.js";
  import { Card, CardContent, CardDescription, CardHeader, CardTitle } from "$lib/components/ui/card/index.js";
  import { Badge } from "$lib/components/ui/badge/index.js";

  import Code2 from "@lucide/svelte/icons/code-2";
  import Brain from "@lucide/svelte/icons/brain";
  import Trophy from "@lucide/svelte/icons/trophy";
  import Timer from "@lucide/svelte/icons/timer";
  import Sparkles from "@lucide/svelte/icons/sparkles";
  import ArrowRight from "@lucide/svelte/icons/arrow-right";
  import CheckCircle from "@lucide/svelte/icons/check-circle";
  import Rocket from "@lucide/svelte/icons/rocket";
</script>

<svelte:head>
  <title>Placement Courses – Full Stack & Problem Solving | MazeMaxx</title>
  <meta name="description" content="10-Day Full Stack Web Dev with Live Project + 30 Placement Problems (TCS, Infosys style) – Interview ready in just 10 days!" />
</svelte:head>

<!-- Hero -->
<section class="relative overflow-hidden py-28 md:py-36">
  <div class="absolute inset-0 -z-10">
    <div class="absolute top-10 right-1/4 w-96 h-96 bg-primary/10 rounded-full blur-3xl animate-pulse"></div>
    <div class="absolute bottom-0 left-1/3 w-80 h-80 bg-primary/5 rounded-full blur-3xl animate-pulse delay-700"></div>
  </div>

  <div class="container text-center">
    <Badge variant="secondary" class="mb-6 text-lg px-8 py-3 animate-in fade-in slide-in-from-top duration-700">
      <Sparkles class="w-5 h-5 mr-2" /> Placement-Focused • Real Projects • Zero Fluff
    </Badge>

    <h1 class="text-5xl md:text-7xl font-bold tracking-tight mb-8 animate-in fade-in slide-in-from-bottom duration-1000">
      Placement-Focused<br />
      <span class="bg-gradient-to-r from-primary to-orange-600 bg-clip-text text-transparent">
        Courses
      </span>
    </h1>

    <p class="text-xl md:text-2xl text-muted-foreground max-w-3xl mx-auto mb-10 animate-in fade-in slide-in-from-bottom delay-300 duration-1000">
      Become interview-ready in just 10 days — with live projects & real company-style coding problems
    </p>
  </div>
</section>

<!-- Courses Grid -->
<section class="py-28">
  <div class="container">
    <div class="grid md:grid-cols-2 gap-12 max-w-6xl mx-auto">

      <!-- Full Stack Course -->
      <Card class="group relative overflow-hidden bg-card/90 backdrop-blur-sm border border-border/50 hover:shadow-2xl hover:shadow-primary/30 hover:-translate-y-5 transition-all duration-700">
        <div class="absolute inset-0 bg-gradient-to-br from-primary/10 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-700"></div>

        <CardHeader class="text-center pb-10">
          <div class="relative inline-block">
            <div class="w-28 h-28 mx-auto mb-6 rounded-3xl bg-primary/10 ring-8 ring-primary/20 flex items-center justify-center group-hover:scale-110 group-hover:ring-primary/40 group-hover:bg-primary/20 transition-all duration-500">
              <Code2 class="h-16 w-16 text-primary" />
            </div>
            <div class="absolute -inset-8 bg-primary/10 rounded-full blur-2xl scale-0 group-hover:scale-100 transition-transform duration-700"></div>
          </div>

          <CardTitle class="text-4xl md:text-5xl font-bold bg-gradient-to-r from-primary to-orange-600 bg-clip-text text-transparent">
            Full Stack Web Dev
          </CardTitle>

          <Badge class="mt-4 text-lg px-6 py-2 shadow-lg">Live Mini Project Included</Badge>
        </CardHeader>

        <CardContent class="space-y-8">
          <div class="text-center">
            <p class="text-5xl font-bold text-primary">₹1,499</p>
            <p class="text-lg text-muted-foreground mt-2">10 Days • Deploy-Ready Project</p>
          </div>

          <p class="text-lg font-medium text-center">
            HTML • CSS • JavaScript • Node.js • Express • SQL
          </p>

          <ul class="space-y-5">
            {#each [
              "Build responsive websites from scratch",
              "Create Login / Register systems",
              "Connect Frontend to Backend to Database",
              "Get deploy-ready code + GitHub repo"
            ] as item}
              <li class="flex items-center gap-4 text-base font-medium">
                <CheckCircle class="h-7 w-7 text-primary flex-shrink-0" />
                {item}
              </li>
            {/each}
          </ul>

          <Button 
            class="w-full text-lg py-8 font-bold group/btn relative overflow-hidden shadow-xl shadow-primary/40"
            href="https://wa.me/919876543210?text=Hi%20MazeMaxx%2C%20I%20want%20to%20join%20Full%20Stack%20Course"
          >
            <span class="relative z-10 flex items-center justify-center">
              Join Full Stack Batch <Rocket class="ml-3 h-7 w-7 group-hover/btn:translate-x-3 transition" />
            </span>
            <div class="absolute inset-0 bg-white/30 translate-y-full group-hover/btn:translate-y-0 transition-transform duration-500"></div>
          </Button>
        </CardContent>
      </Card>

      <!-- 30 Problems Course -->
      <Card class="group relative overflow-hidden bg-card/90 backdrop-blur-sm border border-border/50 hover:shadow-2xl hover:shadow-primary/30 hover:-translate-y-5 transition-all duration-700">
        <div class="absolute inset-0 bg-gradient-to-br from-primary/10 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-700"></div>

        <CardHeader class="text-center pb-10">
          <div class="relative inline-block">
            <div class="w-28 h-28 mx-auto mb-6 rounded-3xl bg-primary/10 ring-8 ring-primary/20 flex items-center justify-center group-hover:scale-110 group-hover:ring-primary/40 group-hover:bg-primary/20 transition-all duration-500">
              <Brain class="h-16 w-16 text-primary" />
            </div>
            <div class="absolute -inset-8 bg-primary/10 rounded-full blur-2xl scale-0 group-hover:scale-100 transition-transform duration-700"></div>
          </div>

          <CardTitle class="text-4xl md:text-5xl font-bold bg-gradient-to-r from-primary to-orange-600 bg-clip-text text-transparent">
            30 Placement Problems
          </CardTitle>

          <Badge class="mt-4 text-lg px-6 py-2 shadow-lg">TCS • Infosys • Accenture Style</Badge>
        </CardHeader>

        <CardContent class="space-y-8">
          <div class="text-center">
            <p class="text-5xl font-bold text-primary">₹999</p>
            <p class="text-lg text-muted-foreground mt-2">10 Days • 3 Problems Daily</p>
          </div>

          <p class="text-center text-lg font-medium">
            6 Basic to 19 Medium to 5 Hard Problems
          </p>

          <div class="flex justify-center gap-8 text-base font-medium">
            <div class="flex items-center gap-3">
              <Timer class="h-6 w-6 text-primary" />
              1 hr/day
            </div>
            <div class="flex items-center gap-3">
              <Trophy class="h-6 w-6 text-primary" />
              Interview Ready
            </div>
          </div>

          <Button 
            class="w-full text-lg py-8 font-bold group/btn relative overflow-hidden shadow-xl shadow-primary/40"
            href="https://wa.me/919876543210?text=Hi%20MazeMaxx%2C%20I%20want%20to%20join%2030%20Placement%20Problems%20Course"
          >
            <span class="relative z-10 flex items-center justify-center">
              Start Problem Solving <ArrowRight class="ml-3 h-7 w-7 group-hover/btn:translate-x-3 transition" />
            </span>
            <div class="absolute inset-0 bg-white/30 translate-y-full group-hover/btn:translate-y-0 transition-transform duration-500"></div>
          </Button>
        </CardContent>
      </Card>

    </div>
  </div>
</section>