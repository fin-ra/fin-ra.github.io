<template>
  <div class="section-wrapper">
    <h1>{{ title }}</h1>
    <img :src="schemeImgSrc" :alt="subtitle" />
    <p>{{ subtitle }} появится здесь позже</p>
  </div>
</template>

<script>
export default {
  name: 'Architecture',
  props: {
    title: String,
    subtitle: String,
    schemeImgSrc: String
  }
}
</script>

<style scoped>

</style>
