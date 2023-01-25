<template>
    <div id="FeaturedProjects">
        <div class="container-fluid pt-5">
            <div class="row mb-5">
                <div class="col-12 text-center"  style="margin: 15vh 0;">
                    <h1>Featured Projects</h1>
                </div>
            </div>
            <div class="row mt-5 mb-5">

                <div class="col-lg-10 col-sm-12 offset-lg-1">
                    <div class="row">

                        <div v-for="project in projects" :key="project.name" class="col">
                            <div class="card border-dark">
                                <div class="card-header">
                                    {{ project.name }}

                                </div>
                                <div class="card-body">
                                    <div class="card-title">
                                        <strong>Project Lead:</strong>
                                        {{ project.owner.name }}
                                        (<a :href="`mailto:${project.owner.email}`">mail</a>)
                                        (<a target="_blank" :href="`https://github.com${project.owner.github}`">github.com/{{ project.owner.github }}</a>)
                                    </div>
                                    <div class="card-title">
                                        <strong>Description:</strong>
                                    </div>
                                    <p>{{ project.description }}</p>
                                    <br>
                                    <span v-for="tag in project.status_tags" :key="tag.name" :class="`badge bg-${tag.color} me-3`" style="font-size: .7em;">
                                        {{ tag.name }}
                                    </span>
                                </div>
                                <div class="card-footer">
                                    <a target="_blank" :href="project.github_url" class="btn btn-dark float-end">View Project</a>
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
  name: 'FeaturedProjects',
  data () {
    return {
      projects: [ // max 4
        {
          name: 'crandom',
          owner: {
            name: 'Alper Berber',
            email: 'berber@sabanciuniv.edu',
            github: 'alperb'
          },
          description: 'A random number generator using circular equations to adjust probability distribution',
          status_tags: [
            { name: 'help-wanted', color: 'success' },
            { name: 'good-first-contribution', color: 'info' }
          ],
          github_url: 'https://github.com/tosuninc/crandom'
        },
        {
          name: 'uniter',
          owner: {
            name: 'Alper Berber',
            email: 'berber@sabanciuniv.edu',
            github: 'alperb'
          },
          description: 'A number millifier for converting long numbers to human readable, prettified format',
          status_tags: [
            { name: 'help-wanted', color: 'success' },
            { name: 'good-first-contribution', color: 'info' }
          ],
          github_url: 'https://github.com/tosuninc/uniter'
        },
        {
          name: 'odenne',
          owner: {
            name: 'Alper Berber',
            email: 'berber@sabanciuniv.edu',
            github: 'alperb'
          },
          description: 'A strongly typed battle simulation module written in Typescript',
          status_tags: [
            { name: 'help-wanted', color: 'success' },
            { name: 'urgent-issues', color: 'danger' },
            { name: 'documentation-missing', color: 'danger' }
          ],
          github_url: 'https://github.com/tosuninc/odenne'
        }

      ]
    }
  }
}
</script>

<style>

</style>
