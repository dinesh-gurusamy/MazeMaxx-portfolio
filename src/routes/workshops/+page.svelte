<script lang="ts">
  import { Button } from "$lib/components/ui/button/index.js";
  import { Card, CardContent, CardDescription, CardHeader, CardTitle } from "$lib/components/ui/card/index.js";
  import { Badge } from "$lib/components/ui/badge/index.js";

  // Individual icon imports (lucide-svelte v0.300+ style)
  import Users from "@lucide/svelte/icons/users";
  import MapPin from "@lucide/svelte/icons/map-pin";
  import Mic2 from "@lucide/svelte/icons/mic-2";
  import Calendar from "@lucide/svelte/icons/calendar";
  import Sparkles from "@lucide/svelte/icons/sparkles";
  import ArrowRight from "@lucide/svelte/icons/arrow-right";
</script>

<svelte:head>
  <title>1-Day Career Workshops • MazeMaxx</title>
  <meta name="description" content="Most engaging 1-day workshops for colleges – Career Plan, Web Dev Career, Placement Strategy • Only ₹199" />
</svelte:head>

<section class="relative overflow-hidden py-24 md:py-32">
  <!-- Background Gradient Blob (Flourish #1) -->
  <div class="absolute inset-0 -z-10">
    <div class="absolute top-20 left-1/4 w-96 h-96 bg-primary/10 rounded-full blur-3xl animate-pulse"></div>
    <div class="absolute bottom-10 right-1/4 w-80 h-80 bg-primary/5 rounded-full blur-3xl animate-pulse delay-1000"></div>
  </div>

  <div class="container relative z-10">
    <!-- Hero -->
    <div class="text-center mb-20">
      <Badge variant="secondary" class="mb-6 text-lg px-6 py-2 animate-in fade-in slide-in-from-top duration-700">
        <Sparkles class="w-4 h-4 mr-2" /> 1–1.5 Hours Only • Just ₹199
      </Badge>

      <h1 class="text-5xl md:text-7xl font-bold tracking-tight mb-6 animate-in fade-in slide-in-from-bottom duration-1000">
        1-Day Career<br />
        <span class="bg-gradient-to-r from-primary to-orange-600 bg-clip-text text-transparent">
          Workshops
        </span>
      </h1>

      <p class="text-xl md:text-2xl text-muted-foreground max-w-2xl mx-auto animate-in fade-in slide-in-from-bottom delay-300 duration-1000">
        Perfect ice-breaker seminars for your college tech fest, CSE department, or training & placement cell
      </p>
    </div>

    <!-- Workshop Cards with Flourish Effects -->
    <div class="grid md:grid-cols-3 gap-10 max-w-6xl mx-auto">
      <!-- Card 1 -->
      <Card 
        class="group relative overflow-hidden border border-border/50 bg-card/80 backdrop-blur-sm 
               hover:shadow-2xl hover:shadow-primary/20 hover:-translate-y-3 
               transition-all duration-500 hover:border-primary/40"
      >
        <div class="absolute inset-0 bg-gradient-to-t from-primary/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>

        <CardHeader class="text-center pb-8">
          <div class="relative inline-block">
            <div class="w-20 h-20 mx-auto mb-6 rounded-3xl bg-primary/10 flex items-center justify-center
                        group-hover:scale-110 group-hover:bg-primary/20 transition-all duration-500">
              <Mic2 class="h-10 w-10 text-primary" />
            </div>
            <div class="absolute -inset-4 bg-primary/5 rounded-full blur-xl scale-0 group-hover:scale-100 transition-transform duration-700"></div>
          </div>

          <CardTitle class="text-2xl md:text-3xl">Web Dev Career</CardTitle>
          <CardDescription class="mt-3 text-base">
            Frontend vs Backend • Real Salaries • Demand • 2026 Roadmap
          </CardDescription>
        </CardHeader>

        <CardContent class="pt-6">
          <Button class="w-full group/btn relative overflow-hidden bg-primary hover:bg-primary/90">
            <span class="relative z-10 flex items-center justify-center">
              Book Workshop • ₹199 <ArrowRight class="ml-2 h-4 w-4 group-hover/btn:translate-x-1 transition" />
            </span>
            <div class="absolute inset-0 bg-white/20 translate-y-full group-hover/btn:translate-y-0 transition-transform duration-500"></div>
          </Button>
        </CardContent>
      </Card>

      <!-- Card 2 – Most Popular (Extra Flourish) -->
      <Card 
        class="group relative overflow-hidden border-2 border-primary/30 bg-gradient-to-br from-primary/5 via-transparent to-transparent
               shadow-xl shadow-primary/10 hover:shadow-2xl hover:shadow-primary/25 
               hover:-translate-y-4 transition-all duration-500"
      >
        <div class="absolute top-0 right-0 px-4 py-1 bg-primary text-white text-xs font-bold rounded-bl-2xl">
          MOST POPULAR
        </div>

        <CardHeader class="text-center pb-8">
          <div class="relative inline-block">
            <div class="w-24 h-24 mx-auto mb-6 rounded-3xl bg-primary/15 ring-4 ring-primary/20 flex items-center justify-center
                        group-hover:scale-110 group-hover:ring-primary/40 transition-all duration-500">
            <MapPin class="h-12 w-12 text-primary" />
          </div>

          <CardTitle class="text-3xl md:text-4xl bg-gradient-to-r from-primary to-orange-600 bg-clip-text text-transparent">
            Career Plan
          </CardTitle>
          <CardDescription class="mt-3 text-lg font-medium">
            Choose the right IT domain • Skills • Full 4-year roadmap
          </CardDescription>
        </CardHeader>

        <CardContent class="pt-6">
          <Button size="lg" class="w-full font-bold text-lg shadow-lg shadow-primary/30">
            Book Now • ₹199
          </Button>
        </CardContent>
      </Card>

      <!-- Card 3 -->
      <Card 
        class="group relative overflow-hidden border border-border/50 bg-card/80 backdrop-blur-sm 
               hover:shadow-2xl hover:shadow-primary/20 hover:-translate-y-3 
               transition-all duration-500 hover:border-primary/40"
      >
        <div class="absolute inset-0 bg-gradient-to-t from-primary/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>

        <CardHeader class="text-center pb-8">
          <div class="relative inline-block">
            <div class="w-20 h-20 mx-auto mb-6 rounded-3xl bg-primary/10 flex items-center justify-center
                        group-hover:scale-110 group-hover:bg-primary/20 transition-all duration-500">
              <Users class="h-10 w-10 text-primary" />
            </div>
          </div>

          <CardTitle class="text-2xl md:text-3xl">Placement Strategy</CardTitle>
          <CardDescription class="mt-3 text-base">
            Resume • Internship • Technical + HR rounds • Final roadmap
          </CardDescription>
        </CardHeader>

        <CardContent class="pt-6">
          <Button class="w-full group/btn relative overflow-hidden bg-primary hover:bg-primary/90">
            <span class="relative z-10 flex items-center justify-center">
              Book Workshop • ₹199 <ArrowRight class="ml-2 h-4 w-4 group-hover/btn:translate-x-1 transition" />
            </span>
            <div class="absolute inset-0 bg-white/20 translate-y-full group-hover/btn:translate-y-0 transition-transform duration-500"></div>
          </Button>
        </CardContent>
      </Card>
    </div>

    <!-- Bottom CTA with flourish -->
    <div class="text-center mt-20">
      <p class="text-xl md:text-2xl text-muted-foreground mb-8">
        Available <span class="text-primary font-bold">Online</span> & 
        <span class="text-primary font-bold">Offline (We visit your college!)</span>
      </p>

      <Button 
        size="lg" 
        class="text-lg px-12 py-7 font-bold bg-gradient-to-r from-primary to-orange-600 shadow-2xl shadow-primary/30
               hover:shadow-primary/40 hover:scale-105 transition-all duration-300"
        href="https://wa.me/919876543210?text=Hi%20MazeMaxx%2C%20we%20want%20to%20book%20a%201-day%20workshop%20for%20our%20college!"
      >
        <Calendar class="mr-3 h-6 w-6" />
        Invite MazeMaxx to Your College
      </Button>

      <p class="mt-6 text-sm text-muted-foreground">
        500+ colleges already loved our workshops
      </p>
    </div>
  </div>
</section>