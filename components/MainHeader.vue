<template>
    <header v-bind:class="$style.headerContainer">
        <button
            v-on:click="toggleMenu"
            v-bind:class="$style.menuBarsBtn"
        >
            <AppIcon
                name="bars"
            />
        </button>
        <nav 
            v-if="hasExpandedMenu"
            v-bind:class="$style.primaryNavigation"
        >
            <ul>
                <li
                    v-for="(item, index) in nav.items"
                    v-bind:key="index"
                    v-bind:class="$style.navItem"
                >
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
                this.hasExpandedMenu = !this.hasExpandedMenu;
            }
        }
    }
</script>

<style lang="scss" module>

    .headerContainer {
        @apply flex flex-row-reverse p-10;
    }

    .primaryNavigation {
        @apply w-full;

        ul {
            @apply flex flex-row mr-10;
        }

        .navItem {
            @apply list-reset w-1/5;

            a {
                @apply no-underline;
            }
        }
    }

    .menuBarsBtn {
        @apply z-20;

        &:focus {
            @apply outline-none;
        }
    }

</style>
