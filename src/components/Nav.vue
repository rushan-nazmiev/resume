<template>
  <nav class="main-nav" role="navigation">
    <ul class="main-menu">
      <li v-for="(item, index) in items"
          :key="index">
        <a href="#section1">
          {{ item }}
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  props:['items']
}
</script>

<style scoped>
.main-nav {
  text-align: center;
}

.main-nav li:last-child a {
  border-bottom: 2px solid #fff;
}

.main-nav li {
  display: block;
}

.main-nav li a {
  height: 70px;
  line-height: 70px;
  display: inline-block;
  font-size: 16px;
  font-weight: 700;
  color: #fff;
  width: 100%;
  transition: all 0.5s;
  border-top: 2px solid #fff;
}

.main-nav li:hover a,
.main-nav li.active a {
  background: #fff;
  color: #8c363e;
}
</style>