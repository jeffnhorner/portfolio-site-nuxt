<template>
  <div>
    <MainHeader />
    <nuxt />
  </div>
</template>

<script>
    import MainHeader from '@/components/MainHeader';

    export default {
        components: {
            MainHeader,
        },
    }
</script>


<style>
    html {
        font-family: 'Montserrat', sans-serif;
        font-size: 16px;
        word-spacing: 1px;
        -ms-text-size-adjust: 100%;
        -webkit-text-size-adjust: 100%;
        -moz-osx-font-smoothing: grayscale;
        -webkit-font-smoothing: antialiased;
        box-sizing: border-box;
        color: #262626;
    }

    *,
    *:before,
    *:after {
        box-sizing: border-box;
        margin: 0;
    }

    .nuxt-link-exact-active {
        border-color: #0071FF;
        background-color: #0071FF;
        color: #fff !important;
    }
</style>
