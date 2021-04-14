<template>
  <footer>
    &copy; {{ foundedInYear }}–{{ currentYear }},
    "{{ title }}"
  </footer>
</template>

<script>
export default {
  name: 'AppFooter',
  props: {
    foundedInYear: Number,
    title: String
  },
  computed: {
    currentYear () {
      return new Date().getFullYear()
    }
  }
}
</script>

<style scoped>
footer {
  font-size: 12px;
  margin-top: 100px;
  padding: 30px 0;
}
</style>
