<script lang="ts">
  import { Button } from "$lib/components/ui/button/index.js";
  import { Card, CardContent, CardDescription, CardHeader, CardTitle } from "$lib/components/ui/card/index.js";
  import { Badge } from "$lib/components/ui/badge/index.js";
  import ArrowRight from "@lucide/svelte/icons/arrow-right";
  import Clock from "@lucide/svelte/icons/clock";
  import Users from "@lucide/svelte/icons/users";
  import Award from "@lucide/svelte/icons/award";
  import Zap from "@lucide/svelte/icons/zap";
  import CheckCircle2 from "@lucide/svelte/icons/check-circle-2";
  import Code from "@lucide/svelte/icons/code";
  import BrainCircuit from "@lucide/svelte/icons/brain-circuit";
  import Presentation from "@lucide/svelte/icons/presentation";
  import Heart from "@lucide/svelte/icons/heart";
  import Sparkles from "@lucide/svelte/icons/sparkles";
</script>

<svelte:head>
	<title>MazeMaxx – Short, Practical & Placement-Focused IT Training for Students</title>
	<meta name="description" content="10-day Java/Python internships, Full Stack, Problem Solving & Workshops – beginner-friendly, real confidence, no false promises." />
</svelte:head>

<!-- Hero -->
<section class="relative overflow-hidden py-24 md:py-36">
  <!-- Background Flourish -->
  <div class="absolute inset-0 -z-10">
    <div class="absolute top-10 left-1/3 w-96 h-96 bg-primary/10 rounded-full blur-3xl animate-pulse"></div>
    <div class="absolute bottom-20 right-1/4 w-80 h-80 bg-primary/5 rounded-full blur-3xl animate-pulse delay-700"></div>
  </div>

  <div class="container text-center relative z-10">
    <Badge variant="secondary" class="mb-6 text-lg px-6 py-2 animate-in fade-in slide-in-from-top duration-700">
      <Sparkles class="w-4 h-4 mr-2" /> Short-term • Beginner-Friendly • Career-Oriented
    </Badge>

    <h1 class="text-5xl md:text-7xl font-bold tracking-tight mb-8 animate-in fade-in slide-in-from-bottom duration-1000">
      Strong Foundations.<br />
      Real Confidence.<br />
      <span class="bg-gradient-to-r from-primary to-orange-600 bg-clip-text text-transparent">
        No False Promises.
      </span>
    </h1>

    <p class="text-xl md:text-2xl text-muted-foreground max-w-2xl mx-auto mb-10 animate-in fade-in slide-in-from-bottom delay-300 duration-1000">
      10-day internships • Full Stack projects • 30 placement problems • 1-day career workshops
    </p>

    <div class="flex flex-col sm:flex-row gap-5 justify-center animate-in fade-in slide-in-from-bottom delay-500 duration-1000">
      <Button size="lg" class="text-lg px-8 font-semibold group/btn relative overflow-hidden bg-primary hover:bg-primary/90 text-white">
        <span class="relative z-10 flex items-center">
          View All Programs <ArrowRight class="ml-2 h-5 w-5 group-hover/btn:translate-x-1 transition" />
        </span>
        <div class="absolute inset-0 bg-white/20 translate-y-full group-hover/btn:translate-y-0 transition-transform duration-500"></div>
      </Button>
      <Button size="lg" variant="outline" class="text-lg">WhatsApp Us</Button>
    </div>
  </div>
</section>

