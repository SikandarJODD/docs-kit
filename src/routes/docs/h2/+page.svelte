<script lang="ts">
  import H1 from "$lib/components/docs/H1.svelte";
  import SubHeading from "$lib/components/docs/SubHeading.svelte";
  import PreviewPlayground from "$lib/components/docs/PreviewPlayground.svelte";
  import H2Component from "$lib/components/docs/H2.svelte";
  import H2Code from "$lib/components/docs/H2.svelte?raw";
</script>

<H1>H2</H1>
<SubHeading>A heading component for level 2.</SubHeading>
<PreviewPlayground code={H2Code} replay={true}>
  <H2Component>Example Heading</H2Component>
</PreviewPlayground>
