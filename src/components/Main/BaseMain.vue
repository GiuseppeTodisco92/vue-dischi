<template>
  <main>
      <album-section/>
  </main>
</template>

<script>
import AlbumSection from '../Section/AlbumSection.vue'
export default {
  components: { AlbumSection },
    name: "BaseMain"
}
</script>

<style lang="scss" scoped>
main{
    background-color: var(--secondary-color);
}
</style>