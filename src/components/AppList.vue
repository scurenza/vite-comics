<script>
export default {
    name: "AppList",
    data () {
        return {
            DcComics: [
                {
                    title: "Character",
                    href: "/characters"
                },
                {
                    title: "Comics",
                    href: "/comics"
                },
                {
                    title: "Movies",
                    href: "/movies"
                },
                {
                    title: "TV",
                    href: "/tv"
                },
                {
                    title: "Games",
                    href: "/games"
                },
                {
                    title: "Videos",
                    href: "/videos"
                },
                {
                    title: "News",
                    href: "/news"
                },
            ],
            Shop: [
                {
                    title: "Shop DC",
                    href: "/shopDC"
                },
                {
                    title: "Shop DC Collectibles",
                    href: "/shopCollectibles"
                }
            ],
            Dc: [
                {
                    title: "Terms Of Use",
                    href: "/terms"
                },
                {
                    title: "Privacy Policy (New)",
                    href: "/policy"
                },
                {
                    title: "Ad Choices",
                    href: "/adChoice"
                },
                {
                    title: "Advertising",
                    href: "/ad"
                },
                {
                    title: "Jobs",
                    href: "/jobs"
                },
                {
                    title: "Subscription",
                    href: "/sub"
                },
                {
                    title: "Talent Workshop",
                    href: "/talent"
                },
                {
                    title: "CPSC Certificates",
                    href: "/certificates"
                },
                {
                    title: "Ratings",
                    href: "/ratings"
                },
                {
                    title: "Shop Help",
                    href: "/help"
                },
                {
                    title: "Contact Us",
                    href: "/contact"
                },
            ],
            Sites: [
                {
                    title: "DC",
                    href: "/dc"
                },
                {
                    title: "MAD Magazine",
                    href: "/mad"
                },
                {
                    title: "DC Kids",
                    href: "/kids"
                },
                {
                    title: "DC Universe",
                    href: "/universe"
                },
                {
                    title: "DC Power Visa",
                    href: "/visa"
                }
            ]
        }
    }
}
</script>

<template>
    <section class="banner">
        <div class="container">
            <div class="links-container">
                <div class="links">
                    <ul>
                        <h3>DC COMICS</h3>
                        <li v-for="(item, index) in DcComics" :key="index">
                            <a :href="item.href">{{ item.title }}</a>
                        </li>
                    </ul>
                    <ul>
                        <h3>SHOP</h3>
                        <li v-for="(item, index) in Shop" :key="index">
                            <a :href="item.href">{{ item.title }}</a>
                        </li>
                    </ul>
                </div>
                <div class="links">
                    <ul>
                        <h3>DC</h3>
                        <li v-for="(item, index) in Dc" :key="index">
                            <a :href="item.href">{{ item.title }}</a>
                        </li>
                    </ul>
                </div>
                <div class="links">
                    <ul>
                        <h3>SITES</h3>
                        <li v-for="(item, index) in Sites" :key="index">
                            <a :href="item.href">{{ item.title }}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="image">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/_mixins.scss" as *;
@use "../styles/partials/_variables.scss" as *;

.banner {
    width: 100%;
    min-height: 350px;
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: top;

    z-index: 1;

    .container{
        width: 70%;
        margin: 0 auto;

        display: flex;
        justify-content: space-between;
        position: relative;

        .links-container{
            width: 35%;
            display: flex;
            justify-content: space-between;
        }
    }

    h3{
        color: white;
        font-weight: 700;
        margin-bottom: 1rem;
    }

    .links{
        padding: 1rem 0;
        min-height: 325px;

        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    // li {
    //     margin-bottom: .5rem;
    // }

    a {
        color: grey;
        font-size: .8rem;
    }

    img{
        position: absolute;
        top: -50%;
        right: 0;

        z-index: 2;
    }
}
</style>