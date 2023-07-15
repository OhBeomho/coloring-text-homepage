<script>
  import Layout from "../components/Layout.svelte"
  import Codeblock from "../components/Codeblock.svelte"
</script>

<Layout>
  <main>
    <h1>coloring-text</h1>
    <p>Make your text colorful!</p>
    <Codeblock>npm i coloring-text</Codeblock>
    <p>
      <a href="/docs" class="button">API Docs</a>
      <a href="/examples" class="button">See Examples</a>
    </p>
  </main>
</Layout>

<style>
  main {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  a.button {
    padding: 6px;
    border-radius: 6px;
    border: 1px solid rgb(80, 80, 80);
    color: rgb(80, 80, 80);
    margin: 4px;

    &:hover {
      background-color: rgb(230, 230, 230);
      text-decoration: none;
    }
  }
</style>
