<template>
    <div id="AllProjects">
        <div class="container-fluid mt-5">
            <div class="row">
                <div class="col-lg-10 col-sm-12 offset-lg-1">
                    <h1>All Projects</h1>
                    <p class="text-muted">
                        Here you can find all of Tosun projects.
                        All of these projects are open-sourced and
                        waiting for your contributions.
                    </p>

                    <p class="text-muted">
                        You can find all the project in Tosun's Github organization too.
                        <br>
                        <a href="https://github.com/tosuninc" target="_blank" class="pretty-hyperlink">
                            <i class="fab fa-github"></i>
                            Tosun Github Organization
                        </a>.
                    </p>
                    <hr>
                </div>
            </div>

            <div class="row mt-3">

                <div class="col-lg-10 col-sm-12 offset-lg-1">
                    <div class="row">

                        <div v-for="project in projects" :key="project.name" class="col-4 mb-3">
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
                                <ul v-if="Object.keys(project.dependencies).length > 0" class="list-group list-group-flush">
                                    <li class="list-group-item"><strong>Dependencies</strong></li>
                                    <li v-for="name in Object.keys(project.dependencies)" :key="name" class="list-group-item">
                                        {{ name }}: {{ project.dependencies[name] }}
                                        <span v-if="isTosunProject(name)" class="badge bg-success float-end">
                                            <i class="fas fa-check"></i>
                                            Tosun Project
                                        </span>
                                    </li>
                                </ul>
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
import AllProjects from '@/assets/allprojects.json'

export default {
  name: 'AllProjects',
  data () {
    return {
      projects: AllProjects
    }
  },
  methods: {
    isTosunProject (name) {
      return this.projects.find(project => project.name === name) !== undefined
    }
  }
}
</script>

<style scoped>
.pretty-hyperlink {
    color: #212121;
    text-decoration: none;
}
.pretty-hyperlink:hover {
    color: #212121;
    text-decoration: underline;
}
</style>
