<template>
  <div>
    <HeaderVue />
    <router-view></router-view>
  </div>
</template>

<script>
import HeaderVue from './components/Header.vue'

export default {
  components: {
    HeaderVue,
  },
  methods: {
    animationScroll() {

      const sr = ScrollReveal({
        origin: 'top',
        distance: '60px',
        duration: 2000,
        delay: 400,
      });

      sr.reveal(`.home__data, .home__social, .contact__container, .footer__container`);
      sr.reveal(`.home__image`, {origin: 'bottom' });
      sr.reveal(`.about__data, .skills__data`, {origin: 'left' });
      sr.reveal(`.about__image, .skills__content`, {origin: 'right' });
      sr.reveal(`.services__card, .projects__card`, {interval: 100 })
    }
  },
  mounted() {
    this.animationScroll()
  }
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
