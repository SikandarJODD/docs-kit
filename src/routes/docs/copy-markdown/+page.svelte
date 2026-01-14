<script lang="ts">
  import H1 from "$lib/components/docs/H1.svelte";
  import SubHeading from "$lib/components/docs/SubHeading.svelte";
  import PreviewPlayground from "$lib/components/docs/PreviewPlayground.svelte";
  import CopyMarkdown from "$lib/components/docs/copy-markdown.svelte";
  import CopyMarkdownCode from "$lib/components/docs/copy-markdown.svelte?raw";
  import CodeSpan from "$lib/components/docs/code-span.svelte";
</script>

<H1>Copy Markdown</H1>
<SubHeading
  >A button component to copy markdown content from a URL to clipboard.</SubHeading
>

<PreviewPlayground code={CopyMarkdownCode} replay={true}>
  <CopyMarkdown
    llmsTxtUrl="https://example.com/llms.txt"
    component="example-component"
    registry="docs-kit"
    source="documentation"
  />
</PreviewPlayground>

<H1>Usage</H1>
<p class="text-sm text-muted-foreground mb-4">
  The <CodeSpan>CopyMarkdown</CodeSpan> component allows users to fetch and copy
  markdown content from a specified URL. It's useful for copying documentation content
  for use with AI assistants.
</p>

<H1>Props</H1>
<div class="space-y-2 text-sm">
  <div class="grid grid-cols-[120px_1fr] gap-2">
    <code class="text-xs bg-muted px-2 py-1 rounded">llmsTxtUrl</code>
    <span class="text-muted-foreground"
      >The URL to fetch markdown content from (required)</span
    >
  </div>
  <div class="grid grid-cols-[120px_1fr] gap-2">
    <code class="text-xs bg-muted px-2 py-1 rounded">component</code>
    <span class="text-muted-foreground">The component name (optional)</span>
  </div>
  <div class="grid grid-cols-[120px_1fr] gap-2">
    <code class="text-xs bg-muted px-2 py-1 rounded">registry</code>
    <span class="text-muted-foreground">The registry name (optional)</span>
  </div>
  <div class="grid grid-cols-[120px_1fr] gap-2">
    <code class="text-xs bg-muted px-2 py-1 rounded">source</code>
    <span class="text-muted-foreground"
      >The source identifier (default: "documentation")</span
    >
  </div>
</div>
