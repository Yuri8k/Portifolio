<template>
  <section class="home section" id="home">
    <div class="snow"></div>
    <div class="home__container container grid">
      <div class="home__content">
        <div class="home__data">
          <h3 class="home__subtitle">Olá, <span>Eu sou</span></h3>

          <h1 class="home__title">Yuri Oliveira</h1>

          <h3 class="home__educatiion">Front-end Developer</h3>

          <h3 class="home__description">
            Desenvolvedor front-end, criação de interfaces de usuário cativantes, funcionais e responsivas, utlizando sass, javascript, VueJS, entre outros.
          </h3>

          <a href="#contact" class="button">Vamos conversar</a>
        </div>

        <div class="home__social">
          <a href="https://github.com/Yuri8k" target="_blank" class="home__social-link">
            <i class="ri-github-fill"></i>
          </a>
          <a
            href="https://www.linkedin.com/in/yuri-oliveira-671b70213/"
            target="_blank"
            class="home__social-link"
          >
            <i class="ri-linkedin-box-fill"></i>
          </a>
        </div>
      </div>

      <div class="home__image">
        <svg class="home__blob" viewBox="0 0 550 591" xmlns="http://www.w3.org/2000/svg">
          <mask id="maskBlob" mask-type="alpha">
            <path
              d="M263 47.1782C270.426 42.891 279.574 42.891 287 47.1782L501.157 
      170.822C508.583 175.109 513.157 183.032 513.157 191.606V438.894C513.157 
      447.468 508.583 455.391 501.157 459.678L287 583.322C279.574 587.609 270.426 
      587.609 263 583.322L48.843 459.678C41.4174 455.391 36.843 447.468 36.843 
      438.894V191.606C36.843 183.032 41.4174 175.109 48.843 170.822L263 47.1782Z"
            />
          </mask>
          <g mask="url(#maskBlob)">
            <path
              d="M263 47.1782C270.426 42.891 279.574 42.891 287 47.1782L501.157 
      170.822C508.583 175.109 513.157 183.032 513.157 191.606V438.894C513.157 
      447.468 508.583 455.391 501.157 459.678L287 583.322C279.574 587.609 270.426 
      587.609 263 583.322L48.843 459.678C41.4174 455.391 36.843 447.468 36.843 
      438.894V191.606C36.843 183.032 41.4174 175.109 48.843 170.822L263 47.1782Z"
            />

            <rect x="37" width="476" height="630" fill="url(#pattern0)" />
          </g>

          <rect x="37" width="476" height="300" fill="url(#pattern1)" />

          <defs>
            <pattern id="pattern0" patternContentUnits="objectBoundingBox" width="1" height="1">
              <use href="#imageBlob" transform="matrix(0.00143057 0 0 0.00108108 0.0404062 0)" />
            </pattern>

            <pattern id="pattern1" patternContentUnits="objectBoundingBox" width="1" height="1">
              <use href="#imageBlob" transform="matrix(0.00143057 0 0 0.00226984 0.0404062 0)" />
            </pattern>

            <!-- Insert your profile (recommended size: 640 x 940) -->
            <image
              class="home__img"
              id="imageBlob"
              width="640"
              height="925"
              href="../assets/img/Foto-portfolio.png"
            />
          </defs>
        </svg>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {}
  }
}
</script>

<style lang="scss">
main {
  .home {
    background: var(--container-color);
    position: relative;
    overflow: hidden;

    .snow {
      &::after, &::before {
        content: '';
        position: absolute;
        top: -650px;
        left: 0;
        right: 0;
        bottom: 0;
        background-image: radial-gradient(4px 4px at 100px 50px, #fff, transparent),
        radial-gradient(6px 6px at 200px 150px, #fff, transparent),
        radial-gradient(3px 3px at 300px 250px, #fff, transparent),
        radial-gradient(4px 4px at 400px 350px, #fff, transparent),
        radial-gradient(6px 6px at 500px 100px, #fff, transparent),
        radial-gradient(3px 3px at 50px 200px, #fff, transparent),
        radial-gradient(4px 4px at 150px 300px, #fff, transparent),
        radial-gradient(6px 6px at 250px 400px, #fff, transparent),
        radial-gradient(3px 3px at 350px 500px, #fff, transparent);
        background-size: 650px 650px;
        animation: snowAnimation 8s linear;
        animation-iteration-count: infinite;
      }

      &::after {
        margin-left: -250px;
        opacity: 0.7;
        filter: blur(1px);
        animation-duration: 12s;
      }
      &::before {
        margin-left: -350px;
        opacity: 1;
        animation-duration: 15s;
      }

      @keyframes snowAnimation {
        from {
          transform: translateY(0);
        }
        to {
          transform: translateY(650px);
        }
      }
    }

    &__container {
      padding-top: 2rem;
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
        grid-template-columns: 455px 550px;
        column-gap: 7rem;
        padding-block: 2rem 3rem;
      }

      .home__content {
        display: grid;
        row-gap: 2rem;

        @media screen and (min-width: 1152px) {
          row-gap: 4.5rem;
        }

        .home__data {
          text-align: center;

          @media screen and (min-width: 768px) {
            text-align: initial;
          }

          .home__subtitle,
          .home__educatiion {
            font-size: var(--brigger-font-size);
          }

          .home__subtitle span,
          .home__title {
            color: var(--first-color);
          }

          .home__title {
            font-size: var(--biggest-font-size);
            font-weight: var(--font-semi-bold);
          }

          .home__description {
            margin-block: 1rem 1.5rem;

            @media screen and (min-width: 1023px) {
              margin-block: 1.5rem 2.5rem;
            }
          }
        }

        .home__social {
          display: flex;
          justify-content: center;
          column-gap: 1.25rem;

          @media screen and (min-width: 768px) {
            justify-content: initial;
          }

          @media screen and (min-width: 1023px) {
            column-gap: 1.5rem;
          }

          &-link {
            display: flex;
            background-color: var(--first-color-alt);
            padding: 0.5rem;
            color: var(--title-color);
            font-size: 1.5rem;
            clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
            transition: transform 0.4s;

            &:hover {
              transform: translateY(-0.25rem);
            }
          }
        }
      }

      .home__image {
        justify-self: center;

        .home__blob {
          width: 320px;
          fill: var(--first-color);
          filter: drop-shadow(0 12px 12px hsla(var(--hue), 100%, 40%, 0.2));

          @media screen and (min-width: 768px) {
            width: 400px;
          }

          @media screen and (min-width: 1152px) {
            width: 550px;
          }
        }
      }
    }
  }
}
</style>
