<template>
    <div id="Footer">
        <div id="footer" class="container-fluid">
            <div class="row">
                <div class="col-12 copy-text text-center">
                    <img src="@/assets/img/only-tosun.png" class="footer-full-tosun" alt="">
                    <br>
                    {{ currentYear }} &copy; Tosun Inc. All rights are open-sourced.
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Footer',
  computed: {
    currentYear () {
      return new Date().getFullYear()
    }
  }
}
</script>

<style src="@/assets/scss/footer.scss" lang="scss">

</style>
