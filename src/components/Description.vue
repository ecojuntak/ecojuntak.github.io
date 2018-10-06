<template>
    <div class="rightside">
        <p v-for="desc in descriptions" v-html="desc"> </p>
        <br><br>

        <p class="cappy"> Cappy Hoding! </p>
    </div>
</template>

<script>
export default {
  name: "Description",
  data() {
    return {
      descriptions: [
        "<b> I'm student at Del Institute of Technology. Previously I work as Full Stack Software Engineer Intern at GO-JEK. </b>",
        "I am a curious learner specially about new technology. I spend my time to read articles and tutorials everyday. I also challenge my self to learn new stuff.",
        "I love to write code. I write code for my study and my self improvement. I also write code and blog to share what I had learned. I love to connect to new people that I can work and learn with. If you love to share something to me, feel free to reach me."
      ]
    };
  }
};
</script>

<style scoped>
.rightside {
  padding-top: 150px;
  width: 50%;
  padding-right: 100px;
  text-align: center;
  color: white;
  float: right;
  animation: slide 1.2s forwards;
  animation-delay: 0s;
  background-color: inherit;
}

@media screen and (max-width: 850px) {
  .rightside {
    padding-top: 20px;
    width: 100%;
    padding-left: 75px;
    padding-right: 75px;
    text-align: center;
    color: white;
    float: right;
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

p {
  color: whitesmoke;
  font-size: 18px;
  font-family: "K2D", sans-serif;
  line-height: 25px;
  text-overflow: unset;
  text-align: left;
}

.cappy::after {
  content: "\258B";
  color: rgb(29, 185, 84);
  animation: blink-animation 1.1s infinite;
  animation-timing-function: ease;
  animation-delay: 0.5s;
  margin-left: 2px;
}
</style>
