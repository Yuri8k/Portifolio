<template>
    <footer class="footer">
        <div class="footer__container container grid">
            <div>
                <h1 class="footer_title">
                    Yuri <span>Oliveira</span>
                </h1>

                <h2 class="footer__education">
                    Front-end Developer
                </h2>
            </div>

            <div class="footer__social">
                <a href="https://www.facebook.com/yuri.oliveira.902819/" target="_blank" class="footer__social-link">
                    <i class="ri-facebook-circle-line"></i>
                </a>

                <a href="https://www.instagram.com/yurioliveira.marques/" target="_blank" class="footer__social-link">
                    <i class="ri-instagram-line"></i>
                </a>
            </div>

            <span class="footer__copy">
                Como Front-end tenho uma
                abordagem centrada no usuário e uma paixão pela excelência técnica, busco constantemente
                superar expectativas e entregar resultados de alta qualidade.
            </span>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style lang="scss">
.footer {
    background-color: var(--container-color);
    padding-block: 3.5rem 2rem;

    @media screen and (min-width: 1152px) {
        padding-block: 4.5rem 4rem;
    }

    &__container {
        row-gap: 2rem;
        text-align: center;
        @media screen and (min-width: 576px) {
            grid-template-columns: 360px;
            justify-content: center;
        }

        @media screen and (min-width: 1023px) {
            grid-template-columns: 768px;
            justify-content: center;
        }

        .footer_title {
           font-size: var(--h1-font-size);
           font-weight: var(--font-semi-bold);
           margin-bottom: .25rem; 

           @media screen and (min-width: 1152px) {
            font-size: var(--bigger-font-size);
           }

           span {
            color: var(--first-color);
           }
        }

        .footer__education {
            font-size: var(--normal-font-size);
        }

        .footer__social {
            display: flex;
            justify-content: center;
            column-gap: 1.25rem;

            @media screen and (min-width: 1152px) {
                column-gap: 1.5rem;
            }

            &-link {
                display: flex;
                background-color: var(--first-color-alt);
                padding: .5rem;
                color: var(--title-color);
                font-size: 1.5rem;
                clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
                transition: transform .4s;

                &:hover {
                    transform: translateY(-.25rem);
                }
            }
        }

        .footer__copy {
            font-size: var(--smaller-font-size);
            margin-top: 2rem;

            @media screen and (min-width: 1152px) {
                margin: 0;
                justify-self: flex-end;
            }
        }
    }
}
</style>