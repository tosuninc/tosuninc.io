<template>
    <div id="Founders">
        <div class="container-fluid" style="margin: 15vh 0 10vh 0;">
            <div class="row">
                <div class="col-lg-10 offset-lg-1 col-sm-12">
                    <h1>Founders</h1>
                    <p class="text-muted">
                        Here are the founders of Tosun. They are the ones who
                        started this community and made it possible.
                    </p>
                    <hr>

                    <div class="row mt-3">
                        <div v-for="founder in founders" :key="founder.name" class="col text-center">
                            <a :href="`https://github.com/${founder.github}`">
                                <img :src="getImage(founder.image)" class="founder-image" alt="Founder image">
                            </a>
                            <h4>{{ founder.name }}</h4>
                            <h6>{{ founder.title }}</h6>
                            <a :href="`mailto:${founder.email}`" class="pretty-hyperlink">
                                <i class="fas fa-envelope"></i>
                                Email
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Founders',
  data () {
    return {
      founders: [
        {
          name: 'Alper Berber',
          title: 'Co-Founder',
          email: 'berber@sabanciuniv.edu',
          image: 'alper.jpeg',
          github: 'alperb'
        },
        {
          name: 'Edip Emre Bodur',
          title: 'Co-Founder',
          email: 'edipemre.bodur@bahcesehir.edu.tr',
          image: 'emrebdr.jpeg',
          github: 'emrebdr'
        },
        {
          name: 'Emirhan Boge',
          title: 'Co-Founder',
          email: 'boge@sabanciuniv.edu',
          image: 'boge.jpeg',
          github: 'emirhanboge'
        },
        {
          name: 'M. Bilgehan Ertan',
          title: 'Co-Founder',
          email: 'mbilgehan@sabanciuniv.edu',
          image: 'bilgehan.jpeg',
          github: 'bilgehanertan'
        }
      ]
    }
  },
  methods: {
    getImage (image) {
      return require(`@/assets/img/members/${image}`)
    }
  }
}
</script>

<style>
.founder-image {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
}
.pretty-hyperlink {
    color: #212121;
    text-decoration: none;
}
.pretty-hyperlink:hover {
    color: #212121;
    text-decoration: underline;
}
</style>
