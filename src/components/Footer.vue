<template>
    <div class="footer">
        {{ msg }}
    </div>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      msg: "Cappy Hoding!"
    };
  }
};
</script>


<style scoped>
.footer {
  height: 60px;
  padding: 10px;
  vertical-align: middle;
  text-align: right;
  width: 100%;
  background-color: rgba(33, 33, 33, 1);
  font-family: "K2D", sans-serif;
  font-size: 24px;
  color: white;
}

.footer::after {
  content: "\258B";
  color: rgb(29, 185, 84);
  animation: blink-animation 1.1s infinite;
  animation-timing-function: ease;
  animation-delay: 0.5s;
  margin-left: 2px;
}
</style>
