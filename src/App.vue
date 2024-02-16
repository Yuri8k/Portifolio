<template>
  <div>
    <HeaderVue />
    <router-view></router-view>
  </div>
</template>

<script>
import HeaderVue from './components/Header.vue'
import Home from './components/Home.vue';

export default {
  components: {
    HeaderVue, 
    Home
  }
}
</script>

<style>

</style>