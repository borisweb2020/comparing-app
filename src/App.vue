<template>
  <header-app></header-app>
  <div class="container">
    <intro-app :smarts="smartphones"></intro-app>
  </div>
  <table-app></table-app>
</template>

<script>
  import HeaderApp from './components/HeaderApp.vue';
  import IntroApp from './components/IntroApp.vue';
  import TableApp from './components/TableApp.vue';

  export default {

    components: {
      HeaderApp,
      IntroApp,
      TableApp
    },

    data(){
      return {
        smartphones: [
          {producer: 'Apple iPnone 12', release: '2020', diagonal: '6.1', state: 'Китай', memory: '128 Гб', refresh: '60 Гц', nfc: false, esim: true, charging: true, price: '81 990 Р', url: 'src/assets/images/apple-12.jpg'},
          {producer: 'Xiaomi Mi 11 Lite', release: '2021', diagonal: '6.55', state: 'Китай', memory: '128 Гб', refresh: '90 Гц', nfc: true, esim: true, charging: false, price: '27 490 Р', url: 'src/assets/images/xiaomi-11.jpg'},
          {producer: 'Samsung Galaxy A72', release: '2021', diagonal: '6.7', state: 'Вьетнам', memory: '128 Гб', refresh: '90 Гц', nfc: true, esim: false, charging: true, price: '32 890 Р', url: 'src/assets/images/samsung-72.jpg'},
        ],
      }
    },

    mounted(){
      this.displayLog();
    },

    methods: {
      displayLog(){
        console.log(this.smartphones.length);
      }
    }

  }
</script>

<style lang="scss">
  .container{
    width: 100%;
    max-width: 1140px;
    padding: 0 15px;
    margin: 0 auto;
  }
</style>
