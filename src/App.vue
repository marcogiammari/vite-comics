<script>
import AppHeader from './components/AppHeader.vue';
import AppFeatures from './components/AppFeatures.vue';
import AppFooter from './components/AppFooter.vue';
import AppJumbo from './components/AppJumbo.vue';
import AppCards from './components/AppCards.vue'
import json from './assets/dc-comics.json'

export default {
    components: {
        AppHeader,
        AppFeatures,
        AppFooter,
        AppJumbo,
        AppCards
    }, 
    data() {
        return {
            myJson: json,

    }
  }
}
</script>


<template>
  <AppHeader />
  <main>
    <AppJumbo />
    <AppCards :cards = myJson />
    <AppFeatures />
  </main>
  <AppFooter />
</template>

<style lang="scss" scoped>
@use './styles/general.scss' as *;


</style>
