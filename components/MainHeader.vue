<template>
    <header>
        <nav class="primaryNavigation">
            <ul 
                v-for="item in nav.items"
                v-bind:key="item.name"
            >
                <li class="navItem">
                    <a v-bind:href="item.link">{{ item.name }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
    export default {
        data () {
            return {
                nav: {
                    items: [
                        {
                            name: 'home',
                            link: '/',
                        },
                        {
                            name: 'about',
                            link: '/about',
                        },
                        {
                            name: 'portfolio',
                            link: '/portfolio',
                        },
                        {
                            name: 'learn-to-code',
                            link: '/learn-to-code',
                        },
                        {
                            name: 'contact',
                            link: '/contact',
                        },
                    ],
                },
            };
        }
    }
</script>

<style lang="scss">
    // @import '@assets/css'

    .primaryNavigation {
        @apply flex flex-row;

        .navItem {
            @apply list-reset;
        }
    }

</style>
