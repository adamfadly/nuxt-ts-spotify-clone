vbase
<template>
  <div class="flex flex-col w-1/6 bg-black h-screen">
    <img
      class="w-full h-22 py-3 px-6"
      src="../../assets/logo/Spotify_Logo_White.png"
      alt=""
    />
    <div class="flex flex-col py-1 px-6">
      <nuxt-link to="/home">
        <div class="flex items-center">
          <HomeIcon class="w-6 h-6" />
          <p class="text-lg font-normal py-2 pl-3">Home</p>
        </div>
      </nuxt-link>
      <nuxt-link to="/library">
        <div class="flex items-center">
          <LibraryIcon class="w-6 h-6" />
          <p class="text-lg font-normal py-2 pl-3">Library</p>
        </div>
      </nuxt-link>
      <nuxt-link to="/search">
        <div class="flex items-center">
          <SearchIcon class="w-6 h-6" />
          <p class="text-lg font-normal py-2 pl-3">Search</p>
        </div>
      </nuxt-link>
    </div>
    <div class="flex flex-col pt-4 pb-1 px-6">
      <div class="flex items-center">
        <PlusIcon class="text-black text-xs bg-white w-6 h-6 p-1" />
        <p class="text-lg font-normal py-2 pl-3">Create Playlist</p>
      </div>
      <div class="flex items-center">
        <LoveIcon
          class="text-xs p-1 w-6 h-6 bg-gradient-to-r from-blue-700 to-blue-300"
        />
        <p class="text-lg font-normal py-2 pl-3">Liked Songs</p>
      </div>
      <div class="flex items-center">
        <PodcastIcon
          class="text-green w-6 h-6 bg-green bg-opacity-50 rounded-sm p-1"
        />
        <p class="text-lg font-normal py-2 pl-3">Your Episode</p>
      </div>
    </div>
    <hr class="bg-gray-300 mx-6" />
    <div class="py-1 overflow-y-auto px-6">
      <p v-for="n in 50" :key="n" class="text-sm py-1">My Playlist</p>
    </div>
    <div class="flex items-center px-6 py-5 h-10 pb-10">
      <ArrowDownIcon class="w-6 h-6" />
      <p class="text-lg font-normal py-2 pl-3">Install App</p>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import HomeIcon from '~/assets/icon/HeroIcons/HomeIcon.vue'
import LibraryIcon from '~/assets/icon/HeroIcons/LibraryIcon.vue'
import SearchIcon from '~/assets/icon/HeroIcons/SearchIcon.vue'
import PlusIcon from '~/assets/icon/HeroIcons/PlusIcon.vue'
import LoveIcon from '~/assets/icon/HeroIcons/LoveIcon.vue'
import PodcastIcon from '~/assets/icon/HeroIcons/PodcastIcon.vue'
import ArrowDownIcon from '~/assets/icon/HeroIcons/ArrowDownIcon.vue'

export default Vue.extend({
  components: {
    HomeIcon,
    LibraryIcon,
    SearchIcon,
    PlusIcon,
    LoveIcon,
    PodcastIcon,
    ArrowDownIcon,
  },
})
</script>

<style scoped></style>
