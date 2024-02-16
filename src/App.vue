<template>
  <div>
    <HeaderVue />
    <router-view></router-view>
  </div>
</template>

<script>
import HeaderVue from './components/Header.vue'
import Home from './components/Home.vue'

export default {
  components: {
    HeaderVue,
    Home
  }
}
</script>

<style lang="scss">
.button {
  display: inline-block;
  background-color: var(--first-color);
  padding: 1rem 1.75rem;
  border-radius: 0.5rem;
  color: var(--title-color);
  font-weight: var(--font-medium);
  transition: box-shaow 0.4s;

  &:hover {
    box-shadow: 0 8px 24px hsla(var(--hue), 100%, 40%, 0.2);
  }
}
</style>
