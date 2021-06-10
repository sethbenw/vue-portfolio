<template>
    <nav class="primary-navigation navbar navbar-expand-md">
      <div class="container-fluid">
        <div class="brand">
            <router-link class="links head-logo" to="/">
            SW
            </router-link>
        </div>
        <button
        class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbar" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <i class="fa fa-bars"></i>
        </button>
        <div class="collapse navbar-collapse justify-content-end" id="navbar">
            <ul class="nav navbar-nav">
                <router-link class="links" to="/about">ABOUT</router-link>
                <router-link class="links" to="/resume">RESUME</router-link>
            </ul>
        </div>
      </div>
    </nav>
</template>

<script>

export default {
    name: 'Header',
    methods: {
      
    }
}
</script>

<style scoped>

.primary-navigation {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 24px !important;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: #328998;
}
.links {
  text-decoration: none;
  margin-right: 55px;
  color: #ccc;
  transition: 0.5s;
  letter-spacing: 2.5px;
}
.links:hover {
  text-decoration: none;
  color: #fff;
  transition: color 0.5s;
}
.nav-links {
  display: none;
}

#navbar {
  padding: auto 0px;
  font-weight: bold;
}
.router-link:hover {
  text-decoration: none;
}
.router-link-active {
  color: #fff;
}
</style>