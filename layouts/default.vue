<template>
    <div>
        <modals-container />

        <Toasts />

        <DevWarsHeader />

        <nuxt />

        <DevWarsFooter />
    </div>
</template>

<script>
import Header from '@/components/layout/Header';
import Toasts from '@/components/toast/Toasts';

export default {
    name: 'Default',

    components: {
        DevWarsHeader: Header,
        DevWarsFooter: () => import('@/components/layout/Footer'),
        Toasts,
    },
};
</script>

<style lang="scss">
@import 'utils.scss';

*,
*:before,
*:after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    font-family: $base-font-face;
    font-size: 62.5%;
    line-height: 1.5;
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%;
    -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}

body {
    height: 100%;
    font-size: $font-size-base;
    color: $base-font-color;
    background: $bg-color-4;
    -webkit-font-smoothing: antialiased;
    transition: transform 300ms ease-in-out; // mobile-nav

    ::-webkit-scrollbar {
        width: 5px;
        height: 5px;
    }

    ::-webkit-scrollbar-track-piece {
        background-color: $bg-color-3;
    }

    ::-webkit-scrollbar-thumb {
        background-color: $silver-color;
        outline: 2px solid $silver-color;
        outline-offset: -2px;
        border: 0.1px solid $silver-color;
    }

    ::-webkit-scrollbar-thumb:hover {
        background-color: lighten($silver-color, 10%);
    }
}

img {
    border: 0;
    max-width: 100%;
}

table {
    border-collapse: collapse;
    border-spacing: 0;
    width: 100%;
}

label {
    display: block;
}

a {
    color: $link-color;
    text-decoration: none;
}

h1,
h2,
h3,
h4,
h5,
h6 {
    margin: 0;
    line-height: normal;
    word-wrap: break-word;
    font-weight: $font-weight-semibold;
}

h1 {
    text-transform: uppercase;
    font-family: $alt-font-face;
    font-size: 3.6rem;
}

h2 {
    font-family: $alt-font-face;
    font-size: 3rem;
}

h3 {
    font-size: 2.4rem;
}

h4 {
    font-size: 1.8rem
}

h5 {
    font-size: $font-size-base;
}

h6 {
    font-size: 1.2rem;
}

p {
    color: #fff;
    line-height: 1.5;
    font-size: 1.6rem;
    word-wrap: break-word;
}

.header-offset {
    padding-top: $header-offset;
    padding-bottom: $xl-space;

    @include breakpoint(md) {
        padding-top: $header-offset / 2;
    }

    @include breakpoint(sm) {
        padding-top: $header-offset / 4;
    }
}

.header-onset {
    padding-top: $header-height;
}

.footer-offset {
    padding-bottom: $xl-space;
}
</style>
