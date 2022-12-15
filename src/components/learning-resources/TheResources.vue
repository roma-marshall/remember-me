<template>
  <base-card>
    <base-button @click="selectedTab('stored-resources')">Stored Resources</base-button>
    <base-button @click="selectedTab('add-resource')">Add Resource</base-button>
  </base-card>
  <component :is="selectedTab"></component>
</template>

<script>
import StoredResources from "./StoredResources";
import AddResource from "./AddResource";

export default {
  components: {
    StoredResources,
    AddResource
  },
  data() {
    return {
      selectedTab: 'stored-resources',
      storedResources: [
        {
          id: 'official-guide',
          title: 'Official Guide',
          description: 'The official Vue 3 documentation',
          link: 'https://vuejs.org'
        },
        {
          id: 'google',
          title: 'Google Inc.',
          description: 'Learn to google',
          link: 'https://google.com'
        }
      ]
    };
  },
  methods: {
    setSelectedTabs(tab) {
      this.selectedTab = tab;
    }
  }
}
</script>

<style scoped>

</style>