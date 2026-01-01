<script lang="ts">
  import H1 from "$lib/components/docs/H1.svelte";
  import SubHeading from "$lib/components/docs/SubHeading.svelte";
  import PreviewPlayground from "$lib/components/docs/PreviewPlayground.svelte";
  import PreviewMultipleFiles from "$lib/components/docs/PreviewMultipleFiles.svelte";
  import PreviewMultipleFilesCode from "$lib/components/docs/PreviewMultipleFiles.svelte?raw";
</script>

<H1>Preview Multiple Files</H1>
<SubHeading>A component for showcasing multiple files.</SubHeading>
<PreviewPlayground code={PreviewMultipleFilesCode} replay={true}>
  <PreviewMultipleFiles />
</PreviewPlayground>
