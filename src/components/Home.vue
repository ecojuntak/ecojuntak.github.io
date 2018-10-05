<template>
  <div class="home">
    <profile/>
    <description/>
  </div>
</template>

<script>
import Profile from './Profile'
import Description from './Description'

export default {
  name: "Home",
  data() {
    return {
      msg: "Hi! I'm Eko Simanjuntak, Passionate Software Engineer",
    };
  },
  components: {
      Profile,
      Description
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .home {
        margin-top: 150px;
    }
</style>
