<script lang="ts">
  import H1 from "$lib/components/docs/H1.svelte";
  import SubHeading from "$lib/components/docs/SubHeading.svelte";
  import PreviewPlayground from "$lib/components/docs/PreviewPlayground.svelte";
  import H1Component from "$lib/components/docs/H1.svelte";
  import H1Code from "$lib/components/docs/H1.svelte?raw";
</script>

<H1>H1</H1>
<SubHeading>A heading component for level 1.</SubHeading>
<PreviewPlayground code={H1Code} replay={true}>
  <H1Component>Example Heading</H1Component>
</PreviewPlayground>
