<script lang="ts">
  import H1 from "$lib/components/docs/H1.svelte";
  import H2 from "$lib/components/docs/H2.svelte";
  import SubHeading from "$lib/components/docs/SubHeading.svelte";
  import PreviewPlayground from "$lib/components/docs/PreviewPlayground.svelte";
  import CodeSpan from "$lib/components/docs/code-span.svelte";
  import {
    OpenIn,
    OpenInTrigger,
    OpenInContent,
    OpenInLabel,
    OpenInSeparator,
    OpenInChatGPT,
    OpenInClaude,
    OpenInT3,
    OpenInV0,
    OpenInScira,
  } from "$lib/components/ai-elements/open-in-chat/index.js";
  import OpenInCode from "$lib/components/ai-elements/open-in-chat/OpenIn.svelte?raw";
  import { Button } from "$lib/components/ui/button/index.js";
  import { BotIcon } from "@lucide/svelte";
</script>

<H1>Open in Chat</H1>
<SubHeading
  >A dropdown menu component to quickly open queries in various AI chat
  assistants.</SubHeading
>

<PreviewPlayground code={OpenInCode} replay={true}>
  <OpenIn query="How do I create a Svelte component?">
    <OpenInTrigger>
      <Button variant="outline" size="sm">
        <BotIcon class="size-4 mr-2" />
        Ask AI
      </Button>
    </OpenInTrigger>
    <OpenInContent>
      <OpenInLabel>Chat Assistants</OpenInLabel>
      <OpenInChatGPT />
      <OpenInClaude />
      <OpenInSeparator />
      <OpenInLabel>Developer Tools</OpenInLabel>
      <OpenInT3 />
      <OpenInV0 />
      <OpenInScira />
    </OpenInContent>
  </OpenIn>
</PreviewPlayground>

<H2>Overview</H2>
<p class="text-sm text-muted-foreground mb-4">
  The <CodeSpan>OpenIn</CodeSpan> component provides a consistent interface for opening
  queries in different AI chat platforms. It's built on top of a dropdown menu and
  includes pre-configured options for popular AI assistants like ChatGPT, Claude,
  and more.
</p>

<H2>Components</H2>
<div class="space-y-4 text-sm mb-6">
  <div>
    <code class="text-xs bg-muted px-2 py-1 rounded">OpenIn</code>
    <p class="text-muted-foreground mt-1">
      Root component that provides context. Takes a <CodeSpan>query</CodeSpan> prop.
    </p>
  </div>
  <div>
    <code class="text-xs bg-muted px-2 py-1 rounded">OpenInTrigger</code>
    <p class="text-muted-foreground mt-1">
      Trigger button to open the dropdown menu.
    </p>
  </div>
  <div>
    <code class="text-xs bg-muted px-2 py-1 rounded">OpenInContent</code>
    <p class="text-muted-foreground mt-1">
      Container for the dropdown menu items.
    </p>
  </div>
  <div>
    <code class="text-xs bg-muted px-2 py-1 rounded">OpenInLabel</code>
    <p class="text-muted-foreground mt-1">Label for grouping menu items.</p>
  </div>
  <div>
    <code class="text-xs bg-muted px-2 py-1 rounded">OpenInSeparator</code>
    <p class="text-muted-foreground mt-1">Visual separator between groups.</p>
  </div>
</div>

<H2>Pre-built Integrations</H2>
<ul class="list-disc list-inside space-y-2 text-sm text-muted-foreground mb-6">
  <li><CodeSpan>OpenInChatGPT</CodeSpan> - Opens query in ChatGPT</li>
  <li><CodeSpan>OpenInClaude</CodeSpan> - Opens query in Claude</li>
  <li><CodeSpan>OpenInT3</CodeSpan> - Opens query in T3 Chat</li>
  <li><CodeSpan>OpenInV0</CodeSpan> - Opens query in Vercel v0</li>
  <li><CodeSpan>OpenInScira</CodeSpan> - Opens query in Scira</li>
</ul>

<H2>Usage Example</H2>
<pre class="bg-muted p-4 rounded-lg text-xs overflow-x-auto"><code
    >{`<OpenIn query="Your question here">
  <OpenInTrigger>
    <Button>Ask AI</Button>
  </OpenInTrigger>
  <OpenInContent>
    <OpenInChatGPT />
    <OpenInClaude />
  </OpenInContent>
</OpenIn>`}</code
  ></pre>
