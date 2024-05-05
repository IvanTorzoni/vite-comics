<script>
export default {
  props: {
    comicImage: String,
    comicSeries: String,
  },
};
</script>

<template>
  <div class="card">
    <img :src="comicImage" alt="" />
    <h4>{{ comicSeries }}</h4>
  </div>
</template>

<style scoped lang="scss">
.card {
  padding: 1rem;
  text-align: center;

  img {
    max-width: 100%;
  }
}
</style>