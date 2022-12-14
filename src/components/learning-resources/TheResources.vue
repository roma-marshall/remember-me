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
      selectedTab: 'stored-resources';
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