<template>
  <div>
    <p>{{ movies }}</p>
    >
  </div>
</template>

<script>
export default {
  data() {
    return {
      movies: []
    }
  },
  mounted() {
    fetch('https://omdbapi.com/?apikey=56edad45&t=%27Harry%20Potter%27')
      .then((res) => res.json())
      .then((data) => (this.movies = data))
      .catch((err) => console.log(err.message))
  }
}
</script>

<style></style>
