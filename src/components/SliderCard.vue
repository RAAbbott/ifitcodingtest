<template>
  <div class="card">
      <div class="logo"><img :src="require(`../assets/${this.review.logo}.svg`)" alt="image"></div>
      <div class="text">{{this.review.text}}</div>
  </div>
</template>

<script>
export default {
    props: ['review'],
};
</script>

<style scoped>
    .card {
        min-height: 184px;
        min-width: 440px;
        border: 0.5px solid rgba(0,0,0,0.1);
        background-color: white;
        box-shadow: 0px 1px 2px #aaaaaa;
    }

    .logo {
        margin-top: 45px;
    }

    .text {
        margin-top: 30px;
        padding: 0 70px;
        opacity: .8;
    }
</style>
