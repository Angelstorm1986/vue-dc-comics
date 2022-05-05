<template>
  <div id="app">
    <app-header/>
    <app-characters/>
    <app-footer/>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppCharacters from './components/AppCharacters.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppCharacters,
    AppFooter
  }
}
</script>

<style lang="scss" scoped>
  @import './style/variables';
  @import './style/general';
  
</style>
