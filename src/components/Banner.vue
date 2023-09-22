<template>
    <div class="cta_banner">
      <div class="content_block">
        <h1>{{ heading }}</h1>
        <h2>{{ Subheading }}</h2>
      </div>
    </div>
</template>

<script>
    export default {
    name: 'Banner',
    props: {
      heading: String,
      Subheading: String,
    }
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
</style>