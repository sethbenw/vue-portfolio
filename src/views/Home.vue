<template>
  <div class="container">
    <div class="hero">
      <div class="hero-text">Developer • Designer • Superhero</div>
      <router-link class="links" to="/resume">
        <a class="contact" href="#">MY RESUME</a>
      </router-link>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
    
  }
}
</script>

<style scoped>

.container {
  margin-top: 90px;
}
/* Contact Info*/
.contact {
  border: solid 1px #ddd;
  transition: 1s;
  letter-spacing: 5.8px;
}
.contact:hover {
  background-color: #ddd;
  color: #444;
  transition: color 0.5s;
  transition: background-color 0.5s linear;
  text-decoration: none;
}

/* Homepage Main Content*/
.hero {
  display: flex;
  justify-content: space-around;
  flex-direction: column;
  text-align: center;
  height: 90vh;
  width: 100%;
  left: 50%;
  color: #ccc;
  opacity: 1;
}

.header {
  border-right: 0.1em solid #fff;
  margin-left: 15%;
  margin-right: 15%;
  margin-bottom: 24px;
  white-space: nowrap;
  overflow: hidden;
  -webkit-animation: typing 4s steps(100, end) 1s 1 normal both,
    blink-caret 0.5s step-end infinite alternate;
}
.hero a {
  text-decoration: none;
  color: #ccc;
  font-size: 2vh;
  padding: 0px 10px 5px 10px;
  margin-top: 15px;
}

.hero-text {

  color: #ccc;
  margin-left: 25px;
  font-size: 5vh;
  text-align: center;
  margin-bottom: 25px;
}

@media only screen and (max-width: 1440px) {
  .hero-text {
    font-size: 6vw;
  }
}
@media only screen and (max-width: 1024px) {
  .hero-container {
    padding-left: 0;
    width: 100%;
    height: 70vh;
    justify-content: flex-end;
  }
}
@media only screen and (max-width: 767px) {
  .hero-text {
    font-size: 7vw;
  }
}
</style>
