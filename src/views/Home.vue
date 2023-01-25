<template>
    <div id="Home">
      <Navbar />
      <AboutTosun />
      <Doings />
      <FeaturedProjects />
      <JoinTosun />
      <Footer />
    </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import AboutTosun from '@/components/Home/About.vue'
import Doings from '@/components/Home/Doings.vue'
import FeaturedProjects from '@/components/Home/FeaturedProjects.vue'
import JoinTosun from '@/components/Home/JoinTosun.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
    Navbar,
    AboutTosun,
    Doings,
    FeaturedProjects,
    JoinTosun,
    Footer
  }
}
</script>
