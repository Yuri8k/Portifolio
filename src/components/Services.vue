<template>
    <section class="services section" id="services">
        <h3 class="section__subtitle">
            O que eu <span>Faço</span>
        </h3>

        <h2 class="section__title">
            Atualmente
        </h2>

        <div class="services__container container grid">
            <article class="services__card">
                <i class="ri-layout-3-line services__icon"></i>

                <h2 class="services__title">Web Developer</h2>

                <p class="services__description">
                    Desenvolvimento de páginas web personalizadas.
                    Usando tecnologias atuais e
                    incluindo a criação de layouts intuitivos, otimizados para diversos dispositivos e navegadores.
                </p>
            </article>

            <article class="services__card">
                <i class="ri-device-line services__icon"></i>

                <h2 class="services__title">Desenvolvimento</h2>

                <p class="services__description">
                    Participação e experiência em métodos de desenvolvimento
                    ágeis, fazemos o uso de Scrumban no desenvolvimento de
                    funcionalidades e Kanban na criação de novas lojas
                </p>
            </article>

            <article class="services__card">
                <i class="ri-shopping-bag-line services__icon"></i>

                <h2 class="services__title">Criação</h2>

                <p class="services__description">
                    Criação do front-end de mais de 50 lojas de e-commerce,
                    utlizando sass, javascript, django, bootstrap, webpack, VueJS entre outros,
                    e Desenvolvimento de novas funcionalidades
                </p>
            </article>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Services'
}
</script>

<style lang="scss">
    .services__container {
        row-gap: 2rem;
        padding-block: 1rem;

        @media screen and (min-width: 576px) {
            grid-template-columns: 360px;
            justify-content: center;
        }

        @media screen and (min-width: 768px) {
            grid-template-columns: repeat(2, 352px);
            align-items: center;
        }

        @media screen and (min-width: 1152px) {
            grid-template-columns:  repeat(3, 352px);
            padding-block: 2.5rem 4rem;
        }

        .services__card {
            text-align: center;
            background-color: var(--container-color);
            padding: 3rem 1.25rem;
            border-radius: 1rem;
            border: 2px solid var(--container-color);
            transition: border .4s;

            @media screen and (max-width: 320px){
                padding-block: 1.5rem;
            }

            @media screen and (min-width: 1152px) {
                padding: 3.5rem 2rem;
            }

            &:hover {
                border: 2px solid var(--first-color);
            }

            .services__icon {
                display: block;
                font-size: 4rem;
                color: var(--first-color);
                margin-bottom: .75rem;
            }

            .services__title {
                font-size: var(--h2-font-size);
                margin-bottom: 1.5rem;
            }
        }
    }
</style>