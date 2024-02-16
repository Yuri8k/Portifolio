<template>
    <header class="header" id="header">
      <nav class="nav container">
        <a href="#" class="nav__logo"> Yuri <span>Oliveira</span> </a>
  
        <div :class="active ? 'show-menu' : 'close-menu'" class="nav__menu" id="nav-menu">
          <ul class="nav__list">
            <li  class="nav__item">
              <a @click="active = !active" href="#home" class="nav__link">Home</a>
            </li>
            <li class="nav__item">
              <a @click="active = !active" href="#about" class="nav__link">Sobre</a>
            </li>
            <li class="nav__item">
              <a @click="active = !active" href="#skills" class="nav__link">Skills</a>
            </li>
            <li class="nav__item">
              <a @click="active = !active" href="#projects" class="nav__link">Projetos</a>
            </li>
            <li class="nav__item">
              <a @click="active = !active" href="#contact" class="nav__link">Contato</a>
            </li>
          </ul>
  
          <div @click="active = !active" class="nav__close" id="nav-close">
            <i class="ri-close-fill"></i>
          </div>
        </div>
  
        <div  @click="active = !active" class="nav__toggle" id="nav-toggle">
          <i class="ri-menu-line"></i>
        </div>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    name: "Header",
    data() {
      return {
          active: true,
      }
    },
  };
  </script>
  
  <style lang="scss">
  .header {
    width: 100%;
    position: fixed;
    background: var(--container-color);
    top: 0;
    left: 0;
    z-index: var(--z-fixed);
    display: flex;
    align-items: center;
    justify-content: center;
  
    .nav {
      height: var(--header-height);
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 100%;
  
      &__logo {
        color: var(--title-color);
        font-weight: var(--font-medium);
  
        span {
          color: var(--first-color);
        }
      }
  
      &__toggle,
      &__close {
        display: flex;
        font-size: 1.25rem;
        color: var(--title-color);
        cursor: pointer;
        @media screen and (min-width: 1023px) {
          display: none;
        }
      }
  
      @media screen and (max-width: 1023px) {
        &__menu {
          position: fixed;
          top: 0;
          right: -100%;
          background: hsla(0, 0%, 10%, 0.3);
          width: 75%;
          height: 100%;
          padding: 4.5rem 0 0 3rem;
          backdrop-filter: blur(24px);
          --webkit-backdrop-filter: blur(24px);
          transition: right 0.4s;
  
          &.show-menu {
              right: 0;
          }
  
          .nav__list {
            display: flex;
            flex-direction: column;
            row-gap: 3rem;
  
            .nav__item {
              .nav__link {
                 color: var(--title-color); 
                 font-weight: var(--font-medium);
                 transition: color .4s;
  
                 &:hover {
                  color: var(--first-color);
                 }
              }
            }
          }
  
          .nav__close {
              position: absolute;
              top: 1rem;
              right: 1.5rem;
          }
        }
      }
  
      @media screen and (min-width: 1023px) {
        &__menu {
          .nav__list {
            display: flex;
            align-items: center;
            justify-content: center;
            row-gap: 3rem;
            gap: 30px;
  
            .nav__item {
              .nav__link {
                 color: var(--title-color); 
                 font-weight: var(--font-medium);
                 transition: color .4s;
  
                 &:hover {
                  color: var(--first-color);
                 }
              }
            }
          }
        }
      }
    }
  }
  </style>
  