<script>
  const year = new Date().getFullYear()
</script>

<div class="wrapper">
  <header>
    <nav>
      <a href="/" class="brand">coloring-text</a>
      <div class="nav-items">
        <a href="/docs">Docs</a>
        <a href="/examples">Examples</a>
      </div>
    </nav>
  </header>
  <slot />
  <footer>
    <p>Copyright {year}. OhBeomho.</p>
  </footer>
</div>

<style>
  :global(body) {
    margin: 0;
  }

  :global(a) {
    color: rgb(0, 100, 255);
    text-decoration: none;

    &:hover {
      text-decoration: underline;
    }
  }

  .wrapper {
    min-height: 100vh;
    display: flex;
    flex-direction: column;

    & nav {
      padding: 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: relative;
      z-index: 10;
      box-shadow: 0 3px 10px 0 rgba(0, 0, 0, 0.15);

      & .brand {
        color: black;
        font-size: 24px;
      }

      & .nav-items a {
        margin: 0 8px;
      }
    }

    & footer {
      background-color: lightgray;
      color: rgb(80, 80, 80);
      text-align: center;
    }
  }
</style>
