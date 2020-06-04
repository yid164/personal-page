<template>
  <v-app>
    <div class="app">
      <NavBar></NavBar>
      <v-content>
        <router-view v-if="isRouterAlive"></router-view>
      </v-content>
    </div>
  </v-app>
</template>

<script>
  import NavBar from "@/components/NavBar";
  export default {
    name: 'App',

    provide(){
      return{
        reload: this.reload,
      }

    },

    components: {
      NavBar
    },

    data(){
      return{
        isRouterAlive: true
      }
    },

    methods:{
      reload(){
        this.isRouterAlive = false;
        this.$nextTick(function () {
          this.isRouterAlive = true
        })
      }
    },
  };
</script>

<style scoped>
  .app {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background: url("https://bs-uploads.toptal.io/blackfish-uploads/uploaded_file/file/53369/image-1568763265231-74e7c5e8b8b8efa17e1ba52b5107e140.gif") no-repeat center center;
    background-size: cover;
  }
</style>
