<template>
    <header class="container">
        <button
            v-on:click="toggleMenu"
            class="menuBars"
        >
            <AppIcon
                name="bars"
            />
        </button>
        <nav 
            v-if="hasExpandedMenu"
            class="primaryNavigation"
        >
            <ul 
                v-for="(item, index) in nav.items"
                v-bind:key="index"
            >
                <li class="navItem">
                    <a v-bind:href="item.link">{{ item.name }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
    import AppIcon from '@/components/framework/AppIcon';

    export default {
        components: {
            AppIcon,
        },
        data () {
            return {
                hasExpandedMenu: false,
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
        },
        methods: {
            toggleMenu () {
                console.log('test');
                this.hasExpandedMenu = !this.hasExpandedMenu;
            }
        }
    }
</script>

<style lang="scss">
    // @import '@assets/css'

    .container {
        @apply flex flex-row-reverse p-10;
    }

    .primaryNavigation {
        @apply flex flex-row mr-10;

        .navItem {
            @apply list-reset;
        }
    }

    .menuBars {
        &:focus {
            @apply outline-none;
        }
    }

</style>
