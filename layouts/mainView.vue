<template>
  <div class="bg-black h-screen w-full flex">
    <LeftNavbar />
    <Nuxt />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import LeftNavbar from '~/components/Navbar/LeftNavbar.vue'

export default Vue.extend({
  components: {
    LeftNavbar,
  },
})
</script>
