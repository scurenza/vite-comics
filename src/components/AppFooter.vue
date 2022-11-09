<script>
export default {
    name: "AppFooter",
    data () {
        return {
            socials: [
                {
                    name: "Facebook",
                    href: "/facebook",
                    imgSrc: "footer-facebook.png"
                },
                {
                    name: "Twitter",
                    href: "/twitter",
                    imgSrc: "footer-twitter.png"
                },
                {
                    name: "Youtube",
                    href: "/youtube",
                    imgSrc: "footer-youtube.png"
                },
                {
                    name: "Pinterest",
                    href: "/pinterest",
                    imgSrc: "footer-pinterest.png"
                },
                {
                    name: "Periscope",
                    href: "/periscope",
                    imgSrc: "footer-periscope.png"
                }
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
    <footer>
        <div class="container">
            <div class="cta">
                <a class="btn" href="">SIGN-UP NOW!</a>
            </div>
            <div class="socials">
                <span>FOLLOW US</span>
                <ul>
                    <li v-for="(item, index) in socials" :key="index">
                        <a :href="item.href">
                            <img :src="getImagePath(`../assets/img/${item.imgSrc}`)" alt="">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/_mixins.scss" as *;
@use "../styles/partials/_variables.scss" as *;

footer{
    width: 100%;
    height: $footer-height;
    background-color: $footer-color;

    position: relative;
    z-index: 5;

    .container{
        width: 70%;
        height: $footer-height;
        margin: 0 auto;
        display: flex;
        align-items: center;
        justify-content: space-between;

        .btn{
            color: white;
            border: 2px solid $primary-color;
            padding: .8rem;
        }

        span{
            color: $primary-color;
            font-size: 1.3rem;
            font-weight: 600;
        }

        .socials{
            width: 30%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        ul{
            width: 65%;
            display: flex;
            justify-content: space-between;
        }
    }
}

</style>