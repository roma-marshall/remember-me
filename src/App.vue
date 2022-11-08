<template>
  <stored-resources></stored-resources>
</template>

<script>
import StoredResources from "@/components/learning-resources/StoredResources";

export default {
  components: {
    StoredResources
  },
  data() {
    return {
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
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}
</style>
