<template>
  <div id="app">
    <HeaderComponent />
    <MainSection />
    <FooterComponent />
    <repos />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainSection from './components/MainSection.vue';
import FooterComponent from './components/FooterComponent.vue';
import repos from './components/repos.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainSection,
    FooterComponent,
    repos
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
}
</style>