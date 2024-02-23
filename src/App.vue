<template>
  <div>
    <HeaderVue />
    <div id="cursor"></div>
    <router-view></router-view>
  </div>
</template>

<script>
import HeaderVue from './components/Header.vue'

export default {
  components: {
    HeaderVue,
  },
}
</script>

<style lang="scss">

  ::-webkit-scrollbar {
    width: .6rem;
    border-radius: .5rem;
    background-color: hsla(228, 12%, 25%);
  }  

  ::-webkit-scrollbar-thumb {
    background-color: hsla(228, 8%, 35%);
    border-radius: .5rem;

    &:hover {
      background-color: hsla(228, 8%, 45%);
    }
  }

  .active-link {
    color: var(--first-color);
  }

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

  @media screen and (max-width: 320px) {
    .container {
      margin-inline: 1rem;
    }
  }

  @media screen and (min-width: 1023px) {
    .section {
      padding-block: 7rem 2rem;

      &__subtitle {
        font-size: var(--normal-font-size);
      }
    }
  }

  @media screen and (min-width: 1152px) {
    .container {
      margin-inline: auto;
    }
  }

</style>
