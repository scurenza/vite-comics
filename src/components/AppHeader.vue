<script>
export default {
    name: "AppHeader",
    data () {
        return {
            logo: {
                title: "header-logo",
                logoName: "dc-logo.png"
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
    },
    methods: {
        getImagePath: function(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>

    <header class="header">
        <div class="container">
        <div class="logo">
            <img :src="getImagePath(`../assets/img/${logo.logoName}`)" :alt='logo.title'>
        </div>
        <div class="list">
            <ul>
                <li v-for="(link, index) in links" :key="index" >
                <a :class="{ 'active': link.active }" :href="link.href" @mouseover="link.active = true" @mouseleave="link.active = false">{{ link.title }}</a>
                </li>
                
            </ul>
        </div>
    </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/_mixins.scss" as *;
@use "../styles/partials/_variables.scss" as *;

header{
    width: 100%;
    background-color: white;
    

    position: fixed;
    top: 0;
    left: 0;
    z-index: 5;

    img{
        width: 75px;
    }
    .container{
        height: $header-height;
        width: 70%;
        margin: 0 auto;
        @include flex-sb-center;
    }
    ul {
        @include flex-sb-center;
        li {
            
            margin-right: 2rem;
            height: $header-height;

            a {
                display: flex;
                align-items: center;
                height: 100%;

                font-size: .8rem;
                font-weight: 600;
            }
            .active{
                color: $primary-color;
                border-bottom: 6px solid $primary-color;
            }
            
        }
    }


}


</style>