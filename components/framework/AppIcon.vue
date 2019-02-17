<template>
    <div>
        <font-awesome-icon
            v-bind:icon="name"
        ></font-awesome-icon>
    </div>
</template>

<script>
    import Vue from 'vue';
    import { library } from '@fortawesome/fontawesome-svg-core'
    import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
    import {
        faBars,
        faTimes,
    } from '@fortawesome/free-solid-svg-icons'

    library.add(
        faBars,
        faTimes,
    )

    Vue.component('font-awesome-icon', FontAwesomeIcon)

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

