<template>
  <div class="bg-black container h-screen">
    <top-navbar></top-navbar>
    <div class="px-5 overflow-y-auto h-screen">
      <!-- tab list -->
      <div>
        <p class="text-4xl font-bold py-5">Good Morning</p>
        <div class="flex flex-wrap justify-between">
          <div v-for="(song, index) in 6" :key="index">
            <play-list-tab></play-list-tab>
          </div>
        </div>
      </div>
      <!-- song card test -->
      <div class="">
        <p class="text-4xl font-bold py-5">Episodes for you</p>
        <song-card class="flex justify-between" :items="5"></song-card>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import TopNavbar from '~/components/Navbar/TopNavbar.vue'
import PlayListTab from '~/components/Playlist/PlayListTab.vue'
import SongCard from '~/components/Playlist/SongCard/SongCard.vue'

export default Vue.extend({
  components: {
    TopNavbar,
    PlayListTab,
    SongCard,
  },
  layout: 'mainView',
})
</script>

<style scoped></style>
