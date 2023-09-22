<template>
     <div class="menu_button" @click="menuActive">
        <div class="menu_line"></div>
        <div class="menu_line"></div>
        <div class="menu_line"></div>
    </div>
    <div class="menu" :class="{menu_on: menu}">
      <div class="cross" :class="{show_nav: menu}" @click="menuActive">
        <div class="cross_line" :class="{left: menu}"></div>
        <div class="cross_line" :class="{right: menu}"></div>
      </div>
      <nav :class="{show_nav: menu}">
        <router-link to="/" @click="menuActive">Home</router-link>
        <router-link to="/projects" @click="menuActive">Projects</router-link>
        <router-link to="/contact" @click="menuActive">Contact</router-link>
      </nav>
    </div>
  </template>

  <script>
  export default {
    name: 'Header',
    data() {
        return {
            menu: false
        }
    },
    methods: {
        menuActive() {
            this.menu = !this.menu;
        }
    }
  } 
</script>

  
  <style scoped>
  a {
    font-size: 2.5rem;
    padding: 2.5px;
    transition: 0.25s ease;
  }

  a:hover {
    font-size: 3.rem;
    font-weight: bold;
  }

  .menu_button {
    position: fixed;
    z-index: 2000;
    top: 2%;
    right: 2%;
    width: 10vw;
    height: 10vw;
    max-width: 50px;
    max-height: 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    cursor: pointer;
  }

  .menu_line {
    width: 100%;
    height: 2px;
    background: #949393;
  }

  .menu {
    position: fixed;
    width: 100%;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 5000;
    background: black;
    transition: 1s ease;
    transform: translateX(-100vw);
  }
  
  .menu_on {
    transform: translateX(0);
  }
  
  .cross {
    position: absolute;
    top: 2%;
    right: 2%;
    width: 10vw;
    height: 10vw;
    max-width: 50px;
    max-height: 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    transition: 3s ease;
    opacity: 0;
    cursor: pointer;
  }
  
  .cross_line {
    position: absolute;
    width: 2px;
    height: 100%;
    background: #949393;
    transition: 3.5s ease;

  }
  
  .right {
    transform: rotateZ(-45deg);
  }
  
  .left {
    transform: rotateZ(45deg);
  }
  
  nav {
    width: auto;
    height: auto;
    transition: 3s ease;
    opacity: 0;
  }

  .show_nav {
    opacity: 1;
  }
  
  ul {
    width: auto;
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  
  #app {
    width: 100%;
  }
  </style>
  