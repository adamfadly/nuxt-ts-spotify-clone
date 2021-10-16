<template>
  <div class="bg-black w-full h-screen">
    <div class="flex flex-col items-center m-auto py-32">
      <img
        class="w-1/2 h-full"
        src="../../assets/logo/Spotify_Logo_Green.png"
        alt=""
      />
      <p
        class="
          mt-20
          text-green
          font-semibold
          text-4xl
          bg-white
          py-4
          px-6
          rounded-full
          hover:bg-green hover:text-white
          transition-all
        "
        @click="goToHome"
      >
        Login
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  methods: {
    goToHome(): void {
      this.$router.push('/home')
    },
  },
})
</script>

<style scoped></style>
