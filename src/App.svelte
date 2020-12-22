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
  <div class="mt-6">
    <div class="columns scrollable">
      <div class="column is-two-ninth">
        <div class="card has-background-primary-light">
          <div class="card-image">
            <figure class="image">
              <img src="https://pbs.twimg.com/profile_images/1121395911849062400/7exmJEg4.png" alt="Book cover">
            </figure>
          </div>
          <div class="card-content">
            <p class="title is-5">Svelte Book</p>
            <p class="subtitle is-6 has-text-danger-dark">$44.99</p>
            <a href="/"  target="_blank" class="button is-primary is-fullwidth">Buy</a>
          </div>
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

  @media screen and (min-width: 769px) {
    .is-two-ninth {
      flex: none;
      width: 22.22%;
    }
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
