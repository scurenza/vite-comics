<script>
export default {
    name: "AppHeader",
    data () {
        return {
            logo: {
                title: "header-logo",
                src: "../assets/img/dc-logo.png"
            },
            links: [
                {
                    title: "CHARACTERS",
                    href: "/characters",
                    active: false,
                },
                {
                    title: "COMICS",
                    href: "/comics",
                    active: false,
                },                {
                    title: "MOVIES",
                    href: "/movies",
                    active: false,
                },                {
                    title: "TV",
                    href: "/tv",
                    active: false,
                },                {
                    title: "GAMES",
                    href: "/games",
                    active: false,
                },                {
                    title: "COLLECTIBLES",
                    href: "/collectibles",
                    active: false,
                },                {
                    title: "VIDEOS",
                    href: "/videos",
                    active: false,
                },                {
                    title: "FANS",
                    href: "/fans",
                    active: false,
                },                {
                    title: "NEWS",
                    href: "/news",
                    active: false,
                },                {
                    title: "SHOP",
                    href: "/shop",
                    active: false,
                },
            ]
        }
    }
}
</script>

<template>

    <header class="header">
        <div class="logo">
            <img :src='logo.src' :alt='logo.title'>
        </div>
    </header>
</template>

<style></style>