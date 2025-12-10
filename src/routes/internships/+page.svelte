<script lang="ts">
  import { Button } from "$lib/components/ui/button/index.js";
  import { Card, CardContent, CardDescription, CardHeader, CardTitle } from "$lib/components/ui/card/index.js";
  import { Badge } from "$lib/components/ui/badge/index.js";
  import ArrowRight from "@lucide/svelte/icons/arrow-right";
  import Calendar from "@lucide/svelte/icons/calendar";
  import Clock from "@lucide/svelte/icons/clock";
  import Award from "@lucide/svelte/icons/award";
  import Zap from "@lucide/svelte/icons/zap";
  import CheckCircle from "@lucide/svelte/icons/check-circle";
  import Code from "@lucide/svelte/icons/code";
  import Laptop from "@lucide/svelte/icons/laptop";
  import Sparkles from "@lucide/svelte/icons/sparkles";
</script>

<svelte:head>
  <title>10-Day Internships – Java & Python | MazeMaxx</title>
  <meta name="description" content="10-day online internship in Java or Python. Only 1–1.25 hrs/day. Beginner-friendly. Certificate + strong foundation." />
</svelte:head>

<!-- Hero Section -->
<section class="relative overflow-hidden py-28 md:py-36">
  <!-- Background Flourish Blobs -->
  <div class="absolute inset-0 -z-10">
    <div class="absolute top-10 left-1/4 w-96 h-96 bg-primary/10 rounded-full blur-3xl animate-pulse"></div>
    <div class="absolute bottom-20 right-1/3 w-80 h-80 bg-primary/8 rounded-full blur-3xl animate-pulse delay-1000"></div>
  </div>

  <div class="container text-center relative z-10">
    <Badge variant="secondary" class="mb-6 text-lg px-6 py-2 animate-in fade-in slide-in-from-top duration-700">
      <Sparkles class="w-5 h-5 mr-2" /> 10 Days • 1–1.25 hrs/day • Online/Offline
    </Badge>

    <h1 class="text-5xl md:text-7xl font-bold tracking-tight mb-8 animate-in fade-in slide-in-from-bottom duration-1000">
      10-Day<br />
      <span class="bg-gradient-to-r from-primary to-orange-600 bg-clip-text text-transparent">
        Programming Internship
      </span>
    </h1>

    <p class="text-xl md:text-2xl text-muted-foreground max-w-3xl mx-auto mb-10 animate-in fade-in slide-in-from-bottom delay-300 duration-1000">
      Fundamentals + OOPS + Collections • Live coding every day • Professional certificate • Real confidence
    </p>

    <Button 
      size="lg" 
      href="#programs"
      class="text-lg px-10 py-7 font-bold group/btn relative overflow-hidden bg-primary hover:bg-primary/90"
    >
      <span class="relative z-10 flex items-center">
        Choose Your Track <ArrowRight class="ml-3 h-6 w-6 group-hover/btn:translate-x-2 transition" />
      </span>
      <div class="absolute inset-0 bg-white/20 translate-y-full group-hover/btn:translate-y-0 transition-transform duration-500"></div>
    </Button>
  </div>
</section>

