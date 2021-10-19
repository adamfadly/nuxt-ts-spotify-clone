<template>
  <div class="bg-black h-screen w-full flex">
    <LeftNavbar />
    <MainView />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import LeftNavbar from '~/components/Navbar/LeftNavbar.vue'
import MainView from '~/components/MainView/MainView.vue'

export default Vue.extend({
  components: { LeftNavbar, MainView },
})
</script>

<style scoped></style>
