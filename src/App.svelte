<script>
  let query = ''

  // put console.log to show the changes of the state (query)
  $: console.log(query)
</script>

<div class="container">
  <div class="mt-6">
    <div class="columns is-centered">
      <div class="column is-4">
        <span class="main-title">FindBooks</span>
        <input 
          bind:value={query}
          class="input is-primary" 
          type="text" 
          placeholder="Search books by title"
        >
        <!-- put text here to show the changes of the state (query) -->
        <p>{query}</p>
        <div class="mt-2 columns is-centered">
          <button class="button is-primary">Search</button>
        </div>
      </div>
    </div>
  </div>
</div>

<svelte:head>
  <!-- BULMA CSS -->
	<link 
		rel="stylesheet" 
    href="https://cdn.jsdelivr.net/npm/bulma@0.9.1/css/bulma.min.css"
  >
    
  <!-- GOOGLE FONTS -->
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link 
    rel="stylesheet"
    href="https://fonts.googleapis.com/css2?family=Monoton&display=swap" 
  >
</svelte:head>

<style>
  .main-title {
    font-family: 'Monoton', cursive;
    font-size: 64px;
    color: green;
  }
</style>
