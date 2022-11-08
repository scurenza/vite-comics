<script>
export default {
    name: "MainContent",
    data () {
        return {
            contents: {
                title: "--> Content goes here <--"
            }
        }
    }
}
</script>

<template>
    <main>
        <div class="main-content">
            <h2>{{ contents.title }}</h2>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../styles/partials/_mixins.scss" as *;
@use "../styles/partials/_variables.scss" as *;

main {
    height: 15vh;
    background-color: black;

    .main-content {
        width: 70%;
        height: 100%;
        margin: 0 auto;

        display: flex;
        align-items: center;
    }
}

h2 {
    font-size: 2rem;
    color: white;
}
</style>