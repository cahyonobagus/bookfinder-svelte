<script>
  import Book from './components/Book.svelte'

  let query = ''
  let books = []
  let isProcessing = false

  async function handleClickSearch(){
    isProcessing = true
    await fetch(`https://api.itbook.store/1.0/search/${query}`)
    .then(response => response.json())
    .then(data => {
      books = data.books
      isProcessing = false
    })
    .catch(error => {
      alert('something went wrong')
      console.error(error)
      isProcessing = false
    })
  }

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
        <div class="mt-2 columns is-centered">
          <button on:click={handleClickSearch} class="button is-primary">Search</button>
        </div>
      </div>
    </div>
  </div>
  <div class="mt-6">
    <div class="columns scrollable">
      {#if books.length == 0 }
        {#if isProcessing }
          <progress class="progress is-small is-primary" max="100"></progress>
        {/if }
      {:else }
        {#each books as book, index (index) }
          <Book book={book}/>
        {/each}
      {/if }
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

  /* Hide scrollbar for Chrome, Safari and Opera */
  .scrollable::-webkit-scrollbar {
    display: none;
  }
  /* Hide scrollbar for IE, Edge, Firefox */
  .scrollable {
    overflow: auto;
    -ms-overflow-style: none;  /* IE and Edge */
    scrollbar-width: none;  /* Firefox */
  }

</style>
