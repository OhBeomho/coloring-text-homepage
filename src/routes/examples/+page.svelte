<script>
  import Layout from "../../components/Layout.svelte"
  import content from "../../assets/examples.md?raw"
  import MarkdownIt from "markdown-it"

  const md = new MarkdownIt({ html: true })
</script>

<Layout>
  <main>
    {@html md.render(content)}
  </main>
</Layout>

<style>
  main {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 20px;
  }
</style>
