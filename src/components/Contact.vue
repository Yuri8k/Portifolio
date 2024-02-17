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

      <form @submit="submitForm" class="contact__form" id="contact--form">
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
    submitForm() {
    const   contacForm = document.getElementById('contact--form'),
            contactMessage = document.getElementById('contact-message')

        const sendEmail = (e) => {
            e.preventDefault();
        }       
    }
  }
}
</script>

<style lang="scss">
.contact {
  &__container {
    padding-top: 1rem;

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
    
    .contact__form {
        position: relative;

        .contact__input {
        padding: 1rem 1.25rem;
        border-radius: .5rem;
        background-color: var(--container-color);
        color: var(--title-color);

            &::placeholder {
                color: var(--text-color);
            }
        }

        textarea {
            height: 11rem;
            resize: none;
            margin-bottom: 2rem;
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
