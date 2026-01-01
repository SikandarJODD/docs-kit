<script lang="ts">
  import H1 from "$lib/components/docs/H1.svelte";
  import SubHeading from "$lib/components/docs/SubHeading.svelte";
  import PreviewPlayground from "$lib/components/docs/PreviewPlayground.svelte";
  import PreviewPlaygroundComponent from "$lib/components/docs/PreviewPlayground.svelte";
  import PreviewPlaygroundCode from "$lib/components/docs/PreviewPlayground.svelte?raw";
</script>

<H1>Preview Playground</H1>
<SubHeading>A tabbed preview component with Preview and Code tabs.</SubHeading>
<PreviewPlayground code={PreviewPlaygroundCode} replay={true}>
  <PreviewPlaygroundComponent code={`<div>Example</div>`} replay={false}>
    <div>Example</div>
  </PreviewPlaygroundComponent>
</PreviewPlayground>
