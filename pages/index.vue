<template>
  <div>

<Slider />
<h1 class="header-doctors">OUR DOCTORS</h1>
<div class="doctorsCards d-flex" >
<Card class="mt-10 ms-6 mx-auto"
 v-for ="infos in doctorsInfo"
  :key="infos.id" 
  :fullInfo="infos"
  />
</div>
<h1 class="header-doctors">Appointments</h1>
<Form/>

  </div>
</template>

<script>
import Navbar from "../components/header/Navbar.vue";
import Slider from "../components/Slider.vue";
import Card from "../components/Card.vue";
import data from "../assets/Data";
import Form from "../components/forms/Form.vue";
import Footer from "../components/footer/Footer.vue";

  export default {
    components: { Navbar, Slider, Card, Form, Footer },

    data() {
      return {
        doctorsInfo: data
      }
    }
}
</script>

<style  >
.header-doctors{
  text-align: center;
  font-weight: bold;
  color: #00d9a5;
  display: flex;
  justify-content: center;
  border-bottom: solid;
  width: 40%;
  align-items: center;
  margin: 2em auto;
  padding-bottom: 0.5em;
}
@media screen and (max-width: 820px){
  .doctorsCards{
    justify-content: center;
    align-items: center;
  }
}
</style>