<template>
    <div id="About">
        <Navbar />
        <AboutTosun />
        <Footer />
    </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import AboutTosun from '@/components/About/AboutTosun.vue'
import Footer from '@/components/Footer.vue'
export default {
  name: 'About',
  components: {
    Navbar,
    AboutTosun,
    Footer
  }
}
</script>

<style>

</style>
