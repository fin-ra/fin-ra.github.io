<template>
  <div class="content-wrapper">

    <AppHeader
      :title="title"
      :subtitle="subtitle">
    </AppHeader>

    <TeamMembers
      :title="ourAmazingTeam.title"
      :persons="ourAmazingTeam.members">
    </TeamMembers>

    <Architecture
      :title="architecture.title"
      :subtitle="architecture.subtitle"
      :schemeImgSrc="architecture.schemeImgSrc">
    </Architecture>

    <TechnologyStack
      :title="technologyStack.title"
      :technologiesUsed="technologyStack.technologies">
    </TechnologyStack>

    <AppFooter
      :title="company.name"
      :foundedInYear="company.foundedInYear">
    </AppFooter>

  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import TeamMembers from './components/TeamMembers.vue'
import Architecture from './components/Architecture.vue'
import TechnologyStack from './components/TechnologyStack.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    TeamMembers,
    Architecture,
    TechnologyStack,
    AppFooter
  },
  data () {
    return {
      title: 'Разработка платформы обучения',
      subtitle: 'на курсах "Портфельных инвестиций"',
      company: {
        name: 'Школа Безопасных Инвестиций',
        foundedInYear: 2016
      },
      ourAmazingTeam: {
        title: 'Команда',
        members: [
          {
            fullName: 'Виталий Вербицкий',
            position: 'Владелец продукта, эксперт в предметной области'
          },
          {
            fullName: 'Вячеслав Симонов',
            position: 'Менеджер проекта и продукта'
          },
          {
            fullName: "Владимир Синявский",
            position: "Руководитель группы разработки, системный архитектор, ведущий фуллстек-разработчик",
            social: { github: "svasorcery" }
          },
          {
            fullName: "Алексей Рогулёв",
            position: "Фронтенд-разработчик",
            social: { github: "rogulev" }
          },
          {
            fullName: "Евгений Козубов",
            position: "UX/UI дизайнер"
          }
        ]
      },
      architecture: {
        title: 'Архитектура',
        subtitle: 'Схема архитектуры системы',
        schemeImgSrc: ''
      }, 
      technologyStack: {
        title: 'Стек технологий',
        technologies: [
          { name: '.NET', version: '5 / Core 3' },
          { name: 'PostrgreSQL', version: '' },
          { name: 'MongoDB', version: '' },
          { name: 'SignalR', version: '' },
          { name: 'Angular', version: '11+' },
          { name: 'RxJs', version: '' },
          { name: 'DigitalOcean', version: '' }
        ]
      }
    }
  }
}
</script>

<style>
body {
  background-color: #363645;
}

#app {
  font-family: 'Roboto', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #ffffff;
  margin: 0 20%;
}

h1 {
  font-size: 2em;
  font-weight: 600;
}

p {
  margin: 5px 0;
}

.section-wrapper {
  margin-top: 100px;
}

.cards-list {
  list-style-type: none;
  padding: 0;
}
</style>
