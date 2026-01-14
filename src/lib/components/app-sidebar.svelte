<script lang="ts" module>
  import AudioWaveformIcon from "@lucide/svelte/icons/audio-waveform";
  import BookOpenIcon from "@lucide/svelte/icons/book-open";
  import BotIcon from "@lucide/svelte/icons/bot";
  import ChartPieIcon from "@lucide/svelte/icons/chart-pie";
  import CommandIcon from "@lucide/svelte/icons/command";
  import FrameIcon from "@lucide/svelte/icons/frame";
  import GalleryVerticalEndIcon from "@lucide/svelte/icons/gallery-vertical-end";
  import MapIcon from "@lucide/svelte/icons/map";
  import Settings2Icon from "@lucide/svelte/icons/settings-2";
  import SquareTerminalIcon from "@lucide/svelte/icons/square-terminal";

  // This is sample data.
  const data = {
    user: {
      name: "Bhide Svelte",
      desc: "I Love Svelte",
      avatar: "https://avatars.githubusercontent.com/u/203207203?s=40&v=4",
    },
    navMain: [
      {
        title: "Home",
        url: "/",
        icon: CommandIcon,
        items: [
          {
            title: "Home",
            url: "/",
          },
          {
            title: "Get Started",
            url: "/docs/get-started",
          },
          {
            title: "Introduction",
            url: "/docs/introduction",
          },
          {
            title: "Installation",
            url: "/docs/installation",
          },
        ],
      },
      {
        title: "Components",
        url: "#",
        icon: BotIcon,
        items: [
          {
            title: "Preview Playground",
            url: "/docs/preview-playground",
          },
          {
            title: "Previous Next",
            url: "/docs/prev-next",
          },
          {
            title: "Heading",
            url: "/docs/heading",
          },
          {
            title: "Preview - Multiple Files",
            url: "/docs/preview-multiple-files",
          },
          {
            title: "Code Span",
            url: "/docs/code-span",
          },
          {
            title: "H1",
            url: "/docs/h1",
          },
          {
            title: "H2",
            url: "/docs/h2",
          },
          {
            title: "H3",
            url: "/docs/h3",
          },
          {
            title: "Sub Heading",
            url: "/docs/sub-heading",
          },
          {
            title: "Copy Markdown",
            url: "/docs/copy-markdown",
          },
          {
            title: "Open in Chat",
            url: "/docs/open-in-chat",
          },
        ],
      },
      {
        title: "Shadcn Svelte Extra",
        url: "#",
        icon: BookOpenIcon,
        items: [
          {
            title: "Table of Contents",
            url: "/docs/toc",
          },
          {
            title: "PM Command",
            url: "/docs/pm-command",
          },
        ],
      },
      {
        title: "Fumadocs Inspiration",
        url: "#",
        icon: Settings2Icon,
        items: [
          {
            title: "Autotype Table",
            url: "/docs/autotype-table",
          },
          {
            title: "File Structure",
            url: "/docs/file-structure",
          },
          {
            title: "Github Info",
            url: "/docs/github-info",
          },
          {
            title: "Zoomable Image",
            url: "/docs/zoomable-image",
          },
        ],
      },
    ],
    projects: [
      {
        name: "Design Engineering",
        url: "#",
        icon: FrameIcon,
      },
      {
        name: "Sales & Marketing",
        url: "#",
        icon: ChartPieIcon,
      },
      {
        name: "Travel",
        url: "#",
        icon: MapIcon,
      },
    ],
  };
</script>

<script lang="ts">
  import NavMain from "./nav-main.svelte";
  import NavProjects from "./nav-projects.svelte";
  import NavUser from "./nav-user.svelte";
  import TeamSwitcher from "./team-switcher.svelte";
  import * as Sidebar from "$lib/components/ui/sidebar/index.js";
  import type { ComponentProps } from "svelte";

  let {
    ref = $bindable(null),
    collapsible = "icon",
    ...restProps
  }: ComponentProps<typeof Sidebar.Root> = $props();
</script>

