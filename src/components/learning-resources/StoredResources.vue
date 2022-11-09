<template>
  <ul>
    <learning-resource
        v-for="res in resources"
        :key="res.id"
        :title="res.title"
        :description="res.description"
        :link="res.link"
    >
    </learning-resource>
  </ul>
</template>

<script>
import LearningResource from "./LearningResource";

export default {
  props: ['resources'],
  components: {
    LearningResource
  }
}
</script>

<style scoped>

</style>