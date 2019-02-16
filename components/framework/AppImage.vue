<template>
    <div class="">
        <img
            v-bind:src="image"
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
    }
</script>

<style lang="scss">
    
</style>
