<template>
  <v-carousel hide-delimiters cycle   >
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
 style="opacity: .7;"
    >
       <v-row
          class="fill-height"
          align="center"
          justify="center"
          
        >
          <div class="slider-content-details">
          <h1 style="color:black">Explore More</h1>
          <button class="slider-btn" @click="btnClicked">Explore Now</button>
          </div>
        </v-row>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://images.unsplash.com/photo-1576091160550-2173dba999ef?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80',
          },
          {
            src: 'https://images.unsplash.com/photo-1581594549595-35f6edc7b762?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80',
          },
          {
            src: 'https://images.unsplash.com/photo-1579165466991-467135ad3110?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80',
          },
          {
            src: 'https://images.unsplash.com/photo-1601055283742-8b27e81b5553?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80',
          },
        ],
      }
    },
    methods: {
      btnClicked() {
        this.$router.push ('/seller')
      }
    }
  }
</script>
<style >
 .slider-content-details .slider-btn{
  background: #00d9a5 !important;
  padding: .7em 1em;
  border-radius: 10px;
}
</style>