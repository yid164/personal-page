<template>
  <div class="home">
    <HomeComp></HomeComp>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeComp from "@/components/HomeComp";

export default {
  name: 'Home',
  components: {
    HomeComp
  }
}
</script>
