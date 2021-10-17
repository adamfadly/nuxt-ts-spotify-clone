vbase
<template>
  <div class="flex flex-col w-1/6 bg-red-900 h-screen">
    <img
      class="w-full h-22 py-3 px-6"
      src="../../assets/logo/Spotify_Logo_White.png"
      alt=""
    />
    <div class="flex flex-col py-1 px-6">
      <div class="flex items-center">
        <HomeIcon class="text-white w-6 h-6" />
        <p class="text-white text-lg font-normal py-2 pl-3">Home</p>
      </div>
      <div class="flex items-center">
        <LibraryIcon class="text-white w-6 h-6" />
        <p class="text-white text-lg font-normal py-2 pl-3">Library</p>
      </div>
      <div class="flex items-center">
        <SearchIcon class="text-white w-6 h-6" />
        <p class="text-white text-lg font-normal py-2 pl-3">Search</p>
      </div>
    </div>
    <div class="flex flex-col pt-4 pb-1 px-6">
      <div class="flex items-center">
        <PlusIcon class="text-black text-xs bg-white w-6 h-6 p-1" />
        <p class="text-white text-lg font-normal py-2 pl-3">Create Playlist</p>
      </div>
      <div class="flex items-center">
        <LoveIcon
          class="
            text-white text-xs
            p-1
            w-6
            h-6
            bg-gradient-to-r
            from-blue-700
            to-blue-300
          "
        />
        <p class="text-white text-lg font-normal py-2 pl-3">Liked Songs</p>
      </div>
      <div class="flex items-center">
        <SearchIcon class="text-white w-6 h-6" />
        <p class="text-white text-lg font-normal py-2 pl-3">Search</p>
      </div>
    </div>
    <hr class="bg-gray-300 mx-6" />
    <div class="py-1 overflow-y-auto px-6">
      <p v-for="n in 100" :key="n" class="text-sm text-white py-1">
        My Playlist
      </p>
    </div>
    <div class="flex items-center px-6 py-5 h-10 pb-10">
      <ArrowDownIcon class="text-white w-6 h-6" />
      <p class="text-white text-lg font-normal py-2 pl-3">Install App</p>
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
import ArrowDownIcon from '~/assets/icon/HeroIcons/ArrowDownIcon.vue'

export default Vue.extend({
  components: {
    HomeIcon,
    LibraryIcon,
    SearchIcon,
    PlusIcon,
    LoveIcon,
    ArrowDownIcon,
  },
})
</script>

<style scoped></style>
