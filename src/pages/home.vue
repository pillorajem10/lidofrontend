<template>
  <div>
    <div class="slider">
      <carousel>
        <slide>
          <img src="../images/slider1.jpg" alt="Slide 1">
        </slide>
        <slide>
          <img src="../images/slider2.jpg" alt="Slide 2">
        </slide>
      </carousel>
    </div>
    <div class="home">
      <div v-for="(item, index) in items" :key="index" class="card">
        <img :src="item.image" :alt="item.name" class="card-image">
        <h3>{{ item.name }}</h3>
        <p>Price: {{ formatPrice(item.price) }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import lechonMacau from '../images/lechonMacau.jpg'
import pugonRoastedAsado from '../images/pugonRoastedAsado.jpg'
import shrimpFooYong from '../images/shrimpFooYong.jpg'
import sweetAndSour from '../images/sweetAndSour.jpg'
import manchurianWings from '../images/manchurianWings.jpg'
import chamiSpecial from '../images/chamiSpecial.jpg'
import lidosSiphonBrewedCoffee from '../images/lidosSiphonBrewedCoffee.jpg'
import bilaoFeast from '../images/bilaoFeast.jpg'
import BlcFeast from '../images/BlcFeast.jpg'
import shrimpBalls from '../images/shrimpBalls.png'
import { Carousel, Slide } from 'vue-carousel'

export default {
  name: 'Home',
  components: {
    Carousel,
    Slide
  },
  data () {
    return {
      items: [
        { name: 'Drunken Lechon Macau', price: 523, image: lechonMacau },
        { name: 'Pugon-Roasted Asado', price: 501, image: pugonRoastedAsado },
        { name: 'Shrimp Foo Yong', price: 572, image: shrimpFooYong },
        { name: 'Sweet and Sour Fish Fillet', price: 413, image: sweetAndSour },
        { name: 'Manchurian Wings', price: 501, image: manchurianWings },
        { name: 'Chami Special', price: 215, image: chamiSpecial },
        { name: 'Lido\'s Siphon Brewed Coffee', price: 143, image: lidosSiphonBrewedCoffee },
        { name: 'BLC Feast', price: 1385, image: bilaoFeast },
        { name: 'BLC Feast C', price: 2573, image: BlcFeast },
        { name: 'Shrimp Balls', price: 479, image: shrimpBalls }
      ]
    }
  },
  methods: {
    formatPrice (value) {
      return value.toLocaleString('en-US', { style: 'currency', currency: 'PHP' })
    }
  }
}
</script>

<style scoped>
  .home {
    display: flex;
    flex-wrap: wrap;
    justify-content: center; /* Center content horizontally */
    margin-top: 2%;
  }

  .card {
    width: 15rem;
    margin: 1rem; /* Add margin between cards */
    padding: 1.5rem;
    border-radius: 8px;
    background-color: #ffffff;
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.5); /* Subtle shadow */
    transition: box-shadow 0.3s ease; /* Smooth shadow transition */
    text-align: center; /* Center text */
  }

  .card h3 {
    margin-bottom: 1rem;
  }

  .card p {
    color: #666666;
  }

  .card-image {
    max-width: 100%;
    border-radius: 8px 8px 0 0; /* Rounded corners on top only */
  }
  .slider {
    width: 100%;
  }

  .slider img {
    width: 100%;
    height: auto;
  }

  @media (max-width: 700px) {
    .nameFields {
        flex-direction: column;
        gap: 0;
    }
    
    .nameFields .fieldContainer {
        width: 100%;
    }

    .card {
      width: 5rem;
    }

    .card h3 {
      font-size: 12px;
      font-weight: bolder;
    }

}
</style>
