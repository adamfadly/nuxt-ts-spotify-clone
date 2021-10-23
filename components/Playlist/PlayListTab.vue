<template>
  <div class="">
    <div class="mt-2 flex h-20" @mouseover="onHover" @mouseout="onHover">
      <div class="rounded-tl-sm rounded-bl-sm">
        <div class="w-20 h-20 rounded-tl-sm rounded-bl-sm bg-purple-900" />
      </div>
      <div
        class="
          flex
          w-64
          items-center
          justify-between
          bg-gray bg-opacity-50
          hover:bg-opacity-100
          transition-2
          rounded-tr-sm rounded-br-sm
          px-5
        "
      >
        <div class="">weekly</div>
        <div class="shadow-2xl">
          <play
            :class="isHovering ? 'opacity-100' : 'opacity-0'"
            class="hover:opacity-100 w-10 h-10 bg-green rounded-full opacity-0"
          ></play>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Play from '~/assets/icon/HeroIcons/Play.vue'

export default Vue.extend({
  components: {
    Play,
  },
  data() {
    return {
      isHovering: false,
    }
  },
  methods: {
    onHover(): void {
      this.isHovering = !this.isHovering
    },
  },
})
</script>

<style scoped></style>
