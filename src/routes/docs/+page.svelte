<script>
  import Layout from "../../components/Layout.svelte"

  let currentDoc = "color"
  let docHTML
  let loading = true

  function loadDoc(doc) {
    if (loading) {
      return
    }

    loading = true

    import(`../../assets/${doc}.md`).then((content) => {
      docHTML = content.html
      currentDoc = doc
      loading = false
    })
  }

  loadDoc(currentDoc)
</script>

<Layout>
  <main>
    <div class="list">
      <h3>Functions</h3>
      {#each ["color", "style"] as doc}
        <button
          class={`doc ${doc === currentDoc ? "selected" : ""}`}
          on:click={() => currentDoc !== doc && loadDoc(currentDoc === "color" ? "style" : "color")}
          >{doc}</button
        >
      {/each}
    </div>
    <div class="content">
      {@html loading ? "<strong>Loading...</strong>" : docHTML}
    </div>
  </main>
</Layout>

<style>
  main {
    flex: 1;
    display: flex;

    & .list {
      display: flex;
      flex-direction: column;
      text-align: center;
      background-color: rgb(240, 240, 240);
      flex: 0.3;

      & .doc {
        padding: 4px;
        border: 0;
      }

      & .doc.selected {
        background-color: rgb(230, 230, 230);
      }
    }

    & .content {
      flex: 1;
      padding: 8px;
    }
  }
</style>
