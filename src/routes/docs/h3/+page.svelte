<script lang="ts">
  import H1 from "$lib/components/docs/H1.svelte";
  import SubHeading from "$lib/components/docs/SubHeading.svelte";
  import PreviewPlayground from "$lib/components/docs/PreviewPlayground.svelte";
  import H3Component from "$lib/components/docs/H3.svelte";
  import H3Code from "$lib/components/docs/H3.svelte?raw";
</script>

<H1>H3</H1>
<SubHeading>A heading component for level 3.</SubHeading>
<PreviewPlayground code={H3Code} replay={true}>
  <H3Component>Example Heading</H3Component>
</PreviewPlayground>
