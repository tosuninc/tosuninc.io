<template>
    <div id="ProjectsView">
        <Navbar />
        <Projects />
        <Footer />
    </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Projects from '@/components/Projects/Projects.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'ProjectsView',
  components: {
    Navbar,
    Projects,
    Footer
  }
}
</script>

<style>

</style>
