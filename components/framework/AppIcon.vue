<template>
    <div>
        <font-awesome-icon
            v-bind:icon="name"
        ></font-awesome-icon>
    </div>
</template>

<script>

    export default {
        props: {
            name: {
                type: [
                    Array,
                    String,
                ],
            required: true,
            },
        },
    }
</script>

