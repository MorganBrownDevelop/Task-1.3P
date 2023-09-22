<template>
  <div class="home">
    <HeroBanner 
    heading="Morgan Brown" 
    Subheading="Dev Portfolio" 
    Image="img/images/hero.jpg"
    />
    <Banner 
    heading="Hello," 
    Subheading="I’m Morgan Let’s begin."
    />
    <HeroBanner 
    heading="I am a front-end developer" 
    Subheading="Since 2021" 
    Description="I have been developing for 2 years professionally. I enjoy everything programming." 
    Image="img/images/about.jpg"
    />
    <Banner 
    heading="My quote," 
    Subheading="Code is everywhere embrace your inner coder &#128187;"
    />
    <HeroBanner 
    heading="Feel free to browse my portfolio" 
    Subheading="via the hamburger menu & footer - Get Inspired"  
    Image="img/images/projects.jpg"
    />
  </div>
</template>

<script>
// @ is an alias to /src
import HeroBanner from '@/components/HeroBanner.vue'
import Banner from '@/components/Banner.vue'

export default {
  name: 'HomeView',
  components: {
    HeroBanner,
    Banner  
  }
}
</script>
