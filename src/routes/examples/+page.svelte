<script>
  import Layout from "../../components/Layout.svelte"
  import { html as content } from "../../assets/examples.md"
</script>

<Layout>
  <main>
    {@html content}
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
