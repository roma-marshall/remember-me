<template>
  <base-card>
    <base-button @click="selectedTab('stored-resources')" :mode="storedResButtonMode">Stored Resources</base-button>
    <base-button @click="selectedTab('add-resource')" :mode="addResButtonMode">Add Resource</base-button>
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
  provide() {
    return {
      resources: this.storedResources
    }
  },
  computed: {
    storedResButtonMode() {
      return this.selectedTab === 'stored-resources' ? null : 'flat';
    },
    addResButtonMode() {
      return this.selectedTab === 'add-resource' ? null : 'flat';
    }
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