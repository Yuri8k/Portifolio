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
                    See fully what skills I have and perform, To develop the projects for you.
                </p>

                <a href="#projects" class="button">See Projects</a>
            </div>

            <div class="skills__content">
                <ol class="skills__group">
                    <li class="skills__item">HTML & SCSS</li>
                    <li class="skills__item">Javascript</li>
                    <li class="skills__item">Bootstrap</li>
                    <li class="skills__item">VueJS</li>
                </ol>

                <ol class="skills__group" start="5">
                    <li class="skills__item">Git & GitHub</li>
                    <li class="skills__item">Automação <br> FRONT-END</li>
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

            .skills__data {
                text-align: center;

                .skills__description {
                    margin-bottom: 2rem;   
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
            }

            .skills__group {
                row-gap: 1rem;
                list-style: decimal-leading-zero;

                .skills__item {
                    font-weight: var(--font-medium);
                    color: var(--title-color);

                    &::marker {
                        color: var(--first-color);
                    }
                }
            }
        }
    }
</style>

<script>
export default {
    name: 'Skills'
}
</script>