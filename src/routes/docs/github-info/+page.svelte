<script lang="ts">
  import H1 from "$lib/components/docs/H1.svelte";
  import H2 from "$lib/components/docs/H2.svelte";
  import SubHeading from "$lib/components/docs/SubHeading.svelte";
  import PreviewPlayground from "$lib/components/docs/PreviewPlayground.svelte";
  import CodeSpan from "$lib/components/docs/code-span.svelte";
  import GithubInfo from "$lib/components/fumadocs/github-info/github-info.svelte";
  import GithubInfoCode from "$lib/components/fumadocs/github-info/github-info.svelte?raw";
</script>

<H1>GitHub Info</H1>
<SubHeading
  >Display GitHub repository information with stars and forks count.</SubHeading
>

<PreviewPlayground code={GithubInfoCode} replay={true}>
  <div class="space-y-3">
    <GithubInfo owner="sveltejs" repo="svelte" />
    <GithubInfo owner="shadcn-svelte" repo="shadcn-svelte" />
    <GithubInfo owner="SikandarJODD" repo="docs-kit" />
  </div>
</PreviewPlayground>

<H2>Overview</H2>
<p class="text-sm text-muted-foreground mb-4">
  The <CodeSpan>GithubInfo</CodeSpan> component fetches and displays GitHub repository
  information including the repository name, owner, and star count. It provides a
  clean, clickable link to the repository with automatic number humanization for
  large star counts.
</p>

<H2>Features</H2>
<ul class="list-disc list-inside space-y-2 text-sm text-muted-foreground mb-6">
  <li>Fetches real-time repository data from GitHub API</li>
  <li>Humanizes large numbers (e.g., 1.5K, 10K)</li>
  <li>Clickable link to the repository</li>
  <li>Hover effects for better UX</li>
  <li>Support for custom GitHub API base URL and tokens</li>
  <li>Responsive design for mobile and desktop</li>
</ul>

<H2>Props</H2>
<div class="space-y-3 text-sm mb-6">
  <div class="grid grid-cols-[120px_1fr] gap-2">
    <code class="text-xs bg-muted px-2 py-1 rounded">owner</code>
    <span class="text-muted-foreground"
      >GitHub repository owner/organization (required)</span
    >
  </div>
  <div class="grid grid-cols-[120px_1fr] gap-2">
    <code class="text-xs bg-muted px-2 py-1 rounded">repo</code>
    <span class="text-muted-foreground">GitHub repository name (required)</span>
  </div>
  <div class="grid grid-cols-[120px_1fr] gap-2">
    <code class="text-xs bg-muted px-2 py-1 rounded">token</code>
    <span class="text-muted-foreground"
      >GitHub API token for authenticated requests (optional)</span
    >
  </div>
  <div class="grid grid-cols-[120px_1fr] gap-2">
    <code class="text-xs bg-muted px-2 py-1 rounded">baseUrl</code>
    <span class="text-muted-foreground"
      >Custom GitHub API base URL (optional, default: "https://api.github.com")</span
    >
  </div>
</div>

<H2>Usage Example</H2>
<pre class="bg-muted p-4 rounded-lg text-xs overflow-x-auto"><code
    >{`\<script\>
  import GithubInfo from "$lib/components/fumadocs/github-info/github-info.svelte";
\<\/script\>

<GithubInfo owner="sveltejs" repo="svelte" />`}</code
  ></pre>

<H2>Number Humanization</H2>
<p class="text-sm text-muted-foreground mb-4">
  The component automatically converts large numbers to a more readable format:
</p>
<ul class="list-disc list-inside space-y-1 text-sm text-muted-foreground mb-6">
  <li>1,500 → 1.5K</li>
  <li>10,000 → 10K</li>
  <li>99,999 → 99K</li>
  <li>1,000,000+ → Displayed as-is</li>
</ul>
