<template>
    <div id="AboutTosun">
        <div class="container-fluid mb-5 mt-5">
            <div class="row">
                <div class="col-lg-5 offset-lg-1 col-sm-12">
                    <h1>What is Tosun?</h1>
                    <p>
                        Tosun is a psuedo-company that creates, maintains and contributes to open source projects.
                        We are a group of developers that are passionate about open source and we want to share our knowledge and experience with the world.
                    </p>
                </div>
                <div class="col-lg-6 text-center col-sm-12 mb-5">
                    <img src="@/assets/img/full-tosun.png" alt="Tosun Logo Full" style="height: 300px;">
                </div>
            </div>
        </div>

        <Doings />

        <JoinTosun />
    </div>
</template>

<script>
import Doings from '@/components/Home/Doings.vue'
import JoinTosun from '@/components/Home/JoinTosun.vue'

export default {
  name: 'AboutTosun',
  components: {
    Doings,
    JoinTosun
  }
}
</script>

<style>

</style>
