<script lang="ts">
  import { Badge } from "$lib/components/ui/badge";
  import { Button } from "$lib/components/ui/button";
  import {
    Flame,
    Waves,
    Activity,
    ArrowRight,
    Shield,
    Users,
    BookOpen,
    Star,
    Boxes
  } from "lucide-svelte";

  const disasterModules = [
    {
      name: "Forest Fire",
      description: "Real-time fire tracking & evacuation routes",
      icon: Flame,
      colors: {
        base: "red",
        gradient: "from-red-500/10 to-orange-500/10",
        hoverGradient: "from-red-500/20 to-orange-500/20"
      }
    },
    {
      name: "Flood",
      description: "Flood history, water bed & intensity monitoring",
      icon: Waves,
      colors: {
        base: "blue",
        gradient: "from-blue-500/10 to-cyan-500/10",
        hoverGradient: "from-blue-500/20 to-cyan-500/20"
      }
    },
    {
      name: "Earthquake",
      description: "Seismic history, area & intensity monitoring",
      icon: Activity,
      colors: {
        base: "emerald",
        gradient: "from-emerald-500/10 to-green-500/10",
        hoverGradient: "from-emerald-500/20 to-green-500/20"
      }
    }
  ];

  const coreFeatures = [
    {
      icon: Shield,
      title: "Comprehensive Coverage",
      description:
        "Deep, focused implementation for each disaster type with purposeful feature development."
    },
    {
      icon: Users,
      title: "Community Network",
      description:
        "Local assistance platforms and real-time crisis communication for community support."
    },
    {
      icon: BookOpen,
      title: "Preparedness Training",
      description:
        "Interactive guides, scenario simulations and regular drill schedules for readiness."
    }
  ];

  const emergencyStats = [
    { value: "24/7", label: "Emergency Response" },
    { value: "15,000+", label: "Registered Users" },
    { value: "500+", label: "Emergency Centers" },
    { value: "99.9%", label: "System Uptime" }
  ];

  const emergencyContacts = [
    { name: "Emergency", number: "911" },
    { name: "Poison Control", number: "1-800-222-1222" },
    { name: "Crisis Hotline", number: "988" }
  ];
</script>

<div
  class="animate-fade-in relative flex min-h-[100vh] w-full flex-col items-center justify-center overflow-hidden bg-inherit px-4"
