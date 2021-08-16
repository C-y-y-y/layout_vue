<template>
  <div id="app">
    <component :is="layout">
      <router-view/>
    </component>
  </div>
</template>

<script>
import Main from '@/views/Main'
export default {
  computed: {
    layout () {
      console.log(this.$route.meta)
      return 'main'
    }
  },
  components: {
    Main
  }
}
</script>

<style lang="scss">
@import '~materialize-css/dist/css/materialize.min.css';
@import 'assets/index.css';
</style>