<Sidebar.Root {collapsible} {...restProps}>
  <Sidebar.Header>
    <!-- <TeamSwitcher teams={data.teams} /> -->
    <Sidebar.Menu>
      <Sidebar.MenuItem>
        <Sidebar.MenuButton size="lg">
          {#snippet child({ props })}
            <a href="##" {...props}>
              <div
                class=" bg-linear-60 from-neutral-700 to-neutral-900 text-sidebar-primary-foreground flex aspect-square size-8 items-center justify-center rounded-lg"
              >
                <!-- <CommandIcon class="size-4" /> -->
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="128"
                  height="128"
                  class="size-4"
                  viewBox="0 0 24 24"
                  fill="none"
                  role="img"
                  color="currentColor"
                >
                  <path
                    opacity="0.4"
                    d="M2 18C2 16.4596 2 15.6893 2.34673 15.1235C2.54074 14.8069 2.80693 14.5407 3.12353 14.3467C3.68934 14 4.45956 14 6 14C7.54044 14 8.31066 14 8.87647 14.3467C9.19307 14.5407 9.45926 14.8069 9.65327 15.1235C10 15.6893 10 16.4596 10 18C10 19.5404 10 20.3107 9.65327 20.8765C9.45926 21.1931 9.19307 21.4593 8.87647 21.6533C8.31066 22 7.54044 22 6 22C4.45956 22 3.68934 22 3.12353 21.6533C2.80693 21.4593 2.54074 21.1931 2.34673 20.8765C2 20.3107 2 19.5404 2 18Z"
                    stroke="currentColor"
                    stroke-width="1.5"
                  ></path>
                  <path
                    d="M14 18C14 16.4596 14 15.6893 14.3467 15.1235C14.5407 14.8069 14.8069 14.5407 15.1235 14.3467C15.6893 14 16.4596 14 18 14C19.5404 14 20.3107 14 20.8765 14.3467C21.1931 14.5407 21.4593 14.8069 21.6533 15.1235C22 15.6893 22 16.4596 22 18C22 19.5404 22 20.3107 21.6533 20.8765C21.4593 21.1931 21.1931 21.4593 20.8765 21.6533C20.3107 22 19.5404 22 18 22C16.4596 22 15.6893 22 15.1235 21.6533C14.8069 21.4593 14.5407 21.1931 14.3467 20.8765C14 20.3107 14 19.5404 14 18Z"
                    stroke="currentColor"
                    stroke-width="1.5"
                  ></path>
                  <path
                    d="M2 6C2 4.45956 2 3.68934 2.34673 3.12353C2.54074 2.80693 2.80693 2.54074 3.12353 2.34673C3.68934 2 4.45956 2 6 2C7.54044 2 8.31066 2 8.87647 2.34673C9.19307 2.54074 9.45926 2.80693 9.65327 3.12353C10 3.68934 10 4.45956 10 6C10 7.54044 10 8.31066 9.65327 8.87647C9.45926 9.19307 9.19307 9.45926 8.87647 9.65327C8.31066 10 7.54044 10 6 10C4.45956 10 3.68934 10 3.12353 9.65327C2.80693 9.45926 2.54074 9.19307 2.34673 8.87647C2 8.31066 2 7.54044 2 6Z"
                    stroke="currentColor"
                    stroke-width="1.5"
                  ></path>
                  <path
                    opacity="0.4"
                    d="M14 6C14 4.45956 14 3.68934 14.3467 3.12353C14.5407 2.80693 14.8069 2.54074 15.1235 2.34673C15.6893 2 16.4596 2 18 2C19.5404 2 20.3107 2 20.8765 2.34673C21.1931 2.54074 21.4593 2.80693 21.6533 3.12353C22 3.68934 22 4.45956 22 6C22 7.54044 22 8.31066 21.6533 8.87647C21.4593 9.19307 21.1931 9.45926 20.8765 9.65327C20.3107 10 19.5404 10 18 10C16.4596 10 15.6893 10 15.1235 9.65327C14.8069 9.45926 14.5407 9.19307 14.3467 8.87647C14 8.31066 14 7.54044 14 6Z"
                    stroke="currentColor"
                    stroke-width="1.5"
                  ></path>
                </svg>
              </div>
              <div class="grid flex-1 text-start text-sm leading-tight">
                <span class="truncate font-medium">Svelte Docs Kit</span>
                <span class="truncate text-xs">Free Docs Components</span>
              </div>
            </a>
          {/snippet}
        </Sidebar.MenuButton>
      </Sidebar.MenuItem>
    </Sidebar.Menu>
  </Sidebar.Header>
  <Sidebar.Content>
    <NavMain items={data.navMain} />
    <!-- <NavProjects projects={data.projects} /> -->
  </Sidebar.Content>
  <Sidebar.Footer>
    <NavUser user={data.user} />
  </Sidebar.Footer>
  <Sidebar.Rail />
</Sidebar.Root>
