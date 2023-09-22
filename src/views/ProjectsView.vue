<template>
  <div class="home">
    <HeroBanner 
    heading="My CSS Prototype Library" 
    Subheading="Projects" 
    Description="This is a personal project, I am still building its a library that is used to quickly prototype." 
    Image="img/images/csshero.png"
    />
    <HeroBanner 
    heading="Digital Car Space" 
    Subheading="Projects" 
    Description="This is a personal project that is a information site about Japanese cars, it's still being built" 
    Image="img/images/digital.png"
    />
    <HeroBanner 
    heading="Tech World" 
    Subheading="Projects" 
    Description="I built this it for university I am proud of what I was able to build." 
    Image="img/images/tech.png"
    />
  </div>
</template>

<script>
// @ is an alias to /src
import HeroBanner from '@/components/HeroBanner.vue'

export default {
  name: 'ProjectsView',
  components: {
    HeroBanner,
  }
}
</script>
