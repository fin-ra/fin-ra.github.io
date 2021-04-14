<template>
  <div class="section-wrapper">
    <h1>{{ title }}</h1>

    <ul class="cards-list">
      <PersonCard v-for="person in persons"
        :key="person.fullName"
        :fullName="person.fullName"
        :position="person.position"
        :social="person.social">
      </PersonCard>
    </ul>
  </div>
</template>

<script>
import PersonCard from './PersonCard.vue'

export default {
  name: 'TeamMembers',
  components: {
    PersonCard
  },
  props: {
    title: String,
    persons: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
