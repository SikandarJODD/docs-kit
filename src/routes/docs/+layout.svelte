<script lang="ts">
  import AppSidebar from "$lib/components/app-sidebar.svelte";
  import * as Sidebar from "$lib/components/ui/sidebar/index.js";
  import * as Breadcrumb from "$lib/components/ui/breadcrumb/index.js";
  import { Separator } from "$lib/components/ui/separator/index.js";
  import { page } from "$app/state";

  let { children } = $props();

  // Derive breadcrumbs from current path
  // $: pathname = $page.url.pathname;
  // $: isComponentPage = pathname.startsWith("/docs/") && pathname !== "/docs";
  // $: componentName = isComponentPage
  //   ? pathname.split("/").pop()?.replace("-", " ")
  //   : null;
  let pathname = $derived(page.url.pathname);
  let isComponentPage = $derived(
    pathname.startsWith("/docs/") && pathname !== "/docs"
  );
  let componentName = $derived(
    isComponentPage ? pathname.split("/").pop()?.replace("-", " ") : null
  );
</script>

<Sidebar.Provider>
  <AppSidebar />
  <Sidebar.Inset>
    {#if isComponentPage}
      <header
        class="flex h-16 shrink-0 items-center gap-2 transition-[width,height] ease-linear group-has-data-[collapsible=icon]/sidebar-wrapper:h-12"
      >
        <div class="flex items-center gap-2 px-4">
          <Sidebar.Trigger class="-ms-1" />
          <Separator
            orientation="vertical"
            class="me-2 data-[orientation=vertical]:h-4"
          />
          <Breadcrumb.Root>
            <Breadcrumb.List>
              <Breadcrumb.Item class="hidden md:block">
                <Breadcrumb.Link href="/docs">Components</Breadcrumb.Link>
              </Breadcrumb.Item>
              <Breadcrumb.Separator class="hidden md:block" />
              <Breadcrumb.Item>
                <Breadcrumb.Page>{componentName}</Breadcrumb.Page>
              </Breadcrumb.Item>
            </Breadcrumb.List>
          </Breadcrumb.Root>
        </div>
      </header>
    {/if}
    <div class="px-4 py-4">
      {@render children()}
    </div>
  </Sidebar.Inset>
</Sidebar.Provider>
