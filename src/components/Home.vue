<template>
  <div class="head">
    <profile/>
    <description/>
  </div>
</template>

<script>
import Profile from "./Profile";
import Description from "./Description";

export default {
  name: "Home",
  data() {
    return {
      msg: "Hi! I'm Eko Simanjuntak, Passionate Software Engineer"
    };
  },
  components: {
    Profile,
    Description
  }
};
</script>

<style>
.head {
  background-color: rgba(33, 33, 33, 1);
  display: flow-root;
  padding-bottom: 100px;
}
</style>
