<template>
  <div class="bg-black h-screen w-full">
    <LeftNavbar />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import LeftNavbar from '~/components/Navbar/LeftNavbar.vue'

export default Vue.extend({
  components: { LeftNavbar },
})
</script>

<style scoped></style>
