<template>
  <v-card
    class="mx-auto"
    max-width="344"
  >
    <v-img
      :src="`${fullInfo.src}`"
      height="350px"
       max-width="344"
       class="card-img-top"
    ></v-img>

    <v-card-title>
     {{fullInfo.title}}
    </v-card-title>

    <v-card-subtitle>
{{fullInfo.des}}
    </v-card-subtitle>

    <v-card-actions>
      <v-btn
        color="success darken-2"
        text
        @click ="handleExplore"
      >
        Explore
      </v-btn>

      <!-- <v-spacer></v-spacer> -->
<!-- 
      <v-btn
        icon
        @click="show = !show"
      >
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn> -->
    </v-card-actions>

  </v-card>
  
</template>

<script>

  export default {
      props:['fullInfo'],
      
    data ()  {

        return {

     
        }
    },
    methods: {
        handleExplore () {
            this.$router.push('/auth/register')
        }
    }

  }
   
</script>