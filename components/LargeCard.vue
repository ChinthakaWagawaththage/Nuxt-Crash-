<template>
  <NuxtLink :to="`/products/${ card.id }`" class="card">
    <img :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)" alt="cars" class="image">
    <h3 class="header">
      {{ card.title }}
    </h3>
    <h4 class="snippet">
      {{ card.snippet }}
    </h4>
  </NuxtLink>
</template>

<script>
export default {
  name: 'LargeCard',
  props: ['card']
}
</script>

<style scoped>
.card {
  width: 31.5%;
  height: 25rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
}
.image {
  height: 65%;
  border-radius: 0.5rem;
}
.header {
  font-size: 1.15rem;
  margin-top: 0.4rem;
}
.snippet {
  color: grey
}
</style>
