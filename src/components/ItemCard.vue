<script>
export default {
    name: "ItemCard",
    props: {
        title: String,
        ImgSrc: String,
        price: String
    }
}
</script>

<template>
    <div class="card">
        <img :src="ImgSrc" :alt="title">
        <div class="card-text">
            <div class="title">
                <h4>{{ title }}</h4>
            </div>
            <div class="price">
                <p>{{ price }}</p>
            </div>

        </div>
    </div>
</template>

<style lang="scss" scoped>
.card{
    width: calc(100% / 6 - 10px);
    margin: 10px;
}
</style>