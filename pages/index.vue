<template>
  <div class="home">
    <h3>Standaard opbouw taarten</h3>
    <p>
      De taarten worden standaard gemaakt van luchtige biscuit.
      Ook zijn de Chocolade biscuit, Red Velvet, en de Kokos soorten mogelijk.
      Er zijn meer smaken mogelijk. Kijk ook bij de
      <nuxt-link to="Prijs">
        prijzen
      </nuxt-link> of neem <nuxt-link to="Contact">
        contact
      </nuxt-link> met ons op.
    </p>
    <div class="imageContainer">
      <b-carousel
        id="carousel-fade"
        style="text-shadow: 0px 0px 2px #000; width:500px;height:750px;"
        fade
        indicators
        controls
      >
        <b-carousel-slide
          v-for="photo in photos"
          :key="photo.id"
          :caption="photo.alt"
          :img-src="photo.src"
        />
      </b-carousel>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
import flamingo from '../assets/images/flamingo.jpg'
import nijntje from '../assets/images/nijntje.jpg'
import kroonMeisje from '../assets/images/kroonMeisje.jpg'
import bruiloft from '../assets/images/bruiloft.jpg'
import lol from '../assets/images/lol.jpg'
import eenhoorn2 from '../assets/images/eenhoorn2.jpg'
import regenboog from '../assets/images/regenboog.jpg'
import dieren from '../assets/images/dieren.jpg'

export default {
  layouts: 'default',
    data: function() {
        return {
            photos: [
                { src: flamingo, alt: 'Flamingo', width: '200px', height: '300px'},
                { src: dieren, alt: 'Dieren', width: '200px', height: '300px'},
                { src: nijntje, alt: 'Nijntje', width: '200px', height: '300px'},
                { src: kroonMeisje, alt: 'Kroon', width: '200px', height: '300px'},
                { src: bruiloft, alt: 'Bruiloft', width: '200px', height: '300px'},
                { src: lol, alt: 'LOL', width: '250px', height: '300px'},
                { src: eenhoorn2, alt: 'Eenhoorn', width: '200px', height: '300px'},
                { src: regenboog, alt: 'Regenboog', width: '280px', height: '300px'},
            ],
        }
    }
}
</script>

<style>
/* // body {
//     margin-top: 180px;
// } */
h3 {
  text-align: center;
}
.home {
    /* // padding: 20px 20px; */
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    padding-top: 160px;
    padding-bottom: 100px;
    text-align: center
}
.photos {
  border-radius: 5px;
  margin: 5px 5px;
}
.imageContainer {
  display: flex;
  justify-content: center !important;
}
.carousel-caption {
  background-color: rgba(255, 192, 203, 0.3);
  color: black;
  padding: 5px 5px;
  border-radius: 3px;
}

</style>
