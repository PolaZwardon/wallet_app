<template>
  <div id="app">
    <div class="container">
      <div class="box box1"><Accounts/></div>
      <div class="box box2"><Profile/></div>
      <div class="box box3"><Navbar></Navbar></div>
      <div class="box box4"><h2>My finance dashboard</h2><p>Welcome to Wallet payment portal</p></div>

    </div>

  </div>
</template>

<script>

  import 'bootstrap/dist/css/bootstrap.css'
  import 'bootstrap-vue/dist/bootstrap-vue.css'
import Navbar from "@/components/Navbar";
import Profile from "@/components/Profile";
import Login from "@/components/Login";
  import Accounts from "@/components/Accounts";

  import Vue from 'vue'
  import { BootstrapVue, IconsPlugin } from 'bootstrap-vue'

  // Install BootstrapVue
  Vue.use(BootstrapVue);
  // Optionally install the BootstrapVue icon components plugin
  Vue.use(IconsPlugin);

export default {
  name: 'App',
  components: {
    Navbar,
    // eslint-disable-next-line vue/no-unused-components
    Profile,
    // eslint-disable-next-line vue/no-unused-components
    Login,
    // eslint-disable-next-line vue/no-unused-components
    Accounts
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background: url("https://img.rawpixel.com/s3fs-private/rawpixel_images/website_content/v498-bb-27-abstractbg_1.jpg?bg=transparent&con=3&cs=srgb&dpr=1&fm=jpg&ixlib=php-3.1.0&q=80&usm=15&vib=3&w=1300&s=d1d2aea1d432c457efbec74429e5056a");
  background-position: top right;
  background-repeat: no-repeat;
  background-size: 100%;
}
/*http://wallpaperping.com/wp-content/uploads/2020/04/v498-bb-29-abstractbg_2.jpg*/
p{
  font-family: Dosis,sans-serif;
  font-size: 15px;
  color: gray;
}
h2{
  font-family: Dosis,sans-serif;
  font-size: 30px;
}
  .container{
  width: 100%;
    height: 100%;
    display: grid;
    grid-template-columns: 1fr 2fr 2fr;
    grid-template-rows: repeat(8, 1fr);
    grid-gap: 2vw;
    background: rgba(251, 251, 251,0.64);

  }
  .box4{
    grid-column: 2/2;
    grid-row: 1/1;
    background: rgba(251, 251, 251,0.74);

  }
  .box5{
    grid-column: 3/3;
    grid-row: 1/1;
  }
  .box2{
    grid-column: 2/2;
    grid-row: 2/9;

  }
.box1{
  grid-column: 3/3;
  grid-row: 2/9;

}
  .box3{
    grid-column: 1/1;
    grid-row: 1/9;
  }
    .box{
    }
@media screen and (max-height: 450px) {
  .sidebar {padding-top: 15px;}
  .sidebar a {font-size: 3vw;}
}
@media screen and (max-width: 770px){
  .container{
    width: 100%;
    height: 100%;
    display: grid;
    grid-template-columns: 1fr 2fr;
    grid-template-rows: repeat(8, 1fr);
    grid-gap: 2vw;
  }
  .box2{
    grid-column: 1/3;
    grid-row: 3/5;

  }
  .box1{
    grid-column: 1/3;
    grid-row: 5/9;

  }
  .box3{
    grid-column: 1/3;
    grid-row: 1/1;
  }
.box4{
  grid-column: 1/3;
  grid-row: 2/2;
  text-align: center;
}
.container{
  grid-template-rows: 1fr;
}
}
</style>
