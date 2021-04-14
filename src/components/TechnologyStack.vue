<template>
  <div class="section-wrapper">
    <h1>{{ title }}</h1>

    <ul class="cards-list">
      <li v-for="tech in technologiesUsed"
        :key="tech.name"
        class="card">
        {{ tech.name }} 
        <span class="version">{{ tech.version }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'TechnologyStack',
  props: {
    title: String,
    technologiesUsed: Array
  }
}
</script>

<style scoped>
.card {
  margin: 20px 0;
  padding: 0;
}

.card .version {
  padding: 0 10px;
  color: #ddd;
}
</style>
