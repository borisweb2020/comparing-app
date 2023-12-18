<template>
  <header-app></header-app>
  <div class="container">
    <intro-app></intro-app>
  </div>
  <table-app></table-app>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';
  import HeaderApp from '@/components/HeaderApp.vue';
  import IntroApp from './components/IntroApp.vue';
  import TableApp from './components/TableApp.vue';



  export default defineComponent({
    name: 'App',
    components: {
      HeaderApp,
      IntroApp,
      TableApp
    },


  });

</script>

<style lang="scss">
  .container{
    width: 100%;
    max-width: 1140px;
    padding: 0 15px;
    margin: 0 auto;
  }
</style>
