<template>
  <dialog open>
    <header>
      <slot>
        <h2> {{ title }}</h2>
      </slot>
    </header>
  </dialog>
</template>

<script>
export default {
  props: ['title']
}
</script>