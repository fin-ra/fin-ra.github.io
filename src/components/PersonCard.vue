<template>
  <li class="card">
    <h3 class="card-header">{{ fullName }}</h3>
    <div class="card-body">{{ position }}</div>
    <div v-if="social" class="icons-wrapper">
      <a v-if="social.github" :href="'https://github.com/' + social.github"
        :title="'@' + social.github"
        target="_blank">
        <i class="octoicon"></i>
      </a>
    </div>
  </li>
</template>

<script>
export default {
  name: 'PersonCard',
  props: {
    fullName: String,
    position: String,
    social: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  margin: 50px 0;
  padding: 0;
}

.card .card-header {
  margin: 12px 0;
}

.card .card-body {
  margin: 12px 0;
}

.icons-wrapper {
  height: 20px;
  margin: 20px 0;
}

.octoicon {
  background-image: url('/assets/img/octo_icon.svg');
  background-position: center;
  position: absolute;
  width: 20px;
  height: 20px;
  cursor: pointer;
}
</style>
