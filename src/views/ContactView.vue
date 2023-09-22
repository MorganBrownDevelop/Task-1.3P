<template>
  <div class="home">
    <HeroBanner 
    heading="Contact" 
    Subheading="Dev Portfolio" 
    Image="img/images/hero.jpg"
    />
    <Form/>
  </div>
</template>

<script>
// @ is an alias to /src
import HeroBanner from '@/components/HeroBanner.vue'
import Banner from '@/components/Banner.vue'
import Form from '@/components/Form.vue'

export default {
  name: 'HomeView',
  components: {
    HeroBanner,
    Banner,
    Form
  }
}
</script>