<!-- Programs Grid -->
<section class="py-24">
  <div class="container">
    <h2 class="text-4xl md:text-5xl font-bold text-center mb-16 animate-in fade-in duration-1000">
      Our <span class="text-primary">Programs</span>
    </h2>

    <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8 max-w-7xl mx-auto">
      <!-- Internship Card -->
      <Card class="group relative overflow-hidden bg-card/80 backdrop-blur-sm hover:shadow-2xl hover:shadow-primary/20 hover:-translate-y-3 transition-all duration-500">
        <div class="absolute inset-0 bg-gradient-to-t from-primary/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
        <CardHeader>
          <div class="w-14 h-14 rounded-2xl bg-primary/10 flex items-center justify-center mb-4 group-hover:scale-110 group-hover:bg-primary/20 transition-all duration-500">
            <Zap class="h-8 w-8 text-primary" />
          </div>
          <CardTitle class="text-2xl">10-Day Internship</CardTitle>
          <CardDescription class="text-base">Java or Python (Fundamentals + OOPS + Collections)</CardDescription>
        </CardHeader>
        <CardContent>
          <p class="text-3xl font-bold text-primary">₹1,199</p>
          <p class="text-sm text-muted-foreground mt-1">1–1.25 hrs/day • Certificate</p>
          <Button class="w-full mt-5 group/btn relative overflow-hidden">
            <span class="relative z-10">View Details</span>
            <div class="absolute inset-0 bg-white/20 translate-y-full group-hover/btn:translate-y-0 transition-transform duration-500"></div>
          </Button>
        </CardContent>
      </Card>

      <!-- Full Stack -->
      <Card class="group relative overflow-hidden bg-card/80 backdrop-blur-sm hover:shadow-2xl hover:shadow-primary/20 hover:-translate-y-3 transition-all duration-500">
        <div class="absolute inset-0 bg-gradient-to-t from-primary/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
        <CardHeader>
          <div class="w-14 h-14 rounded-2xl bg-primary/10 flex items-center justify-center mb-4 group-hover:scale-110 group-hover:bg-primary/20 transition-all duration-500">
            <Code class="h-8 w-8 text-primary" />
          </div>
          <CardTitle class="text-2xl">Full Stack Web Dev</CardTitle>
          <CardDescription class="text-base">HTML • CSS • JS • Node • Express • SQL + Project</CardDescription>
        </CardHeader>
        <CardContent>
          <p class="text-3xl font-bold text-primary">₹1,499</p>
          <Button class="w-full mt-5 group/btn relative overflow-hidden">
            <span class="relative z-10">View Details</span>
            <div class="absolute inset-0 bg-white/20 translate-y-full group-hover/btn:translate-y-0 transition-transform duration-500"></div>
          </Button>
        </CardContent>
      </Card>

      <!-- Problem Solving -->
      <Card class="group relative overflow-hidden bg-card/80 backdrop-blur-sm hover:shadow-2xl hover:shadow-primary/20 hover:-translate-y-3 transition-all duration-500">
        <div class="absolute inset-0 bg-gradient-to-t from-primary/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
        <CardHeader>
          <div class="w-14 h-14 rounded-2xl bg-primary/10 flex items-center justify-center mb-4 group-hover:scale-110 group-hover:bg-primary/20 transition-all duration-500">
            <BrainCircuit class="h-8 w-8 text-primary" />
          </div>
          <CardTitle class="text-2xl">30 Placement Problems</CardTitle>
          <CardDescription class="text-base">Easy → Medium → 5 Hard (TCS, Infosys style)</CardDescription>
        </CardHeader>
        <CardContent>
          <p class="text-3xl font-bold text-primary">₹999</p>
          <Button class="w-full mt-5 group/btn relative overflow-hidden">
            <span class="relative z-10">View Details</span>
            <div class="absolute inset-0 bg-white/20 translate-y-full group-hover/btn:translate-y-0 transition-transform duration-500"></div>
          </Button>
        </CardContent>
      </Card>

      <!-- Workshop -->
      <Card class="group relative overflow-hidden bg-card/80 backdrop-blur-sm hover:shadow-2xl hover:shadow-primary/20 hover:-translate-y-3 transition-all duration-500">
        <div class="absolute inset-0 bg-gradient-to-t from-primary/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
        <CardHeader>
          <div class="w-14 h-14 rounded-2xl bg-primary/10 flex items-center justify-center mb-4 group-hover:scale-110 group-hover:bg-primary/20 transition-all duration-500">
            <Presentation class="h-8 w-8 text-primary" />
          </div>
          <CardTitle class="text-2xl">1-Day Workshop</CardTitle>
          <CardDescription class="text-base">Career Plan • Placement Strategy • Web Dev Awareness</CardDescription>
        </CardHeader>
        <CardContent>
          <p class="text-3xl font-bold text-primary">₹199</p>
          <Button class="w-full mt-5 group/btn relative overflow-hidden">
            <span class="relative z-10">View Details</span>
            <div class="absolute inset-0 bg-white/20 translate-y-full group-hover/btn:translate-y-0 transition-transform duration-500"></div>
          </Button>
        </CardContent>
      </Card>
    </div>
  </div>
</section>

<!-- USP Section -->
<section class="py-24 bg-muted/50">
  <div class="container">
    <h2 class="text-4xl md:text-5xl font-bold text-center mb-16 animate-in fade-in duration-1000">
      Why Students <span class="text-primary">Love</span> MazeMaxx
    </h2>

    <div class="grid md:grid-cols-3 gap-10 max-w-5xl mx-auto">
      {#each [
        { icon: CheckCircle2, title: "No False Mastery Promises", desc: "We focus on strong basics & correct direction" },
        { icon: Users, title: "Beginner to Placement Ready", desc: "Perfect for college students" },
        { icon: Clock, title: "Only 1–1.25 hrs/day", desc: "No burnout, fits college schedule" },
        { icon: Award, title: "Professional Certificate", desc: "Boost your resume & LinkedIn" },
        { icon: Zap, title: "Live Coding + Practice", desc: "Daily doubt clearing included" },
        { icon: Heart, title: "Affordable Pricing", desc: "Designed for Indian students" }
      ] as item, i}
        <div class="text-center group animate-in fade-in slide-in-from-bottom duration-1000" style="animation-delay: {i * 100}ms;">
          <div class="relative inline-block">
            <item.icon class="h-14 w-14 mx-auto mb-5 text-primary group-hover:scale-110 transition-all duration-500" />
            <div class="absolute -inset-4 bg-primary/10 rounded-full blur-xl scale-0 group-hover:scale-100 transition-transform duration-700"></div>
          </div>
          <h3 class="font-bold text-xl mb-3">{item.title}</h3>
          <p class="text-muted-foreground text-base">{item.desc}</p>
        </div>
      {/each}
    </div>
  </div>
</section>

<!-- Final CTA -->
<section class="py-28 text-center relative overflow-hidden">
  <div class="absolute inset-0 -z-10">
    <div class="absolute inset-x-0 top-0 h-96 bg-primary/5 blur-3xl"></div>
  </div>

  <div class="container">
    <h2 class="text-4xl md:text-6xl font-bold mb-8 animate-in fade-in duration-1000">
      Ready to Build Your IT Career the Right Way?
    </h2>
    <p class="text-xl md:text-2xl text-muted-foreground mb-10 max-w-3xl mx-auto animate-in fade-in delay-300 duration-1000">
      “MazeMaxx doesn’t overload students.<br />We build strong foundations, clear direction, and real confidence.”
    </p>
    <Button 
      size="lg" 
      class="text-xl px-12 py-8 font-bold bg-gradient-to-r from-primary to-orange-600 shadow-2xl shadow-primary/40
             hover:shadow-primary/50 hover:scale-105 transition-all duration-300"
    >
      <Sparkles class="mr-3 h-6 w-6" />
      Enroll Today – Limited Seats!
    </Button>
    <p class="mt-6 text-muted-foreground animate-in fade-in delay-500 duration-1000">
      Next batches start in just 5 days!
    </p>
  </div>
</section>