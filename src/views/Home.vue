<template>
  <div class="content-area">
    <form>
      <div v-show="step ===1">
        <Basics />
        <button @click.prevent="next()">Next</button>
      </div>
      <div v-show="step ===2">
        <Work />
        <button @click.prevent="next()">Next</button>
        <button @click.prevent="prev()">Previous</button>
      </div>
      <div v-show="step ===3">
        <Volunteer />
        <button @click.prevent="next()">Next</button>
        <button @click.prevent="prev()">Previous</button>
      </div>
      <div v-show="step ===4">
        <Education />
        <button @click.prevent="next()">Next</button>
        <button @click.prevent="prev()">Previous</button>
      </div>
      <div v-show="step ===5">
        <Awards/>
        <button @click.prevent="next()">Next</button>
        <button @click.prevent="prev()">Previous</button>
      </div>
      <div v-show="step ===6">
        <Certificate />
        <button @click.prevent="next()">Next</button>
        <button @click.prevent="prev()">Previous</button>
      </div>
      <div v-show="step ===7">
        <Publications />
        <button @click.prevent="next()">Next</button>
        <button @click.prevent="prev()">Previous</button>
      </div>
      <div v-show="step ===8">
        <Skills />
        <button @click.prevent="next()">Next</button>
        <button @click.prevent="prev()">Previous</button>
      </div>
      <div v-show="step ===9">
        <Languages />
        <button @click.prevent="next()">Next</button>
        <button @click.prevent="prev()">Previous</button>
      </div>
      <div v-show="step ===10">
        <Interests />
        <button @click.prevent="next()">Next</button>
        <button @click.prevent="prev()">Previous</button>
      </div>
      <div v-show="step ===11">
        <Referance />
        <button @click.prevent="next()">Next</button>
        <button @click.prevent="prev()">Previous</button>
      </div>
      <div v-show="step ===12">
        <Project />
        <button @click.prevent="next()">Next</button>
        <button @click.prevent="prev()">Previous</button>
      </div>
      <div v-show="step ===13">
        <CoverLetter />
        <button @click.prevent="next()">Next</button>
        <button @click.prevent="prev()">Previous</button>
      </div>
    </form>
    
  </div>
</template>

<script>
// @ is an alias to /src
import Basics from '../components/FormSteps/Basics.vue';
import Work from '../components/FormSteps/Work.vue';
import Volunteer from '../components/FormSteps/Volunteer1.vue'
import Education from '../components/FormSteps/Education.vue'
import Awards from '../components/FormSteps/Awards.vue'
import Certificate from '../components/FormSteps/Certificate.vue'
import Publications from '../components/FormSteps/Publications.vue'
import Skills from '../components/FormSteps/Skills.vue'
import Languages from '../components/FormSteps/Languages.vue'
import Interests from '../components/FormSteps/Interests.vue'
import Referance from '../components/FormSteps/Referance.vue'
import Project from '../components/FormSteps/Project.vue'
import CoverLetter from '../components/FormSteps/CoverLetter.vue'
export default {
  name: 'Home',
  components: {
    Basics,
    Work,
    Volunteer,
    Education,
    Awards,
    Certificate,
    Publications,
    Skills,
    Languages,
    Interests,
    Referance,
    Project,
    CoverLetter,
  },
  data(){
        return{
            step:1,
        }
    },

    methods:{
        next(){
            this.step++;
        },
        prev(){
            this.step--;
        },
        newProfile(){
            this.profile.push({ network: '',username:'',url:'' });
        },
        removeProfile(k) {
            this.profile.splice(k,1);
        }
        
    }
}
</script>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat&family=Oswald:wght@700&display=swap");

* {
  padding: 0;
  margin: 0;
}


body {
  background-color: #3b4050;
}

h1,h2,h3,h4,p{
  font-family: "Oswald", sans-serif;
}
h1 {
    color: white;
    letter-spacing: 2px;
    padding-top: 60px;
    font-size: xxx-large;
    text-align: center;
}

.content-area {
    margin: 15px;
    background-color: white;
    border-radius: 15px;
    margin-left: 10%;
    width: 80%;
    height: 100%;
    margin-bottom: 20px;
    -webkit-box-shadow: 0 2px 10px 1px rgba(0, 0, 0, 0.5);
    box-shadow: 0 2px 10px 1px rgba(0, 0, 0, 0.5);
}
button {
    margin: 25px;
    padding: 10px 10px;
    outline: 0;
    width: 120px;
    font-size: 14px;
    font-weight: bold;
    text-align: center;
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: .08em;
    background-color: #3b4050;
    border: none;
    color:white;
    border-radius: 10px;
}

button:hover {
    color: rgb(255, 255, 255);
    background: rgb(46, 129, 207);
    border-radius: 10px;
}
</style>