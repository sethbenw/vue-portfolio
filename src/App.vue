<template>
  <router-view></router-view>
  <Header />
</template>

<script>
import Header from './components/Header'

export default {
  name: 'App',
  components: {
    Header,
  },
  methods: {
    async fetchTasks() {
        const res = await fetch ('api/tasks')
        
        const data = await res.json()

        return data
    },
    async fetchTask() {
        const res = await fetch (`api/tasks/${id}`)
        
        const data = await res.json()

        return data
    }
  },
  async created() {
    this.tasks = await this.fetchTasks()
  }
}
</script>


<style>
body {
  font-family: 'Questrial', sans-serif;
  margin: 0;
}

body {
  background: linear-gradient(rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)),
    url('../public/bkgd.jpg');
  position: relative;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  height: 100%;
  display: table;
}

.head-logo {
  height: 40px;
  font-size: 45px;
  color: rgba(0, 0, 0, 0);
  background: url('../public/filler-logo.png');
  background-position: center;
  background-repeat: no-repeat;
}

.contact-links {
  text-decoration: none;
  margin-right: 55px;
  color: #ccc;
  transition: 0.5s;
}
.contact-links:hover {
  text-decoration: none;
  color: #fff;
  transition: color 0.5s;
}

a img {
  display: inline;
}
li a:hover {
  color: #fff;
}
i {
  color: #ccc;
}
.sidearmtext {
  color: #fff;
}
.cusetext {
  color: #fff;
}
.card img {
  padding: 20px;
  width: 100%;
  height: auto;
}
.contact-apps .text:first-of-type {
  display: none !important;
}
.contact-apps .text:last-of-type {
  display: none !important;
}
.smimgmargin {
  margin-top: 100px;
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

/* Animations */
.slide-fade-enter-active {
  transition: all 0.4s ease;
}
.slide-fade-leave-active {
  transition: all 0.2s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateY(-15px);
  opacity: 0;
}
.port-apps .github i {
  justify-content: center;
}

/* Responsiveness */
@media only screen and (max-width: 1024px) {
  .hero a {
    font-size: 5vw;
  }
  .employer-container {
    display: none;
  }
  .app-container {
    align-items: flex-start;
    justify-content: center;
    margin-left: 1vw;
    margin-right: 1vw;
    height: auto;
    margin-bottom: 15px;
  }
  .apps {
    height: 80vh;
  }
  .employers-apps {
    height: auto;
  }
  .edu-apps .app-container {
    height: auto;
    margin-bottom: 15px;
  }
  .apps a {
    border: none;
  }
  .employers-apps .app-bkgd {
    height: auto;
  }
  .apps img {
    width: 22vw;
    height: 22vw;
  }
  .text-container {
    width: 95%;
    margin-right: 15px;
  }
  .contact-apps .text-container {
    display: flex;
    justify-content: center;
  }
  .text {
    position: static;
    display: block !important;
    margin: 0 0 10px 0;
    width: 100%;
    transition: none;
  }
  .apps i {
    font-size: 125px;
  }
  .contact-apps .text {
    width: auto;
    height: auto;
  }
  .phone-text .job-title {
    padding: 15px;
  }
  .apps .linkedin i {
    font-size: 23.7vw;
    padding: 10px 10px 5px 10px;
  }
  .apps .phone i {
    font-size: 22vw;
  }
  .apps .mail i {
    font-size: 22vw;
  }
}
@media only screen and (max-width: 767px) {
  .apps {
    flex-direction: column;
  }
  .hero {
    height: 60vh;
  }
  .app-bkgd {
    margin: 0 0.5vw 0 0.5vw;
  }
  .app-container {
    flex-direction: row;
    height: auto;
    width: 12vw;
  }
  .app-bkgd:last-of-type {
    padding-right: 0;
  }
  .employers-apps .text {
    padding-bottom: 10px;
  }
  .github i {
    font-size: 28vw;
  }
  .phone i {
    padding: 10px;
  }
  .mail i {
    padding: 10px;
  }
  .text {
    width: 99%;
    height: 100%;
  }
  .text-container {
    flex-direction: row;
    width: 90%;
    margin: 0;
  }
  .port-header {
    padding-top: 24px;
  }
  .apps {
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
}
@media only screen and (max-width: 540px) {
  .apps img {
    width: 16vw;
    height: 16vw;
  }
  .edu-apps img {
    width: 30vw;
    height: 30vw;
  }
  .employers-apps .app-bkgd {
    margin: 15px;
  }
  .app-container {
    margin: 0;
  }
  .reddragons ul {
    padding: 0;
  }
}
@media only screen and (max-width: 400px) {
  .edu-apps img {
    width: 40vw;
    height: 40vw;
  }
}
@-webkit-keyframes typing {
  from {
    width: 0;
  }
  to {
    width: 72%;
  }
}
@-webkit-keyframes blink-caret {
  50% {
    border-color: transparent;
  }
}

</style>
