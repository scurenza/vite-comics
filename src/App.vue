<script>
  import AppHeader from "./components/AppHeader.vue"
  import AppFooter from "./components/AppFooter.vue"
  import AppBanner from "./components/AppBanner.vue"
  import AppList from "./components/AppList.vue"
  import MainContent from "./components/MainContent.vue"

  export default {
    components: {
      AppHeader,
      MainContent,
      AppBanner,
      AppList,
      AppFooter
    }
  }
</script>

<template>
  <AppHeader />
  <MainContent />
  <AppBanner />
  <AppList />
  <AppList />
</template>

<style lang="scss">

@use "./styles/general.scss" as *;

#app {
  width: 100%;
  height: 100vh;
}
</style>