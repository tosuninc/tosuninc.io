<template>
    <div id="TeamView">
        <Navbar />
        <Founders />
        <Teams />
        <AllMembers />
        <Footer />
    </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Founders from '@/components/Team/Founders.vue'
import Teams from '@/components/Team/Teams.vue'
import AllMembers from '@/components/Team/AllMembers.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'TeamView',
  components: {
    Navbar,
    Founders,
    Teams,
    AllMembers,
    Footer
  }
}
</script>

<style>

</style>
