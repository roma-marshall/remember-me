<template>
  <li>
    <div>
      <header>
        <h3>
          <button>Delete</button>
        </h3>
      </header>
    </div>
    <p></p>
    <nav>
      <a href="">View Resource</a>
    </nav>
  </li>
</template>

<script>
export default {
  props: ['title', 'description', 'link']
}
</script>

<style scoped>

</style>