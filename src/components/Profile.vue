<template>
  <div class="leftside">
    <v-avatar :size="200" color="grey lighten-4">
      <img class="img-profile" src="../assets/img/ecojuntak.jpeg">
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

h1,
h2 {
  font-weight: normal;
}

.header-text {
  color: rgb(29, 185, 84);
  margin: 30px;
  font-family: "K2D", sans-serif;
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
  padding-top: 150px;
  width: 50%;
  padding-left: 75px;
  padding-right: 75px;
  text-align: center;
  float: left;
  animation: slide 1.2s forwards;
  animation-delay: 0s;
  min-width: inherit;
  background-color: inherit;
}

@media screen and (max-width: 850px) {
  .leftside {
    padding-top: 50px;
    width: 100%;
    padding-left: 75px;
    padding-right: 75px;
    text-align: center;
    float: left;
    animation: slide 1.2s forwards;
    animation-delay: 0s;
    background-color: inherit;
  }
}

@-webkit-keyframes slide {
  0% {
    transform: translateY(-100%);
  }
  100% {
    transform: translateY(0);
  }
}

@keyframes slide {
  0% {
    transform: translateY(-100%);
  }
  100% {
    transform: translateY(0);
  }
}

.icon {
  color: white;
}

.icon :hover {
  color: rgb(29, 185, 84);
}

.img-profile {
  border: 5px;
  border-color: antiquewhite;
}
</style>
