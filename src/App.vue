<script>
import AppHeader from './components/AppHeader.vue';
import AppFeatures from './components/AppFeatures.vue';
import AppFooter from './components/AppFooter.vue';


export default {
  components: {
    AppHeader,
    AppFeatures,
    AppFooter
  }
}
</script>


<template>
  <AppHeader />
  <main>
    <section id="content"></section>
    <AppFeatures />
  </main>
  <AppFooter />
</template>

<style scoped>


</style>
