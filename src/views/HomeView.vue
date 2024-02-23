<script setup>
import Start from '@/components/Start.vue';
import About from '@/components/About.vue';
import Skills from '@/components/Skills.vue';
import Services from '@/components/Services.vue';
import Projects from '@/components/Projects.vue';
import Contact from '@/components/Contact.vue';
import Footer from '@/components/Footer.vue';
import ScrollUp from '@/components/ScrollUp.vue';

</script>

<script>
export default {
  name: 'HomeView',
  methods: {
    animationScroll() {
      const sr = ScrollReveal({
        origin: 'top',
        distance: '60px',
        duration: 2500,
        delay: 400,
      });

      sr.reveal(`.home__data, .home__social, .contact__container, .footer__container`);
      sr.reveal(`.home__image`, {origin: 'bottom' });
      sr.reveal(`.about__data, .skills__data`, {origin: 'left' });
      sr.reveal(`.about__image, .skills__content`, {origin: 'right' });
      sr.reveal(`.services__card, .projects__card`, {interval: 100 })
    },
    animaCursor() {
      const circle = document.getElementById('circle');

      document.addEventListener('mousemove', (e) => {
        const x = e.pageX;
        const y = e.pageY;

        circle.style.left = x + 'px';
        circle.style.top = y + 'px';
      });

      document.addEventListener('scroll', (e) => {
        const x = e.pageX;
        const y = e.pageY;

        circle.style.left = x + 'px';
        circle.style.top = y + 'px';
      });
    }
  },
  mounted() {
    this.animationScroll();
    this.animaCursor()
  }
}
</script>

<template>
  <main class="main">
    <Start />
    <About />
    <Skills />
    <Services />
    <Projects />
    <Contact />
    <Footer />
    <ScrollUp />

    <span class="circle" id="circle"></span>
  </main>
</template>

<style lang="scss">
.circle {
  z-index: 999;
  width: 20px;
  height: 20px;
  background: var(--first-color);
  border-radius: 50%;
  pointer-events: none;
  position: absolute;
  box-shadow: 0 0 20px var(--first-color)
  0 0 60px var(--first-color)
  0 0 100px var(--first-color);
  animation: colors 5s infinite;

  &:before {
    content: '';
    position: absolute;
    background: var(--first-color-alt);
    width: 50px;
    height: 50px;
    opacity: 0.2;
    transform: translate(-30%, -30%);
    border-radius: 50%;
  }
}

@keyframes colors {
 0% {
  filter: hue-rotate(0deg);
 } 
 100% {
  filter: hue-rotate(360deg);
 }
}
</style>
