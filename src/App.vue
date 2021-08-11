<template>
  <div id="app">
    <nav class="navbar navbar-light bg-light">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img src="/src/assets/logo.png" alt="">
        </a>
      </div>
    </nav>
    <h1 style="text-align: left;">Products</h1>
    <p style="text-align: left; ">7 items</p>
    <div class="container-fluid d-flex justify-content-center p-0">
      <div class="row justify-content-center w-100">
        <TheCard v-for="(card, i) in products" :key="i"
          :imgsrc=card.image />
      </div>
    </div>

  </div>
</template>

<script>
import TheCard from './components/TheCard.vue'

export default {
  name: 'App',

  components: {
    TheCard
  },

  data() {
    return {
      products: [
        {
              "id": 100,
              "name": "Denim wash shirt",
              "image": "denim_wash_shirt.jpg",
              "price": 25,
              "sizes": ["S", "M"]
          },
          {
              "id": 101,
              "name": "Plaid shirt",
              "image": "plaid_shirt.jpg",
              "price": 50,
              "sizes": ["S", "M", "L", "XL"]
          },
          {
              "id": 102,
              "name": "Raglan tee",
              "image": "raglan_tee.jpg",
              "price": 30,
              "sizes": ["S", "M", "L"]
          },
          {
              "id": 103,
              "name": "Rugby jersey",
              "image": "rugby_jersey.jpg",
              "price": 35,
              "sizes": ["S", "L", "XL"]
          },
          {
              "id": 104,
              "name": "Staple tee",
              "image": "staple_tee.jpg",
              "price": 20,
              "sizes": ["L", "XL"]
          },
          {
              "id": 105,
              "name": "Staple stripe tee",
              "image": "staple_stripe.jpg",
              "price": 22,
              "sizes": ["S", "L"]
          },
          {
              "id": 106,
              "name": "Stone wash singlet",
              "image": "stone_wash.jpg",
              "price": 15,
              "sizes": ["S", "M", "XL"]
          }
      ]
    }
  },

  methods: {
  }
}
</script>

<style>
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
