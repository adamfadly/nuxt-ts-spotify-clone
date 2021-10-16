<template>
  <div>
    <Home />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Home from '~/views/Home/Home.vue'

export default Vue.extend({
  components: {
    Home,
  },
})
</script>

<style scoped></style>
