<template>
    <div class="app-container">
      <header class="header-slice">
        <HeaderCompo class="layout-center"/>
      </header>

      <main>
        <mainCompo class="layout-center"></mainCompo>
      </main>

      <footer>
        <slot name="footer"></slot>
      </footer>
    </div>
</template>

<script>
import HeaderCompo from './Header'
import mainCompo from './MainCenter'
export default {
  name: "index.vue",
  components: {
    HeaderCompo,
    mainCompo,
  }
}
</script>

<style scoped lang="scss">
.app-container {
  width: 100%;
}
.header-slice {
  width: 100%;
  background-color: #eee;
  height: 50px;
}
</style>
