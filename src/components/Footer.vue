<template>
    <div class="cta_banner">
      <div class="content_block">
        <nav>
        <router-link to="/">Home</router-link>
        <router-link to="/projects">Projects</router-link>
        <router-link to="/contact">Contact</router-link>
      </nav>
      </div>
    </div>
</template>

<script>
    export default {
    name: 'Footer',
  }
</script>

<style scoped>
    .cta_banner {
      width: 100%;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: #070707;
    }
    .content_block {
      width: auto;
      height: auto;
    }
    a {
    font-size: 2.5rem;
    padding: 2.5px;
    transition: 0.25s ease;
  }

  a:hover {
    font-size: 3.rem;
    font-weight: bold;
  }
  
  nav {
    width: auto;
    height: auto;
    transition: 3s ease;
  }
  
  ul {
    width: auto;
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
</style>