<script>
  import ChevronRight from "@lucide/svelte/icons/chevron-right";
  import Menu from "@lucide/svelte/icons/menu";
  import X from "@lucide/svelte/icons/x";
  import Button from "$lib/components/ui/button/button.svelte";

  // You can store Hero Header Component in separate file
  // I have used snippet for better readability

  // Hero Header Component

  import { cn } from "$lib/utils";
  import { scrollY } from "svelte/reactivity/window";

  let menuItems = [
    { name: "Home", href: "#a" },
    { name: "Features", href: "#a" },
  ];
  let menuState = $state(false);
  let isScrolled = $derived.by(() => {
    if (scrollY.current !== undefined && scrollY.current > 50) {
      return true;
    }
    return false;
  });
</script>

<main class="overflow-hidden">
  <div class="absolute inset-0 isolate hidden contain-strict lg:block">
    <div
      class="w-140 h-320 -translate-y-87.5 absolute left-0 top-0 -rotate-45 rounded-full bg-[radial-gradient(68.54%_68.72%_at_55.02%_31.46%,hsla(0,0%,85%,.08)_0,hsla(0,0%,55%,.02)_50%,hsla(0,0%,45%,0)_80%)]"
    ></div>
    <div
      class="h-320 absolute left-0 top-0 w-60 -rotate-45 rounded-full bg-[radial-gradient(50%_50%_at_50%_50%,hsla(0,0%,85%,.06)_0,hsla(0,0%,45%,.02)_80%,transparent_100%)] [translate:5%_-50%]"
    ></div>
    <div
      class="h-320 -translate-y-87.5 absolute left-0 top-0 w-60 -rotate-45 bg-[radial-gradient(50%_50%_at_50%_50%,hsla(0,0%,85%,.04)_0,hsla(0,0%,45%,.02)_80%,transparent_100%)]"
    ></div>
  </div>
  <section>
    <div class="relative pt-24">
      <div
        class="absolute inset-0 -z-10 size-full [background:radial-gradient(125%_125%_at_50%_100%,transparent_0%,var(--color-background)_75%)]"
      ></div>
      <div class="mx-auto max-w-5xl px-6">
        <div class="sm:mx-auto lg:mr-auto lg:mt-0">
          <h1
            class="mt-8 max-w-2xl text-balance text-5xl font-medium md:text-6xl lg:mt-16"
          >
            Svelte Docs Kit
          </h1>
          <p class="mt-8 max-w-2xl text-pretty text-lg">
            Build to solve the common problems faced when creating documentation
            sites with Svelte and SvelteKit.
          </p>

          <div class="mt-12 flex items-center gap-2">
            <Button href="/docs" size="lg">Components</Button>
            <Button
              size="lg"
              variant="secondary"
              href="https://github.com/sponsors/SikandarJODD"
              target="_blank">Support</Button
            >
          </div>
        </div>
      </div>
    </div>
  </section>
</main>
