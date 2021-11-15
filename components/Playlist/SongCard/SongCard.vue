<template>
  <div>
    <div v-for="(song, index) in 5" :key="index" class="">
      <div
        class="wrap-card w-52 h-64 bg-gray flex flex-col p-4 rounded-sm"
        :class="isHovering ? 'bg-opacity-100' : 'bg-opacity-25'"
        @mouseover="onHover"
        @mouseout="onHover"
      >
        <div class="mb-2 relative">
          <div class="bg-black w-44 h-44 rounded-sm relative"></div>
          <play
            :class="isHovering ? 'opacity-100' : 'opacity-0'"
            class="absolute bottom-2 right-2 bg-green rounded-full w-10 h-10"
          ></play>
        </div>
        <div class="flex flex-col text-left">
          <p class="text-base font-medium">Title</p>
          <p class="font-medium text-gray-dark text-sm">artist</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Play from '~/assets/icon/HeroIcons/Play.vue'

export default Vue.extend({
  components: { Play },
  props: {
    category: {
      type: String,
      default: '',
    },
    items: {
      type: Number,
      default: null,
    },
  },
  data() {
    return {
      isHovering: false,
    }
  },
  methods: {
    onHover(): void {
      console.log('yolo')
      this.isHovering = !this.isHovering
    },
  },
})
</script>
