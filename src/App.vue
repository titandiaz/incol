<template>
  <div id="app">
    <TopMenu/>
    <Menu v-if="toggleMenu"/>
    <transition name="fade">
      <Menu class="fixed" name="fade" v-if="!toggleMenu"/>
    </transition>
    <router-view/>
  </div>
</template>

<script>
import TopMenu from "@/components/TopMenu";
import Menu from "@/components/Menu.vue";
export default {
  name: "App",
  created() {
    window.addEventListener("scroll", this.handleScroll);

  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  components: {
    TopMenu,
    Menu
  },
  data() {
    return {
      toggleMenu: true
    };
  },
  methods: {
    handleScroll(event) {
      if (window.scrollY >= 100) {
        this.toggleMenu = false
      } else {
        this.toggleMenu = true;
      }
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
body {
  margin: 0;
}
.fade-enter-active {
  transition: opacity 0.5s;
  transition: all .8s ease; 
}
.fade-enter /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
  transform: translateY(-70px);
}
.fixed {
  position: fixed;
  top: 0;
  left: 0;
  box-shadow: 0px 13px 30px -12px rgba(0, 0, 0, 0.75);
}
</style>
