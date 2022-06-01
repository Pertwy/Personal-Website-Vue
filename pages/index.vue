<template>
  <div class="app">
      <Nav />
      <HeroSection />


      <h1 class="recent-certifications-header">Recent Certifications</h1>
      <section class="row space-between">
          <Certification 
            v-for = "cert in certifications" 
            :key="cert.id" 
            :id="cert.id" 
            :title="cert.title"
            :image="cert.image"
            :link="cert.link"
          />
        </section>


        <section>
          <Portfolio/>
        </section>

  </div>
</template>

<script>
let id = 0
import Certification from "../components/Certification.vue"
import Portfolio from "../components/Portfolio.vue"
import Nav from "../components/Nav.vue"
import HeroSection from "../components/HeroSection.vue"
export default {
  name: 'IndexPage',
  components: {
    Certification,
    Portfolio,
    Nav,
    HeroSection
},
  methods: {
    toggle() {
      this.showData = !this.showData
    },
  },
  data() {
    return {
      showData: true,
      certifications:[
        {
          id: id++,
          title:"AWS Certified Cloud Practitioner",
          image:"https://images.credly.com/size/680x680/images/68468004-5a85-4f3b-bc58-590773979486/AWS-CloudPractitioner-2020.png",
          link:"https://www.credly.com/badges/85703df6-a110-422d-838c-e7b5c3b5ad35/linked_in",
        },
        {
          id: id++,
          title:"MongoDB A300: Atlas Security",
          image:"https://res.cloudinary.com/startup-grind/image/upload/c_fill,dpr_2,f_auto,g_center,q_auto:good/v1/gcs/platform-data-mongodb/events/mon.png",
          link:"https://university.mongodb.com/course_completion/b03927d1-9235-4c01-ab34-f4aad2452096?utm_source=copy&utm_medium=social&utm_campaign=university_social_sharing",
        },
        {
          id:id++,
          title:"MongoDB M001: MongoDB basics",
          image:"https://res.cloudinary.com/startup-grind/image/upload/c_fill,dpr_2,f_auto,g_center,q_auto:good/v1/gcs/platform-data-mongodb/events/mon.png",
          link:"https://university.mongodb.com/course_completion/4872ae8a-1f73-469c-95ce-3c350676db45?utm_source=linkedin&utm_medium=social&utm_campaign=university_social_sharing"
        }
      ]
    }
  }
}
</script>

<style >
@import url("https://fonts.googleapis.com/css?family=Abril+Fatface|Roboto:300,700");
@import url('https://fonts.googleapis.com/css2?family=Hind:wght@300;500&display=swap');

body {
  font-family: 'Hind', sans-serif;
  font-weight: 300;
  }
  h1, h2, h3, h4, h5, h6 {
    font-family: 'Hind', sans-serif;
    font-weight: 500;
  }

p, h1, h2, h3, h4, h5, h6{
  margin:0px
}
section{
  margin-bottom: 10vh;
}

.app {
  /* text-align: center; */
  margin-left: 10%;
  margin-right: 10%;
}

.space-between{
  display: flex;
  justify-content: space-between;
}
.recent-certifications-header{
  margin-bottom: 15px;
}
.row{
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  /* justify-content: space-around; */
}
.justify-left{
  justify-content: left;
  text-align: left;
}
.center{
  align-items: center;
  text-align: center;
  margin:auto;
  align-content: center;
}
.grid-half{
  display: grid;
  gap: 20px;
  grid-gap: 30px;
  height: 100%;
  grid-template-columns: 1fr 1fr;
}
svg:hover{
  fill: rgb(63, 63, 63);
}
svg{
  height:25px;
  width:25px;
  margin-right:5px
}
@media (max-width: 768px) {
  .grid-half, .grid-three-one, .grid-one-one-one
{
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
  }
  .grid-one-one-one-one{
    grid-template-columns: 1fr 1fr;
  }

}
</style>