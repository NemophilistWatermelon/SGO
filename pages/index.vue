<template>
  <AppMain />
</template>

<script lang="ts">
import Vue from 'vue'
import AppMain from '~/components/BaseLayout/main.vue'

export default Vue.extend({
  name: 'IndexPage',
  components: {
    AppMain
  }
})
</script>
