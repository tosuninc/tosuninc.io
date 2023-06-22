<template>
    <div id="Teams">
        <div class="container-fluid" style="margin: 15vh 0 10vh 0;">
            <div class="row">
                <div class="col-lg-10 offset-lg-1 col-sm-12">
                    <h1>Tosun Teams</h1>
                    <p class="text-muted">
                        There are many teams under Tosun organization.
                        Each team has its own purpose and goals.
                    </p>

                    <hr>

                    <div class="row mt-5">

                        <div v-for="team in teams" :key="team.name" class="col-lg-6 col-sm-12 mt-4">
                            <h4>{{ team.name }}</h4>
                            <hr>

                            <div class="row">
                                <div v-for="member in team.members" :key="member.name" class="col-3 text-center">
                                    <a :href="`https://github.com/${member.github}`">
                                        <img :src="getImage(member.image)" alt="Member image" class="member-image">
                                    </a>
                                    <h6>{{ member.name }}</h6>
                                </div>
                            </div>
                        </div>

                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Teams',
  data () {
    return {
      teams: [
        {
          name: 'Security Managers',
          description: 'This team is responsible for the security of Tosun organization.',
          members: [
            { name: 'M. Bilgehan Ertan', github: 'bilgehanertan', image: 'bilgehan.jpeg' }
          ]
        },
        {
          name: 'AI Researchers',
          description: 'This team is responsible for the AI researches of Tosun organization.',
          members: [
            { name: 'Emirhan Boge', github: 'emirhanboge', image: 'boge.jpeg' }
          ]
        },
        {
          name: 'Project Leads',
          description: 'This team is responsible for leading the projects of Tosun organization.',
          members: [
            { name: 'Alper Berber', github: 'alperb', image: 'alper.jpeg' },
            { name: 'Edip Emre Bodur', github: 'emrebdr', image: 'emrebdr.jpeg' }
          ]
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
.member-image {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    object-fit: cover;
}
</style>
