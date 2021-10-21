<template>
  <div>
    <div class="py-3 bg-purple-900">
      <div class="flex items-center justify-between px-4">
        <div class="flex items-center">
          <chevron-left
            class="bg-black opacity-100 rounded-full mx-1"
          ></chevron-left>
          <chevron-right
            class="bg-black bg-opacity-100 rounded-full mx-1"
          ></chevron-right>
        </div>
        <div @click="onUserAccount">
          <div
            class="
              flex
              items-center
              justify-between
              bg-black
              p-1
              rounded-full
              cursor-pointer
            "
          >
            <div class="pr-1">
              <img
                class="h-7 w-7 rounded-full"
                src="https://images.unsplash.com/photo-1491528323818-fdd1faba62cc?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                alt=""
              />
            </div>
            <div class="text-xs font-medium px-2">Mocha Adam Fadly</div>
            <chevron-right
              :class="dropDown ? 'transform rotate-90' : 'transform -rotate-90'"
            >
            </chevron-right>
          </div>
          <div
            v-if="dropDown"
            class="
              bg-black
              absolute
              mt-1
              flex flex-col
              w-48
              p-2
              rounded-md
              cursor-pointer
            "
          >
            <div class="flex justify-between">
              <div>account</div>
              <log-out></log-out>
            </div>
            <div class="">profile</div>
            <div class="">logout</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import ChevronLeft from '~/assets/icon/HeroIcons/ChevronLeft.vue'
import ChevronRight from '~/assets/icon/HeroIcons/ChevronRight.vue'
import LogOut from '~/assets/icon/HeroIcons/LogOut.vue'

export default Vue.extend({
  components: {
    ChevronLeft,
    ChevronRight,
    LogOut,
  },
  data() {
    return {
      dropDown: true,
    }
  },
  methods: {
    onUserAccount() {
      this.dropDown = !this.dropDown
    },
  },
})
</script>
