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
  },
  mounted() {
    this.animationScroll();
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
  </main>
</template>
