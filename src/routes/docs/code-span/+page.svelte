<script lang="ts">
  import H1 from "$lib/components/docs/H1.svelte";
  import SubHeading from "$lib/components/docs/SubHeading.svelte";
  import PreviewPlayground from "$lib/components/docs/PreviewPlayground.svelte";
  import CodeSpan from "$lib/components/docs/code-span.svelte";
  import CodeSpanCode from "$lib/components/docs/code-span.svelte?raw";
</script>

<H1>Code Span</H1>
<SubHeading>A simple inline code span component.</SubHeading>
<PreviewPlayground code={CodeSpanCode} replay={true}>
  <CodeSpan>example code</CodeSpan>
</PreviewPlayground>
