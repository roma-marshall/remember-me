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
export default {
  props: ['resources']
}
</script>

<style scoped>

</style>