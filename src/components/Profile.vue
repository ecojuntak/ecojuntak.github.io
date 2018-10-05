<template>
  <div class="leftside">
    <v-avatar :size="200" color="grey lighten-4">
      <img src="../assets/ecojuntak.jpeg">
    </v-avatar>

    <h1 class="header-text" v-html="msg"></h1>

    <v-layout justify-space-around>
      <ul>
        <li v-for="social in socials">
          <a :href=social.url target="_blank" >
            <v-icon class="icon" :name=social.icon scale="2"/>
          </a>
        </li>
      </ul>
    </v-layout>

    <v-divider vertical></v-divider>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Hi! I'm Eko Simanjuntak, <br> a Passionate Software Engineer",
      socials: [
        {
          url: "mailto:ecojuntak@gmail.com",
          icon: "regular/envelope"
        },
        {
          url: "https://linkedin.com/in/ecojuntak",
          icon: "brands/linkedin"
        },
        {
          url: "https://github.com/ecojuntak",
          icon: "brands/github"
        },
        {
          url: "https://gitlab.com/ecojuntak",
          icon: "brands/gitlab"
        },
        {
          url: "https://facebook.com/ecojuntak",
          icon: "brands/facebook"
        },
        {
          url: "https://twitter.com/cappyhoding",
          icon: "brands/twitter"
        },
        {
          url: "https://medium.com/@ecojuntak",
          icon: "brands/medium"
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

.header-text {
  color: #1e7ddd;
  margin: 30px;
  font-family: 'Noto Sans KR', sans-serif;
}

ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}

.leftside {
  width: 50%;
  padding-left: 75px;
  padding-right: 75px;
  text-align: center;
  float: left;
}

.icon {
  color: #1e7ddd;
}

</style>
