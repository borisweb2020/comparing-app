<template>
  <header-app></header-app>
  <div class="container">
    <intro-app :smarts="smartphonesDisplay" @point="changeCount"></intro-app>
  </div>
  <table-app :smarts="smartphonesDisplay"></table-app>
  <modal-app></modal-app>
</template>

<script>
  import HeaderApp from '@/components/HeaderApp.vue';
  import IntroApp from '@/components/IntroApp.vue';
  import TableApp from '@/components/TableApp.vue';
  import ModalApp from '@/components/ModalApp.vue';

  export default {

    components: {
      HeaderApp,
      IntroApp,
      TableApp,
      ModalApp
    },

    data(){
      return {
        count: 3,
        smartphones: [
          {producer: 'Apple iPnone 12', release: '2020', diagonal: '6.1', state: 'Китай', memory: '128 Гб', refresh: '60 Гц', nfc: false, esim: true, charging: true, price: '81 990 Р', url: 'src/assets/images/apple-12.jpg'},
          {producer: 'Xiaomi Mi 11 Lite', release: '2021', diagonal: '6.55', state: 'Китай', memory: '128 Гб', refresh: '90 Гц', nfc: true, esim: true, charging: false, price: '27 490 Р', url: 'src/assets/images/xiaomi-11.jpg'},
          {producer: 'Samsung Galaxy A72', release: '2021', diagonal: '6.7', state: 'Вьетнам', memory: '128 Гб', refresh: '90 Гц', nfc: true, esim: false, charging: true, price: '32 890 Р', url: 'src/assets/images/samsung-72.jpg'},
          {producer: 'Apple iPnone XR', release: '2020', diagonal: '6.1', state: 'Китай', memory: '128 Гб', refresh: '60 Гц', nfc: false, esim: true, charging: true, price: '81 990 Р', url: 'src/assets/images/apple-12.jpg'},
          {producer: 'Xiaomi 13 Pro', release: '2021', diagonal: '6.55', state: 'Китай', memory: '128 Гб', refresh: '90 Гц', nfc: true, esim: true, charging: false, price: '27 490 Р', url: 'src/assets/images/xiaomi-11.jpg'},
          {producer: 'Samsung Galaxy S23', release: '2021', diagonal: '6.7', state: 'Вьетнам', memory: '128 Гб', refresh: '90 Гц', nfc: true, esim: false, charging: true, price: '32 890 Р', url: 'src/assets/images/samsung-72.jpg'},
          {producer: 'Apple iPnone 11 Pro', release: '2020', diagonal: '6.1', state: 'Китай', memory: '128 Гб', refresh: '60 Гц', nfc: false, esim: true, charging: true, price: '81 990 Р', url: 'src/assets/images/apple-12.jpg'},
          {producer: 'Xiaomi Mix Fold', release: '2021', diagonal: '6.55', state: 'Китай', memory: '128 Гб', refresh: '90 Гц', nfc: true, esim: true, charging: false, price: '27 490 Р', url: 'src/assets/images/xiaomi-11.jpg'},
          {producer: 'Apple iPnone 14', release: '2020', diagonal: '6.1', state: 'Китай', memory: '128 Гб', refresh: '60 Гц', nfc: false, esim: true, charging: true, price: '81 990 Р', url: 'src/assets/images/apple-12.jpg'},
        ],
        smartphonesDisplay: [],
      }
    },

    mounted(){
      this.displaySmarts(this.count);
      this.displayLog();
    },

    methods: {
      displayLog(){
        console.log(this.count);
        console.log(this.smartphones);
      },

      changeCount(value){
        this.count = value;
        this.smartphonesDisplay = [];
        this.smartphonesDisplay = [].concat(this.smartphones);
        this.smartphonesDisplay.length = this.count;
        return this.smartphonesDisplay;
      },

      displaySmarts(count){
        this.smartphonesDisplay = [].concat(this.smartphones);
        this.smartphonesDisplay.length = count;
        return this.smartphonesDisplay;
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
