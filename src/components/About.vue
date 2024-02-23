<template>
  <section class="about section" id="about">
    <div class="about__container container grid">
      <div class="about__data">
        <h3 class="section__subtitle">Minha <span>Intro</span></h3>

        <h2 class="section__title">Sobre  Mim</h2>

        <p class="about__description">
          Como desenvolvedor front-end, minha paixão é criar interfaces de usuário cativantes e
          funcionais. Com habilidades em sass, javascript, VueJS, VueEX entre outros,
          transformo designs em experiências interativas e responsivas. Trabalho em estreita
          colaboração com designers e desenvolvedores back-end para garantir uma integração perfeita
          entre o visual e a funcionalidade dos aplicativos web. Além disso, estou
          sempre atualizado com as mais recentes tecnologias e tendências do setor para oferecer
          soluções inovadoras que proporcionem uma experiência de usuário excepcional.
        </p>

        <a href="#contact" class="button">contate-me</a>
      </div>

      <div class="about__image">
        <svg
          class="about__blob"
          viewBox="0 0 550 592"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <mask id="maskBorder" mask-type="alpha">
            <path
              d="M263 48.1782C270.426 43.891 279.574 43.891 287 48.1782L501.157 
                        171.822C508.583 176.109 513.157 184.032 513.157 192.606V439.894C513.157 
                        448.468 508.583 456.391 501.157 460.678L287 584.322C279.574 588.609 
                        270.426 588.609 263 584.322L48.843 460.678C41.4174 456.391 36.843 448.468 36.843 
                        439.894V192.606C36.843 184.032 41.4174 176.109 48.843 171.822L263 48.1782Z"
              fill="black"
            />
          </mask>
          <g mask="url(#maskBorder)">
            <rect x="37" width="476" height="630" fill="url(#pattern2)" />

            <path
              d="M285 51.6423L499.157 175.286C505.345 178.859 509.157 185.461 509.157 
                        192.606V439.894C509.157 447.039 505.345 453.641 499.157 457.214L285 
                        580.858C278.812 584.43 271.188 584.43 265 580.858L50.843 457.214C44.655 453.641 
                        40.843 447.039 40.843 439.894V192.606C40.843 185.461 44.655 178.859 50.843 
                        175.286L265 51.6423C271.188 48.0697 278.812 48.0696 285 51.6423Z"
              stroke="black"
              stroke-width="10"
            />
          </g>

          <rect x="37" width="476" height="300" fill="url(#pattern3)" />

          <defs>
            <pattern id="pattern2" patternContentUnits="objectBoundingBox" width="1" height="1">
              <use href="#imageBorder" transform="matrix(0.00143057 0 0 0.00108108 0.0404062 0)" />
            </pattern>

            <pattern id="pattern3" patternContentUnits="objectBoundingBox" width="1" height="1">
              <use href="#imageBorder" transform="matrix(0.00143057 0 0 0.00226984 0.0404062 0)" />
            </pattern>

            <image
              class="about__img"
              id="imageBorder"
              width="640"
              height="940"
              href="../assets/img/foto-1.png"
            />
          </defs>
        </svg>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'About',
  data() {
    return {}
  }
}
</script>

<style lang="scss">
.about__container {
  row-gap: 2.5rem;
  @media screen and (min-width: 576px) {
    grid-template-columns: 360px;
    justify-content: center;
  }

  @media screen and (min-width: 768px) {
    grid-template-columns: repeat(2, 1fr);
    align-items: center;
  }

  @media screen and (min-width: 1152px) {
    grid-template-columns: 550px 460px;
    column-gap: 4.5rem;
    padding-bottom: 1rem;
  }

  .about__data {
    text-align: center;

    @media screen and (min-width: 768px) {
      text-align: initial;
      order: 1;

      .section__subtitle, .section__title{
        text-align: initial;
      }
    }

    .about__description {
      margin-bottom: 2rem;
      @media screen and (min-width: 768px) {
        font-size: 0.85rem;
      }
      @media screen and (min-width: 1023px) {
        font-size: 1rem;
      }
      @media screen and (min-width: 1152px) {
        margin-bottom: 3rem;
      }
    }
  }

  .about__image {
    justify-self: center;

    .about__blob {
      width: 320px;

      @media screen and (min-width: 768px) {
        width: 400px;
      }

      @media screen and (min-width: 1152px) {
        width: 550px;
      }
  
      path {
        stroke: var(--first-color);
      }
    }
  }
}
</style>
