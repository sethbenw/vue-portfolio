<template>
  <div class="container d-flex flex-wrap">
    <div class="hero-top">
      <p class="">Above all things I love comic books: the characters, the stories, and most of all the art. Artists and Writers alike inspired me to follow my passion of art and creativity which led to my interest in graphic design and web development.</p>
      
      <!--div :show="isActive" class="">
        <div class="employers-apps apps">
          <div class="app-container">
            <div
              v-for="(job, index) in jobs"
              :key="index"
              @mouseover="selectIndex(index)"
              @mouseout="ItemIndex = null"
              class="app-bkgd"
            >
              <a :href="job.link">
                <div :class="job.employer">
                  <img :src="getSrc(job.employer)" />
                </div>
              </a>
              <div class="employer">{{ job.employerDisplay }}</div>
            </div>
          </div>
        </div>
      </div-->

      <router-link class="links d-flex justify-content-center mt-5" to="/resume">
        <a class="contact">MY RESUME</a>
      </router-link>
    </div>    
  </div>

</template>

<script>
// @ is an alias to /src

export default {
  name: 'About',
  components: {},
  data: {
    isActive: false
  },
  data() {
    return {
      jobs: [
        {
          employerDisplay: 'Designer',
          employer: 'ybfcare',
          text: 'dovr',
          link: '/',
          title: 'Project Development Coordinator',
          hover: false,
          description: [
            { bullet: 'Mentored over 20 students during Lab days' },
            {
              bullet:
                'Evaluated labs assignments created by the professor before being released to students',
            },
            {
              bullet:
                'Tutored students during office hours without the instructor every week for 1 hour',
            },
          ],
        },
        {
          employerDisplay: 'Developer',
          employer: 'sidearm',
          text: 'sidearmsports',
          link: '/',
          title: 'Data Curation & Production Assistant',
          hover: false,
          description: [
            {
              bullet:
                'Analyzed and managed data from over 85 legacy websites in order to update the new sites via proprietary SQL-based CMS',
            },
            {
              bullet:
                'Collaborated with programming team daily to communicate issues relating with data retrieval',
            },
            {
              bullet:
                'Collaborated with project managers when contact with the client organization was necessary',
            },
          ],
        },
        {
          employerDisplay: 'Superhero',
          employer: 'kappathetapi',
          text: 'dovr',
          link: '/',
          title: 'VP of Design and Development',
          hover: false,
          description: [
            {
              bullet:
                'Created graphics, advertisments and web content for the high-end interior design magazine, Design Dwell, in the attempt to grow the companys online presence',
            },
            {
              bullet:
                'Specifically, I created advertisements for use in the re-branded magazine, these ads were published and used as proof of product for clients and shareholders.',
            },
          ],
        },
      ],
      ItemIndex: null,
    }
  },
  methods: {
    selectIndex(Index) {
      this.ItemIndex = Index
    },
    getSrc(employer) {
      var images = require.context('../assets/', false, /\.png$/)
      return images('./' + employer + '.png')
    },
  },
}
</script>

<style scoped>
.container {
  margin-top: 90px;
}
/* Homepage Main Content*/
.hero-top {
  display: flex;
  justify-content: center;
  flex-direction: column;
  height: 90vh;
  width: 100%;
  left: 50%;
  font-size: 1.5rem;
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
.hero-top a {
  text-decoration: none;
  color: #ccc;
  font-size: 1.5rem;
  padding: 0px 10px 5px 10px;
  margin-top: 5px;
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

.employer {
  color: #ccc;
  padding-top: 5px;
  text-align: center;
}
.apps {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.apps a {
  border: 25px solid transparent;
}
.apps img {
  height: 200px;
}
.sidearm {
  background-color: #283b4c;
  border-radius: 25px;
  padding: 10px;
  transition: 0.5s;
}
.sidearm:hover {
  background-color: #000;
  transition: 0.5s;
}
.sidearmsports {
  background-color: #283b4c;
  color: #fff;
}
.text {
  position: absolute;
  left: 50%;
  height: 100%;
  margin-left: -375px;
  border-radius: 25px;
  height: 175px;
  width: 750px;
  margin-top: 15px;
}
.job-title {
  padding-top: 20px;
  font-weight: 700;
}
.dovr .job-title,
.sidearmsports .job-title {
  padding-left: 25px;
}
.job-description li {
  line-height: 30px;
}
.ybfcare {
  background-color: #fff;
  border-radius: 25px;
  padding: 10px;
  transition: 0.5s;
}
.dovr {
  background-color: #fff;
}
.app-bkgd {
  margin: 0 25px 0 25px;
}
.app-container {
  display: flex;
  justify-content: center;
  align-items: flex-end;
  height: 45vh;
}
.ybfcare:hover {
  background-color: #000e54;
  transition: 0.5s;
}
.ybfcare img {
  height: 200px;
}
.cuse {
  background-color: #222;
  color: #fff;
  text-align: center;
}
.cuse ul {
  list-style: none;
}
.kappathetapi {
  background-color: #222;
  border-radius: 25px;
  padding: 10px;
  transition: 0.5s;
}
.kappathetapi:hover {
  background-color: #fff;
  transition: 0.5s;
}
.kappathetapi img {
  height: 200px;
}
.kappathetapi-text {
  border-radius: 25px;
  background-color: #222;
  color: #fff;
  height: 175px;
  width: 100%;
  margin: 15px;
}
.ddtampabay .job-title {
  padding: 20px 20px 0 20px;
}
.kappathetapi-link {
  text-align: center;
  padding-top: 15px;
  font-weight: 100;
}
.kappathetapi-link a {
  color: #fff;
}
</style>
