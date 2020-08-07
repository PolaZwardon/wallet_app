<template>
  <div class="wrapper">
    <div class="logo">
      <h1>Wallet</h1>
    </div>
  <b-navbar toggleable type="dark" variant="dark" class="navbar">
    <b-navbar-toggle target="navbar-toggle-collapse">
      <template v-slot:default="{ expanded }">
        <b-icon v-if="expanded" icon="chevron-bar-up"></b-icon>
        <b-icon v-else icon="chevron-bar-down"></b-icon>
      </template>
    </b-navbar-toggle>
    <b-collapse id="navbar-toggle-collapse" is-nav>
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="#profile"><i class="fas fa-border-all"></i> Dashboard</b-nav-item>
        <b-nav-item href="#services"><i class="fas fa-user-circle"></i> Accounts</b-nav-item>
        <b-nav-item href="#mobile"><i class="fas fa-mobile-alt"></i> Mobile</b-nav-item>
        <b-nav-item href="#payments"><i class="fas fa-money-check-alt"></i> Payments</b-nav-item>
        <b-nav-item href="#complaints"><i class="fas fa-comment-dots"></i> Complaints</b-nav-item>
        <b-nav-item href="#supports"><i class="fas fa-headset"></i> Supports</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
  </div>
<!--  <div class="wrapper">
    <div class="logo">
      <h1>Wallet</h1>
    </div>
    <div class="sidebar">

      <a href="#profile"><i class="fas fa-border-all"></i> Dashboard</a>
      <a href="#services"><i class="fas fa-user-circle"></i> Accounts</a>
      <a href="#mobile"><i class="fas fa-mobile-alt"></i> Mobile</a>
      <a href="#payments"><i class="fas fa-money-check-alt"></i> Payments</a>
      <a href="#complaints"><i class="far fa-comment-dots"></i> Complaints</a>
      <a href="#supports"><i class="fas fa-headset"></i> Supports</a>

    </div>

  </div>-->
</template>

<script>
  import Vue from 'vue'
  import 'bootstrap/dist/css/bootstrap.css'
  import 'bootstrap-vue/dist/bootstrap-vue.css'
  import { BNavbar } from 'bootstrap-vue'
  Vue.component('b-navbar', BNavbar);
export default {
  name: 'Navbar',
  props: {
  }
}

</script>

<style scoped>
  h1{
    margin: auto;
    font-family: Dosis,sans-serif;
    font-size: 40px;
  }
  .wrapper h1{
    text-align: center;
    margin-top: 12px;
  }
  .sidebar {
    height: 100%;
    width: 160px;
    position: relative;
    z-index: 1;
    top: 0;
    left: 0;
    overflow-x: hidden;
    padding-top: 65px;

  }

  /* Style sidebar links */
  .sidebar a {
    padding: 15px 15px 50px 16px;
    text-decoration: none;
    font-size: 20px;
    font-family: Dosis, sans-serif;
    color: rgba(40,40,40,0.89);
    display: block;
    background: rgba(251, 251, 251,0.94);

  }

  /* Style links on mouse-over */
  .sidebar a:hover {
    color: rgba(0, 165, 195,0.35);
  }

  /* Style the main content */
  .wrapper {
    padding: 0px 10px;
  }

  /* Add media queries for small screens (when the height of the screen is less than 450px, add a smaller padding and font-size) */
  @media screen and (max-height: 450px) {
    .sidebar {padding-top: 15px;}
    .sidebar a {font-size: 3vw;}
  }
  @media screen and (max-width: 450px){
    .sidebar {width: 25vw;   margin-left: 0vw;
    }
    .sidebar a {padding: 4vw}
    .sidebar a {font-size: 4vw;}

  }
  .logo{
    align-self: center;
  }
  .fas{
    font-size: 25px;
  }
  .ml-auto{
    font-size: 17px;
    font-family: Dosis,sans-serif;
  }
  .navbar{
  margin-top: 45px;
  }
</style>
