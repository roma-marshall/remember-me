<template>
  <ul>
    <li></li>
  </ul>
</template>

<script>
import LearningResource from './components/LearningResource'

export default {
  components: {
    LearningResource
  },
  data() {
    return {
      storedResources: {
        id: 'official-guide',
        title: 'Official Guide',
        description: 'The official Vue 3 documentation',
        link: 'https://vuejs.org'
      }
    }
  }
}
</script>

<style>

</style>
