<template>
  <div id="Navbar">
    <nav class="navbar navbar-expand-lg navbar-light bg-tosun">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">
                <img src="@/assets/img/only-tosun.png" class="navbar-tosun" alt="only tosun logo">
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarColor03" aria-controls="navbarColor03" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarColor03">
                <ul class="navbar-nav me-auto">
                    <li class="nav-item">
                        <router-link class="nav-link" to="/">Home</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link class="nav-link" to="/about">About</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link class="nav-link" to="/projects">Projects</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link class="nav-link" to="/team">Team</router-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.bg-tosun {
    background-color: #FFFBFB;
    border-bottom: 1px solid rgba(33, 33, 33, 0.4);
}
.navbar-tosun {
    width: 50px;
    height: 50px;
}
</style>
