<script lang="ts">
  import H1 from "$lib/components/docs/H1.svelte";
  import SubHeading from "$lib/components/docs/SubHeading.svelte";
  import PreviewPlayground from "$lib/components/docs/PreviewPlayground.svelte";
  import SubHeadingComponent from "$lib/components/docs/SubHeading.svelte";
  import SubHeadingCode from "$lib/components/docs/SubHeading.svelte?raw";
</script>

<H1>Sub Heading</H1>
<SubHeading>A subheading component using a paragraph tag.</SubHeading>
<PreviewPlayground code={SubHeadingCode} replay={true}>
  <SubHeadingComponent>Example subheading</SubHeadingComponent>
</PreviewPlayground>
