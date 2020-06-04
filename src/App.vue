<template>
  <v-app>
    <NavBar></NavBar>
    <v-content>
      <router-view v-if="isRouterAlive"></router-view>
    </v-content>
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
