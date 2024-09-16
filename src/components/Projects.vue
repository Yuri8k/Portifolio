<template>
    <section class="projects section" id="projects">
        <h3 class="section__subtitle">
            Meus <span>trabalhos</span>
        </h3>

        <h2 class="section__title">
            Principais Projetos
        </h2>

        <div class="projects__container container grid">
            <article class="projects__card">
                <img src="../assets/img/project-img-1.png" alt="Animation Effects" class="projects__img">

                <div class="projects__modal">
                    <span class="projects__subtitle">Web</span>

                    <h2 class="projects__title">Animações modernas</h2>

                    <a target="_blank" href="https://yuri8k.github.io/Animation-Effects/?=987123" class="projects__button">
                        Ver Projeto <i class="ri-external-link-line"></i>
                    </a>
                </div>
            </article>

            <article class="projects__card">
                <img src="../assets/img/project-img-2.png" alt="Basic Project VueJS" class="projects__img">

                <div class="projects__modal">
                    <span class="projects__subtitle">Web</span>

                    <h2 class="projects__title">Projeto básico de Vue</h2>

                    <a target="_blank" href="https://yuri8k.github.io/basic-design-add-cart-VUEJS/" class="projects__button">
                        Ver Projeto <i class="ri-external-link-line"></i>
                    </a>
                </div>
            </article>

            <article class="projects__card">
                <img src="../assets/img/Web Ecommerce.png" alt="Modern Register and Login" class="projects__img">

                <div class="projects__modal">
                    <span class="projects__subtitle">Andamento</span>

                    <h2 class="projects__title">Fake Store API</h2>

                    <a target="_blank" href="https://ecommerce-eight-plum-27.vercel.app/" class="projects__button">
                        Ver Projeto <i class="ri-external-link-line"></i>
                    </a>
                </div>
            </article>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Projects'
}
</script>

<style lang="scss">
    .projects {
        background-color: var(--conainer-color);

        &__container {
            row-gap: 2rem;
            justify-content: center;
            padding-block: 1rem;
            @media screen and (min-width: 576px) {
                grid-template-columns: 360px;
                justify-content: center;
            }

            @media screen and (min-width: 768px) {
                grid-template-columns: repeat(2, 352px);
                align-items: center;
            }

            @media screen and (min-width: 1023px) {
                grid-template-columns: repeat(3, 350px);
                row-gap: 3rem;
                padding-block: 2.5rem 4rem;
            }

            .projects__card {
                position: relative;
                border-radius: 1rem;
                overflow: hidden;
                height: 100%;

                @media screen and (min-width: 1023px) {
                    &:hover {
                        .projects__modal {
                            bottom: 0;
                        }
                    }
                }

                .projects__img {
                    width: 100%;
                    height: 100%;
                }

                .projects__modal {
                    position: absolute;
                    left: 0;
                    bottom: 0;
                    width: 100%;
                    height: 100%;
                    background: linear-gradient(180deg, hsla(0, 0%, 0%, 0) 0%, hsla(var(--hue), 70%, 40%, .8) 120%);
                    backdrop-filter: blur(4px);
                    --webkit-backdrop-filter: blur(4px);
                    border-radius: 1rem;
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    justify-content: center;
                    transition: bottom .4s;

                    @media screen and (min-width: 1023px) {
                        bottom: -100%;
                    }

                    .projects__subtitle, .projects__button {
                        color: var(--title-color);
                        font-size: var(--small-font-size);
                    }

                    .projects__subtitle {
                        display: block;
                        margin-bottom: .25rem;
                    }

                    .projects__title {
                        font-size: var(--h2-font-size);
                        margin-bottom: .75rem;
                    }

                    .projects__button {
                        display: flex;
                        align-content: center;
                        column-gap: .5rem;
                        font-weight: var(--font-medium);

                        @media screen and (min-width: 1152px) {
                            font-size: var(--normal-font-size);
                        }

                        i {
                            font-size: 1.25rem;
                        }
                    }
                }
            }
        }
    }
</style>