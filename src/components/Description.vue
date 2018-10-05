<template>
    <div class="leftside">
        <p v-for="desc in descriptions" v-html="desc"> </p>
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
        "I love to write code. I write code for my study and my self improvement. I also write code and blog to share what I had learned. I love to connect to new people that I can work and learn with. If you love to share something to me, feel free to reach me.",
        "<br><br> Cappy Hoding!",
      ]
    };
  }
};
</script>

<style scoped>
.leftside {
  width: 50%;
  padding-right: 100px;
  text-align: center;
  float: right;
}

p {
  color: grey;
  font-size: 18px;
  font-family: 'Noto Sans KR', sans-serif;
  line-height: 25px;
  text-overflow: unset;
  text-align: left;
}

</style>
