<template>
  <div>
    <b-navbar toggleable="lg" type="light" variant="info">
      <b-navbar-brand href="#">
        <nuxt-link class="nav-link" to="/">
          <img :src="logo" class="logo" alt="Logo">
        </nuxt-link>
      </b-navbar-brand>
      <b-navbar-toggle target="nav-collapse" />

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <nuxt-link class="nav-link" to="/">
            <b-icon-house /> Home
          </nuxt-link>
          <!-- <nuxt-link class="nav-link" to="Contact">
            <b-icon-mailbox /> Contact
          </nuxt-link> -->
          <nuxt-link class="nav-link" to="Prijs">
            <b-icon-cash /> Prijzen
          </nuxt-link>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
import logo from '../assets/images/logo.png'

export default {
  data () {
    return {
      logo
    }
  }
}
</script>

<style>

body {
    color: black;
}
    .menu {
        top: 0%;
        left: 0%;
        position: fixed;
        height: 95px;
        width: 100%;
        background-color: #f2e4fe;
        box-shadow: 3px 3px 10px black;
        z-index: 5;
    }

    .list {
        /* display: inline-block; */
        width: auto;
        float: right;
        list-style-type: none;
    }
    .list-item {
        float: right;
    }
    .navbar {
      background-color: #f2e4fe !important;
    }
    a.nav-link {
      color: black !important;
      text-decoration: none;
    }
    a.nav-link:hover {
      text-decoration: underline;
    }

    .logo {
        border: none;
        width: 85px;
        height: 85px;
    }
 @media screen and (max-width: 320px) {
    .list {
        width: 20%;
        /* padding: 5px 2px; */
    }
 }
</style>
