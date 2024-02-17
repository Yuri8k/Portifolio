<template>
    <section class="services section" id="services">
        <h3 class="section__subtitle">
            My <span>Services</span>
        </h3>

        <h2 class="section__title">
            What I Do
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

        .services__card {
            text-align: center;
            background-color: var(--container-color);
            padding: 3rem 1.25rem;
            border-radius: 1rem;
            border: 2px solid var(--container-color);
            transition: border .4s;

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