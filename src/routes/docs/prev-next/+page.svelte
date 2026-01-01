<script lang="ts">
  import H1 from "$lib/components/docs/H1.svelte";
  import SubHeading from "$lib/components/docs/SubHeading.svelte";
  import PreviewPlayground from "$lib/components/docs/PreviewPlayground.svelte";
  import PrevNext from "$lib/components/docs/PrevNext.svelte";
  import PrevNextCode from "$lib/components/docs/PrevNext.svelte?raw";
</script>

<H1>Prev Next</H1>
<SubHeading>A component for previous/next navigation.</SubHeading>
<PreviewPlayground code={PrevNextCode} replay={true}>
  <PrevNext />
</PreviewPlayground>