<!-- Internship Cards -->
<section id="programs" class="py-28">
  <div class="container">
    <h2 class="text-4xl md:text-5xl font-bold text-center mb-16 animate-in fade-in duration-1000">
      Choose Your <span class="text-primary">Track</span>
    </h2>

    <div class="grid md:grid-cols-2 gap-10 max-w-6xl mx-auto">

      <!-- Java Card -->
      <Card class="group relative overflow-hidden bg-card/90 backdrop-blur-sm border border-border/50 hover:shadow-2xl hover:shadow-primary/25 hover:-translate-y-4 transition-all duration-700">
        <div class="absolute inset-0 bg-gradient-to-t from-primary/10 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-700"></div>

        <CardHeader class="text-center pb-10">
          <div class="relative inline-block">
            <div class="w-24 h-24 mx-auto mb-6 rounded-3xl bg-primary/10 ring-4 ring-primary/20 flex items-center justify-center group-hover:scale-110 group-hover:ring-primary/40 group-hover:bg-primary/20 transition-all duration-500">
              <Code class="h-14 w-14 text-primary" />
            </div>
            <div class="absolute -inset-6 bg-primary/10 rounded-full blur-xl scale-0 group-hover:scale-100 transition-transform duration-700"></div>
          </div>

          <CardTitle class="text-4xl md:text-5xl font-bold bg-gradient-to-r from-primary to-orange-600 bg-clip-text text-transparent">
            Java Internship
          </CardTitle>
          <CardDescription class="text-lg mt-3 font-medium">
            #1 language in campus placements • TCS • Infosys • Accenture
          </CardDescription>
        </CardHeader>

        <CardContent class="space-y-8">
          <div class="text-center">
            <p class="text-5xl font-bold text-primary">₹1,199</p>
            <p class="text-lg text-muted-foreground mt-2 flex items-center justify-center gap-2">
              <Award class="h-5 w-5" /> Certificate + LinkedIn Ready
            </p>
          </div>

          <ul class="space-y-4">
            {#each [
              "Variables, Loops, Conditionals",
              "Classes, Objects, Constructors",
              "Inheritance & Polymorphism",
              "Encapsulation + Abstraction",
              "ArrayList • HashMap • HashSet"
            ] as topic}
              <li class="flex items-center gap-4 text-base">
                <CheckCircle class="h-6 w-6 text-primary flex-shrink-0" />
                <span class="font-medium">{topic}</span>
              </li>
            {/each}
          </ul>

          <Button 
            class="w-full text-lg py-7 font-bold group/btn relative overflow-hidden shadow-lg shadow-primary/30"
            href="https://wa.me/919876543210?text=Hi%20MazeMaxx%2C%20I%20want%20to%20join%20the%20Java%20Internship"
          >
            <span class="relative z-10 flex items-center justify-center">
              Enroll Now – Java <Zap class="ml-3 h-6 w-6 group-hover/btn:scale-125 transition" />
            </span>
            <div class="absolute inset-0 bg-white/25 translate-y-full group-hover/btn:translate-y-0 transition-transform duration-500"></div>
          </Button>
        </CardContent>
      </Card>

      <!-- Python Card -->
      <Card class="group relative overflow-hidden bg-card/90 backdrop-blur-sm border border-border/50 hover:shadow-2xl hover:shadow-primary/25 hover:-translate-y-4 transition-all duration-700">
        <div class="absolute inset-0 bg-gradient-to-t from-primary/10 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-700"></div>

        <CardHeader class="text-center pb-10">
          <div class="relative inline-block">
            <div class="w-24 h-24 mx-auto mb-6 rounded-3xl bg-primary/10 ring-4 ring-primary/20 flex items-center justify-center group-hover:scale-110 group-hover:ring-primary/40 group-hover:bg-primary/20 transition-all duration-500">
              <Laptop class="h-14 w-14 text-primary" />
            </div>
            <div class="absolute -inset-6 bg-primary/10 rounded-full blur-xl scale-0 group-hover:scale-100 transition-transform duration-700"></div>
          </div>

          <CardTitle class="text-4xl md:text-5xl font-bold bg-gradient-to-r from-primary to-orange-600 bg-clip-text text-transparent">
            Python Internship
          </CardTitle>
          <CardDescription class="text-lg mt-3 font-medium">
            Perfect for Web • Automation • Data Science • AI • ML
          </CardDescription>
        </CardHeader>

        <CardContent class="space-y-8">
          <div class="text-center">
            <p class="text-5xl font-bold text-primary">₹1,199</p>
            <p class="text-lg text-muted-foreground mt-2 flex items-center justify-center gap-2">
              <Award class="h-5 w-5" /> Certificate + LinkedIn Ready
            </p>
          </div>

          <ul class="space-y-4">
            {#each [
              "Variables, Loops, Lists, Tuples",
              "Functions & Modules",
              "OOPS – Classes & Objects",
              "Inheritance & Polymorphism",
              "Dictionary • Set operations"
            ] as topic}
              <li class="flex items-center gap-4 text-base">
                <CheckCircle class="h-6 w-6 text-primary flex-shrink-0" />
                <span class="font-medium">{topic}</span>
              </li>
            {/each}
          </ul>

          <Button 
            class="w-full text-lg py-7 font-bold group/btn relative overflow-hidden shadow-lg shadow-primary/30"
            href="https://wa.me/919876543210?text=Hi%20MazeMaxx%2C%20I%20want%20to%20join%20the%20Python%20Internship"
          >
            <span class="relative z-10 flex items-center justify-center">
              Enroll Now – Python <Zap class="ml-3 h-6 w-6 group-hover/btn:scale-125 transition" />
            </span>
            <div class="absolute inset-0 bg-white/25 translate-y-full group-hover/btn:translate-y-0 transition-transform duration-500"></div>
          </Button>
        </CardContent>
      </Card>

    </div>

    <!-- Bottom Section -->
    <div class="text-center mt-20">
      <p class="text-xl text-muted-foreground mb-8 max-w-3xl mx-auto">
        <Clock class="inline-block h-6 w-6 mr-2" />
        Daily class: 20 min theory • 25 min live coding • 25 min practice & doubts
      </p>

      <Badge variant="outline" class="text-xl px-8 py-4 font-medium shadow-lg">
        <Calendar class="mr-3 h-6 w-6 text-primary" />
        <span class="font-bold">Next Batch Starts:</span> 15th Dec 2025
      </Badge>
    </div>
  </div>
</section>