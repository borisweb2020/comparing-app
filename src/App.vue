<template>
  <header-app></header-app>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';
  import HeaderApp from '@/components/HeaderApp.vue';

  export default defineComponent({
    name: 'App',
    components: {
      HeaderApp
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
