<template>
    <div class="split_banner" @mouseenter="scroller" @mouseleave="scroller">
      <div class="content_block" ref="block">
        <h1 ref="textMain">{{ heading }}</h1>
        <h2 ref="textSub">{{ Subheading }}</h2>
        <p ref="textDes">{{ Description }}</p>
      </div>
      <div class="image_block" ref="image">
        <img :src="Image" alt="" >
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HeroBanner',
    props: {
      heading: String,
      Subheading: String,
      Description: String,
      Image: String
    },
    methods: {
      scroller () {
          this.$refs.block.classList.toggle("blockAnimate");
          this.$refs.image.classList.toggle("imageAnimate");
          this.$refs.textMain.classList.toggle("textAnimateMain");
          this.$refs.textSub.classList.toggle("textAnimateSub");
          this.$refs.textDes.classList.toggle("textAnimateDes");
      }
    }
  }
  </script>
  
  <style scoped>
    h1, h2 {
      transition: 3s ease-in-out;
    }
    .split_banner {
      width: 100%;
      height: 100vh;
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      overflow: hidden;
      position: relative;
    }
    p {
      font-size: 1rem;
      transition: 3s ease-in-out;
    }
    .content_block {
      width: auto;
      height: auto;
      padding: 2%;
      transition: 3s ease-in-out;
    }
    .image_block {
      left: auto;
      right: 0;
      width: 30%;
      height: 100%;
      transition: 3s ease;
      z-index: -1;
      position: absolute;
      opacity: 1;
    }
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    .imageAnimate {
      width: 100%;
      opacity: 0.2;
    }
    .blockAnimate {

      padding: 0px;
     
    }
    .textAnimateMain {
      transform: translateX(50px);
      margin-top: 50px;
    }
    .textAnimateSub {
      transform: translateX(50px);
      margin-top: 25px;
    }
    .textAnimateDes {
      transform: translateX(50px);
      margin-top: 25px;
    }
  </style>
  