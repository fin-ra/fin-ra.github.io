<template>
  <div class="section-wrapper">
    <div class="logo-wrapper">
      <img src="/assets/img/logo_dark.svg" />
    </div>
    <p class="main-text">
      {{ title }} <br />
      {{ subtitle }}
    </p>
  </div>
</template>

<script>
export default {
  name: 'AppHeader',
  props: {
    title: String,
    subtitle: String
  }
}
</script>

<style scoped>
.logo-wrapper {
  margin-bottom: 5%;
  height: 200px;
}
  .logo-wrapper img {
    height: 100%;
  }

.main-text {
  font-size: 2.5em;
}
</style>
