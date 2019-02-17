<template>
    <div class="">
        <img
            v-bind:src="imagePath"
            v-bind:alt="alt"
        >
    </div>
</template>

<script>
    export default {
        props: {
            image: {
                type: String,
                required: true,
            },
            alt: {
                type: String,
                required: true,
            },
        },
        computed: {
            imagePath () {
                return '/_nuxt/' + this.image;
            }
        }
    }
</script>
