<script>
export default {
    name: "AppBanner",
    data () {
        return {
            shopItems: [
                {
                    itemName: "DIGITAL COMICS",
                    itemImage: "buy-comics-digital-comics.png",
                    href: "/comics",
                    active: false
                },
                {
                    itemName: "DC MERCHANDISE",
                    itemImage: "buy-comics-merchandise.png",
                    href: "/merchandise",
                    active: false
                },
                {
                    itemName: "SUBSCRIPTION",
                    itemImage: "buy-comics-subscriptions.png",
                    href: "/subscription",
                    active: false
                },
                {
                    itemName: "COMIC SHOP LOCATOR",
                    itemImage: "buy-comics-shop-locator.png",
                    href: "/shop",
                    active: false
                },
                {
                    itemName: "DC POWER VISA",
                    itemImage: "buy-dc-power-visa.svg",
                    href: "/visa",
                    active: false
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
    <section class="banner">
        <div class="banner-content">
            <ul>
                <li v-for="(item, index) in shopItems" :key="index">
                    <a :href="item.href" :class="{ 'active': item.active }" @mouseover="item.active = true" @mouseleave="item.active = false">
                    <img :src="getImagePath(`../assets/img/${item.itemImage}`)" :alt="item.itemName">
                    <span>{{ item.itemName }}</span>
                    </a>
                </li>
            </ul>
        </div>

    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/_mixins.scss" as *;
@use "../styles/partials/_variables.scss" as *;

.banner{
    width: 100%;
    height: $banner-height;

    background-color: $primary-color;
    

    &-content{
        width: 70%;
        margin: 0 auto;
        
    }

    ul {
        @include flex-sb-center;
        padding: 0 3rem;
        
        li {
            height: $banner-height;
            width: calc(100% / 5 - 1rem);

            display: flex;
            align-items: center;

            a {
                height: $banner-height;
                display: flex;
                align-items: center;
                z-index: 5;
            }

            img {
                width: 50px;
                height: 60px;
                margin-right: 1rem;
            }

            span {
                color: white;
            }

            .active {
                border-bottom: 6px solid white;
            }
        }
    }
}
</style>