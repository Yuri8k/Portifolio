<template>
    <section class="skills section" id="skills">
        <div class="skills__container container grid">
            <div class="skills__data">
                <h3 class="section__subtitle">
                    Favorite <span>Skills</span>
                </h3>

                <h2 class="section__title">
                    My Skills
                </h2>

                <p class="skills__description">
                    Veja na íntegra quais habilidades possuo e atuo, para desenvolver os meus projetos.
                </p>

                <a href="#projects" class="button">See Projects</a>
            </div>

            <div class="skills__content">
                <ol class="skills__group">
                    <li class="skills__item">HTML & SCSS</li>
                    <li class="skills__item">Javascript</li>
                    <li class="skills__item">VueJS</li>
                    <li class="skills__item">VueEX</li>
                </ol>

                <ol class="skills__group" start="5">
                    <li class="skills__item">NuxtJS</li>
                    <li class="skills__item">Git & GitHub</li>
                </ol>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
    .skills {
        background-color: var(--container-color);
        display: flex;
        align-content: center;
        justify-content: center;

        &__container {
            padding-bottom: 2rem;
            row-gap: 3.5rem;
            @media screen and (min-width: 576px) {
                grid-template-columns: 360px;
                justify-content: center;
            }

            @media screen and (min-width: 768px) {
                grid-template-columns: repeat(2, 1fr);
                align-items: center;
            }

            @media screen and (min-width: 1152px) {
                grid-template-columns:  340px 425px;
                column-gap: 10rem;
                padding-bottom: 4rem;
            }

            .skills__data {
                text-align: center;

                @media screen and (min-width: 768px) {
                    text-align: initial;

                    .section__subtitle, .section__title{
                        text-align: initial;
                    }
                }

                .skills__description {
                    margin-bottom: 2rem;   

                    @media screen and (min-width: 1152px) {
                        margin-bottom: 3rem;
                    }
                }
            }

            .skills__content, .skills__group {
                display: grid;
            }

            .skills__content {
                grid-template-columns: repeat(2, max-content);
                column-gap: 4rem;
                justify-content: center;
                align-items: baseline;

                @media screen and (min-width: 1152px) {
                    column-gap: 8rem;
                }
            }

            .skills__group {
                row-gap: 1rem;
                list-style: decimal-leading-zero;

                @media screen and (min-width: 1152px) {
                    row-gap: 1.5rem;

                    .skills__item {
                        font-size: var(--h3-font-size);
                    }
                }

                .skills__item {
                    font-weight: var(--font-medium);
                    color: var(--title-color);

                    &::marker {
                        color: var(--first-color);
                    }
                }
            }
        }

        @media screen and (max-width: 320px) {
            .skills__content {
                grid-template-columns: max-content;
                row-gap: 1rem;
            }
        }
    }
</style>

<script>
export default {
    name: 'Skills'
}
</script>