>
  <!-- Background Gradient -->
  <div class="absolute inset-0 flex items-center justify-center">
    <div
      class="absolute h-full w-full bg-gradient-to-r from-primary/10 to-accent/10 blur-2xl saturate-200 [mask-image:radial-gradient(ellipse_at_center,transparent_20%,black)]"
    ></div>
  </div>

  <div class="relative z-10 mx-auto w-full max-w-7xl px-6 py-20 md:py-36">
    <div class="flex flex-col items-center gap-8 md:gap-12">
      <!-- Hero Section -->
      <div
        class="flex w-full flex-col space-y-8 md:flex-row md:items-start md:justify-between md:space-x-12 md:space-y-0"
      >
        <div class="text-center md:flex-1 md:text-left">
          <h1
            class="animate-fade-up xs:text-6xl bg-gradient-to-tr from-primary via-foreground to-accent bg-clip-text text-5xl font-extrabold tracking-tight text-transparent drop-shadow-sm sm:text-6xl md:text-7xl lg:text-8xl"
          >
            AURA<span class="text-primary">.</span>
          </h1>
          <p
            class="animate-fade-up xs:text-3xl mt-4 text-2xl font-semibold tracking-wide text-muted-foreground/90 sm:text-4xl md:text-5xl lg:text-6xl"
          >
            adaptive unified resilience & alerts
          </p>
          <p
            class="animate-fade-up mt-8 max-w-2xl text-base leading-relaxed text-muted-foreground/90 backdrop-blur-sm sm:text-lg md:text-xl"
          >
            Your one-stop solution for disaster preparedness, response, and recovery.
          </p>
        </div>

        <!-- Risk Assessment Card -->
        <div class="animate-fade-up group relative w-full md:w-2/5">
          <div
            class="absolute -inset-1 rounded-2xl bg-gradient-to-r from-primary/50 to-accent/50 opacity-30 blur-md transition duration-300 group-hover:opacity-100 group-hover:duration-200"
          ></div>
          <div
            class="absolute -inset-[100px] animate-[pulse_4s_ease-in-out_infinite] rounded-full bg-gradient-to-r from-primary/20 via-accent/20 to-primary/20 opacity-30 blur-3xl"
          ></div>
          <div
            class="absolute -inset-[50px] animate-[pulse_6s_ease-in-out_infinite_1s] rounded-full bg-gradient-to-r from-accent/20 via-primary/20 to-accent/20 opacity-20 blur-2xl"
          ></div>

          <div
            class="relative overflow-hidden rounded-xl border border-border/30 bg-background/90 shadow-xl backdrop-blur-xl transition-all duration-300 group-hover:border-border/50"
          >
            <div class="space-y-4 p-6">
              <div class="flex items-center justify-between">
                <h3
                  class="bg-gradient-to-r from-primary to-accent bg-clip-text text-2xl font-semibold text-transparent"
                >
                  Risk Assessment
                </h3>
                <div
                  class="flex h-8 w-8 items-center justify-center rounded-full bg-gradient-to-r from-primary/20 to-accent/20 backdrop-blur-sm"
                >
                  <div class="h-2 w-2 animate-pulse rounded-full bg-primary"></div>
                </div>
              </div>

              <div class="space-y-2">
                <div class="flex items-center space-x-3 text-muted-foreground/80">
                  <Activity class="h-4 w-4 text-primary" />
                  <span class="text-sm"
                    >Dynamic Risk Score: <Badge variant="outline">High</Badge></span
                  >
                </div>
                <div class="h-1 overflow-hidden rounded-full bg-background/50 backdrop-blur-sm">
                  <div
                    class="h-full w-2/3 animate-pulse rounded-full bg-gradient-to-r from-primary to-accent"
                  ></div>
                </div>
              </div>

              <div class="space-y-3">
                <p class="text-sm text-muted-foreground/70">
                  Real-time hazard monitoring and geographic risk analysis for your location
                </p>

                <div class="space-y-1 text-sm text-muted-foreground/70">
                  <div class="flex items-center space-x-2">
                    <Flame class="h-3 w-3 text-red-500" />
                    <span
                      >Forest fire risk <Badge variant="outline">Critical</Badge> - High temperature</span
                    >
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Disaster Modules Section -->
      <div class="animate-fade-up mx-auto mt-24 flex w-full max-w-6xl flex-col gap-12">
        <div class="relative mb-12 text-center">
          <div
            class="absolute -inset-[50px] animate-[pulse_6s_ease-in-out_infinite] rounded-full bg-gradient-to-r from-primary/10 via-accent/10 to-primary/10 opacity-30 blur-2xl"
          ></div>
          <div class="flex flex-col items-center justify-center gap-3 md:flex-row">
            <div class="rounded-xl bg-blue-500/10 p-3">
              <Boxes class="h-8 w-8 text-blue-500" />
            </div>
            <h3 class="text-3xl font-bold text-blue-500">Disaster Modules</h3>
          </div>
          <p class="mx-auto mt-4 max-w-2xl text-lg leading-relaxed text-muted-foreground/80">
            Each module is designed to be of utmost utility and ease of use. Completeness and
            reliability are paramount.
          </p>
        </div>

        <div class="grid grid-cols-1 gap-8 sm:grid-cols-3">
          {#each disasterModules as module}
            <div
              class="group relative rounded-3xl border border-border/10 bg-background/10 p-8 backdrop-blur-sm transition-all duration-500 hover:scale-[1.02] hover:border-border/30 hover:bg-background/20 hover:shadow-xl"
            >
              <div
                class="absolute -inset-1 rounded-[24px] bg-gradient-to-r {module.colors
                  .gradient} blur-xl"
              ></div>
              <div
                class="absolute -inset-1 rounded-[24px] bg-gradient-to-r {module.colors
                  .hoverGradient} opacity-0 blur transition duration-500 group-hover:opacity-100"
              ></div>

              <div class="relative flex flex-col gap-4">
                <div class="flex items-center gap-3">
                  <div
                    class="rounded-xl bg-{module.colors
                      .base}-500/10 p-2 transition-colors duration-500 group-hover:bg-{module.colors
                      .base}-500/20"
                  >
                    <svelte:component
                      this={module.icon}
                      class="h-6 w-6 text-{module.colors.base}-500 group-hover:animate-bounce"
                    />
                  </div>
                  <h3
                    class="text-2xl font-medium text-{module.colors
                      .base}-500 transition-colors duration-500 group-hover:text-{module.colors
                      .base}-400"
                  >
                    {module.name}
                  </h3>
                </div>
                <p
                  class="text-muted-foreground/70 transition-colors duration-500 group-hover:text-muted-foreground/90"
                >
                  {module.description}
                </p>
                <div
                  class="flex items-center gap-2 text-{module.colors
                    .base}-500 transition-colors duration-500 group-hover:translate-x-1 group-hover:text-{module
                    .colors.base}-400"
                >
                  <span>Explore Module</span>
                  <ArrowRight
                    class="h-4 w-4 transition-transform duration-300 group-hover:translate-x-1"
                  />
                </div>
              </div>
            </div>
          {/each}
        </div>
      </div>

      <!-- Core Features -->
      <div class="relative mt-16 w-full">
        <div class="relative mb-12 text-center">
          <div
            class="absolute -inset-[50px] animate-[pulse_6s_ease-in-out_infinite] rounded-full bg-gradient-to-r from-primary/10 via-accent/10 to-primary/10 opacity-30 blur-2xl"
          ></div>
          <div class="flex flex-col items-center justify-center gap-3 md:flex-row">
            <div class="rounded-xl bg-blue-500/10 p-3">
              <Star class="h-8 w-8 text-blue-500" />
            </div>
            <h3 class="text-3xl font-bold text-blue-500">Core Features</h3>
          </div>
          <p class="mx-auto mt-4 max-w-2xl text-lg leading-relaxed text-muted-foreground/80">
            Empowering users with the tools they need to stay prepared and informed.
          </p>
        </div>

        <div
          class="absolute inset-0 rounded-3xl bg-gradient-to-r from-primary/5 via-accent/5 to-primary/5 blur-3xl"
        ></div>
        <div class="relative grid grid-cols-1 gap-8 px-4 py-8 md:grid-cols-3 md:p-8">
          {#each coreFeatures as feature}
            <div
              class="group rounded-2xl border border-border/30 bg-background/40 p-6 backdrop-blur-xl transition-all duration-300 hover:border-border/50 md:p-8"
            >
              <div
                class="mb-6 flex h-12 w-12 items-center justify-center rounded-xl bg-primary/10 transition-transform duration-300 group-hover:scale-110"
              >
                <svelte:component this={feature.icon} class="h-6 w-6 text-primary" />
              </div>
              <h3 class="mb-3 text-xl font-semibold">{feature.title}</h3>
              <p class="text-muted-foreground/70">{feature.description}</p>
            </div>
          {/each}
        </div>
      </div>

      <!-- Emergency Stats Section -->
      <div class="relative w-full bg-gradient-to-b from-transparent to-primary/5 pt-24">
        <div class="mx-auto max-w-7xl px-6 pb-20">
          <div class="grid grid-cols-1 gap-8 md:grid-cols-4">
            {#each emergencyStats as stat}
              <div class="text-center">
                <div class="text-4xl font-bold text-primary">{stat.value}</div>
                <div class="mt-2 text-sm text-muted-foreground/70">{stat.label}</div>
              </div>
            {/each}
          </div>

          <div class="mt-16 flex flex-col items-center justify-center gap-4 text-center">
            <h4 class="text-xl font-semibold">Emergency Contacts</h4>
            <div class="flex flex-wrap justify-center gap-4">
              {#each emergencyContacts as contact}
                <div class="rounded-lg bg-background/50 px-6 py-3 backdrop-blur-sm">
                  <div class="font-semibold">{contact.name}</div>
                  <div class="text-lg text-primary">{contact.number}</div>
                </div>
              {/each}
            </div>
          </div>
        </div>

        <!-- Bottom wave decoration -->
        <div class="absolute bottom-0 left-0 w-full overflow-hidden leading-none">
          <svg
            class="relative block h-[100px] w-full"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 1200 120"
            preserveAspectRatio="none"
          >
            <path
              d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z"
              class="fill-primary/10"
            ></path>
          </svg>
        </div>
      </div>
    </div>
  </div>
</div>
