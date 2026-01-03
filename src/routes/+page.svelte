<script lang="ts">
  import {
    H1,
    H2,
    H3,
    OrderedList,
    UnorderedList,
    Link,
    ListItem,
    Paragraph,
    Table,
    Tbody,
    Thead,
    Tr,
    Th,
    Td,
    Divider,
    Blockquote,
    Steps,
    Step,
  } from "$lib/components/motion-core-docs/markdown";
</script>

<div class="p-6">
  <H1>Svelte Docs Kit</H1>
  <H2>Svelte Docs Kit</H2>
  <H3>Svelte Docs Kit</H3>
  <Paragraph>
    Lorem ipsum dolor sit amet <Link href="#">Coding</Link>, adipisicing elit.
    Quidem temporibus esse sapiente quas totam fugiat at <Link href="#">it</Link
    >. Iusto, quas incidunt.
  </Paragraph>
  <OrderedList>
    <ListItem>First item</ListItem>
    <ListItem>Second item</ListItem>
    <ListItem>Third item</ListItem>
  </OrderedList>
  <UnorderedList>
    <ListItem>First item</ListItem>
    <ListItem>Second item</ListItem>
    <ListItem>Third item</ListItem>
  </UnorderedList>

  <Table>
    <Thead>
      <Tr>
        <Th>Header 1</Th>
        <Th>Header 2</Th>
        <Th>Header 3</Th>
      </Tr>
    </Thead>
    <Tbody>
      <Tr>
        <Td>Row 1, Cell 1</Td>
        <Td>Row 1, Cell 2</Td>
        <Td>Row 1, Cell 3</Td>
      </Tr>
      <Tr>
        <Td>Row 2, Cell 1</Td>
        <Td>Row 2, Cell 2</Td>
        <Td>Row 2, Cell 3</Td>
      </Tr>
      <Tr>
        <Td>Row 3, Cell 1</Td>
        <Td>Row 3, Cell 2</Td>
        <Td>Row 3, Cell 3</Td>
      </Tr>
    </Tbody>
  </Table>

  <Divider />
  <Blockquote>
    This is a blockquote. Lorem ipsum dolor sit amet, consectetur adipiscing
    elit. Integer posuere erat a ante.
  </Blockquote>

  <Divider />
  <Steps>
    <Step title="Step 1">
      lorem3000 ipsum dolor sit amet, consectetur adipiscing elit.
    </Step>
    <Step title="Step 2">This is the second step.</Step>
    <Step title="Step 3">This is the third step.</Step>
  </Steps>
</div>
