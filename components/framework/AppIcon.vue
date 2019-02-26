<template>
    <div>
        <font-awesome-icon
            v-bind:icon="name"
            v-bind:transform="transform"
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
        faHome,
        faWrench,
        faBook,
        faCode,
        faPencilAlt,
        faEnvelope,
    } from '@fortawesome/free-solid-svg-icons'

    library.add(
        faBars,
        faTimes,
        faHome,
        faWrench,
        faBook,
        faCode,
        faPencilAlt,
        faEnvelope,
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
            transform: {
                type: String,
                default: '',
            }
        },
    }
</script>

