<template>
  <div class="bg-black container">
    <top-navbar></top-navbar>
    <div class="px-5">
      <p class="text-4xl font-bold py-5">Good Morning</p>
      <div class="flex flex-wrap justify-between">
        <div v-for="n in 6" :key="n">
          <play-list-tab></play-list-tab>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import TopNavbar from '~/components/Navbar/TopNavbar.vue'
import PlayListTab from '~/components/Playlist/PlayListTab.vue'

export default Vue.extend({
  components: {
    TopNavbar,
    PlayListTab,
  },
  layout: 'mainView',
})
</script>

<style scoped></style>
