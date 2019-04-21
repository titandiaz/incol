<template>
  <div class="menu">
    <div class="logo">TU LOGO</div>
    <nav>
      <ul class="list-items">
        <li class="item" v-for="(item, index) in routes" :key="index">
          <a href="#">{{item}}</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      routes: ["Inicio", "Portafolio", "Zonas Comunes", "Contacto"]
    };
  }
};
</script>

<style scoped>
.menu {
  z-index: 9999;
  height: 70px;
  width: 100%;
  display: flex;
  justify-content: center;
  background-color: rgb(13, 5, 51);
  box-shadow: 0px 13px 30px -12px rgba(0, 0, 0, 0.75);
}
nav {
  max-width: 1200px;
  width: 100%;
  height: 100%;
  box-sizing: border-box;
  padding: 0 15px;
  display: flex;
  justify-content: flex-end;
}
.list-items {
  list-style: none;
  display: flex;
  margin: 0;
  padding: 0;
  align-items: center;
  height: 100%;
}
.item {
  text-align: center;
  line-height: 1;
  font-size: 15px;
  color: #fff;
  font-weight: 600;
  height: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  box-sizing: border-box;
  text-transform: uppercase;
}
.item:hover a {
  color: rgb(98, 98, 245);
}
.item a {
  border-right: 1px solid rgba(238, 238, 238, 0.2);
  text-decoration: none;
  color: #fff;
  padding: 0 20px;
}
li:last-child a {
  border: 0;
}
.logo {
  color: #fff;
  font-weight: 600;
  display: flex;
  align-items: center;
}
</style>
