<script>
  const year = new Date().getFullYear()
</script>

<div class="wrapper">
  <header>
    <nav>
      <a href="/" class="brand">coloring-text</a>
      <div>
        <a href="/docs">Docs</a>
        <a href="/examples">Examples</a>
      </div>
    </nav>
  </header>
  <main>
    <slot />
  </main>
  <footer>
    <p>Copyright {year}. OhBeomho.</p>
  </footer>
</div>
