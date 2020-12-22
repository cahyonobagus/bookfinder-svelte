<script>
  export let book = {
    image: '',
    title: '',
    price: '',
    url: ''
  }
</script>

<div class="column is-two-ninth">
  <div class="card has-background-primary-light">
    <div class="card-image">
      <figure class="image">
        <img src={book.image} alt="Book cover">
      </figure>
    </div>
    <div class="card-content">
      <p class="title is-5">{book.title}</p>
      <p class="subtitle is-6 has-text-danger-dark">{book.price}</p>
      <a href={book.url}  target="_blank" class="button is-primary is-fullwidth">Buy</a>
    </div>
  </div>
</div>

<style>

  @media screen and (min-width: 769px) {
    .is-two-ninth {
      flex: none;
      width: 22.22%;
    }
  }

</style>
