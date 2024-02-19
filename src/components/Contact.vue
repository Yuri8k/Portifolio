<template>
  <section class="contact section" id="contact">
    <h3 class="section__subtitle">Get in <span>Touch</span></h3>

    <h2 class="section__title">Contact Me</h2>

    <div class="contact__container container grid">

      <div class="contact__social">
        <a href="https://github.com/Yuri8k" target="_blank" class="contact__social-link">
          <i class="ri-github-fill"></i>
        </a>
        <a
          href="https://www.linkedin.com/in/yuri-oliveira-671b70213/"
          target="_blank"
          class="contact__social-link"
        >
          <i class="ri-linkedin-box-fill"></i>
        </a>
        <a href="mailto:yuridevfrontend@gmail.com" target="_blank" class="contact__social-link">
          <i class="ri-mail-line"></i>
        </a>
        <a href="https://wa.me/16993777570?" target="_blank" class="contact__social-link">
          <i class="ri-whatsapp-line"></i>
        </a>
      </div>

      <form @submit.prevent="sendEmail" class="contact__form" id="contact--form">
        <div class="contact__group">
            <input type="text" name="user_name" required placeholder="Enter your name" class="contact__input">
            <input type="email" name="user_email" required placeholder="Enter your email" class="contact__input">
        </div>

        <textarea name="user_project" required placeholder="Enter your message" class="contact__input"></textarea>

        <p class="contact__message" id="contact-message"></p>

        <button type="submit" class="button contact__button">
            Send Message
        </button>
      </form>
    </div>

    <div></div>
  </section>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
    }
  },
  methods: {  
    sendEmail() {
      const contactMessage = document.getElementById('contact-message');
      const contactForm = document.getElementById('contact--form');

      emailjs.sendForm('service_bltvn57', 'template_povv9k9', '#contact--form', 'ZZtw7IUkOOJWGDsu6')     
      .then(() => {
          contactMessage.textContent = 'Mensagem enviado com sucesso!'

          setTimeout(() => {
            contactMessage.textContent = ''
          }, 5000);

          contactForm.reset()

      }, () => {
          contactMessage.textContent = 'Erro ao enviar a mensagem!'
      });
    },
  }
}
</script>

<style lang="scss">
.contact {
  &__container {
    padding-top: 1rem;
    @media screen and (min-width: 576px) {
      grid-template-columns: 360px;
      justify-content: center;
    }

    @media screen and (min-width: 1152px) {
      grid-template-columns: 680px;
      padding-block: 2.5rem 2rem;
    }

    .contact__social {
      display: flex;
      justify-content: center;
      column-gap: 1.25rem;

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

    .contact__form,
    .contact__group {
        display: grid;
        row-gap: 1rem;
    } 

    @media screen and (min-width: 1152px) {
      .contact__group {
        grid-template-columns: repeat(2, 1fr);
        column-gap: 1.5rem;
      }
    }
    
    .contact__form {
      position: relative;

      @media screen and (min-width: 1152px) {
        row-gap: 1.5rem;
      }

      .contact__input {
      padding: 1rem 1.25rem;
      border-radius: .5rem;
      background-color: var(--container-color);
      color: var(--title-color);

      @media screen and (min-width: 1152px) {
        padding: 1.5rem;
      }

        &::placeholder {
          color: var(--text-color);
        }
      }

        textarea {
          height: 11rem;
          resize: none;
          margin-bottom: 2rem;

          @media screen and (min-width: 1152px) {
            height: 20rem;
          }
        }

        .contact__message {
          position: absolute;
          left: 0;
          bottom: 4.5rem;
          font-size: var(--small-font-size);
          color: var(--title-color);
        }

        .contact__button {
          justify-self: center;
          cursor: pointer;
        }
    }
  }
}
</style>
