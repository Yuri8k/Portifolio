<template>
    <a href="#" class="scrollup" id="scroll-up">
        <i class="ri-arrow-up-line"></i>
    </a>
</template>

<script>
export default {
    name: 'ScrollUp',
    methods: {
    scrollUp() {
      const scrollUp = document.getElementById('scroll-up')
      scrollY >= 350 ? scrollUp.classList.add('show-scroll') : scrollUp.classList.remove('show-scroll')
        }
    },
    created() {
        addEventListener('scroll', this.scrollUp);
    }
}
</script>

<style lang="scss">
    .scrollup {
        position: fixed;
        right: 1rem;
        bottom: -50%;
        background-color: var(--body-color);
        padding: 6px;
        display: inline-flex;
        border-radius: .25rem;
        color: var(--first-color);
        font-size: 1.25rem;
        box-shadow: 0 4px 12px hsla(228, 15%, 8%, .4);
        z-index: var(--z-tooltip);
        transition: bottom .4s, transform .4s;

        @media screen and (min-width: 1152px) {
            right: 3rem;
        }

        &.show-scroll {
            bottom: 3rem;
        }

        &:hover {
            transform: translateY(-.25rem);
        }
    }
</style>