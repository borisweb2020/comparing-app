<template>
  <div class="container">
    <h1 class="title">Hello</h1>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';

  export default defineComponent({
    name: 'App'
  });

</script>

<style lang="scss">
  .container{
    width: 100%;
    max-width: 1430px;
    padding: 0 15px;
    margin: 0 auto;
  }
</style>
