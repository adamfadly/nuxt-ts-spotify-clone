<template>
  <div>
    <Login />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Login from '~/views/Login/Login.vue'

export default Vue.extend({
  components: {
    Login,
  },
  data() {
    return {
      name: 'Adam Fadly',
    }
  },
})
</script>
