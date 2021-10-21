<template>
  <div class="bg-gray w-full h-screen">
    <top-navbar></top-navbar>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import TopNavbar from '~/components/Navbar/TopNavbar.vue'

export default Vue.extend({
  layout: 'mainView',
  components: {
    TopNavbar,
  },
})
</script>

<style scoped></style>
