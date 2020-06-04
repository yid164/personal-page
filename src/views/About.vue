<template>
  <div class="about">
    <AboutComp></AboutComp>
  </div>
</template>

<script>
  // @ is an alias to /src
  import AboutComp from "@/components/AboutComp";

  export default {
    name: 'Home',
    components: {
      AboutComp
    }
  }
</script>
