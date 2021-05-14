<template>
  <div class="responsive-nav">
    <i class="fa fa-bars" id="menu-toggle"></i>
    <div id="menu" class="menu">
      <i class="fa fa-times" id="menu-close"></i>
      <div class="container">
        <div class="image">
          <a href="#"><img src="/src/assets/images/author.jpeg" alt="" /></a>
        </div>
        <div class="author-content">
          <h4>{{ name }}</h4>
          <span>{{ description }}</span>
        </div>
        <Nav :items="items"/>
        <Social/>
        <div class="copyright-text">
          <p>{{ bottomTitle }}</p>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import Nav from './Nav';
import Social from './Social';
export default {
  components:{
    Nav,
    Social,
  },
  data(){
    return{
      items:['About Me','What I’m good at','My Work','Contact Me'],
      name:'Rushan Nazmiev',
      description: 'Web Developer',
      bottomTitle: 'Copyright 2019 Reflux Design'
    }
  }
}
</script>

<style>
.responsive-nav {
  display: inline-block;
}
.menu {
  left: 10%;
  -webkit-transition: -webkit-transform 233ms cubic-bezier(0, 0, 0.21, 1);
  -webkit-overflow-scrolling: touch;
  background-color: #a43f49;
  box-sizing: border-box;
  height: 100vh;
  max-height: 100vh !important;
  max-width: 80vw !important;
  min-width: 45px !important;
  outline: none;
  overflow-x: hidden !important;
  overflow-y: auto !important;
  padding: 0;
  position: fixed !important;
  top: calc(0px);
  width: 20%;
  will-change: transform;
  z-index: 9999 !important;
  text-align: center;
}
.menu .container {
  padding-left: 0;
  padding-right: 0;
}
.menu a {
  text-decoration: none;
  color: inherit;
}
.menu .image img {
  width: 140px;
  height: 140px;
  border-radius: 50%;
  text-align: center;
}
@media screen and (max-width: 1680px){
  .menu {
    left: 5%;
  }
}
@media screen and (max-width: 1680px) and (min-width: 846px){
  .menu .image {
    margin-top: 60px;
  }
}

</style>