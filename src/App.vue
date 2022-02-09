<template>
  <div id="app">
    <Header />
    <Main />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'


export default {
  name: 'App',
  components: {
    Header,
    Main
  }
}
</script>

<style lang="scss">
@import './assets/style/global.scss';
/*BOOTSTRAP ICONS*/
@import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.8.1/font/bootstrap-icons.css");

</style>
