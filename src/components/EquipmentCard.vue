<template>
  <div class="card">
      <div class="logo"><img :src="require(`../assets/avatars/${this.equipment.image}.png`)" alt="image"></div>
      <div class="text">{{this.equipment.text}}</div>
  </div>
</template>

<script>
export default {
    props: ['equipment']
};
</script>

<style scoped>
    .card {
        min-height: 330px;
        min-width: 330px;
        background-color: white;
        box-shadow: 0px 1px 1px #aaaaaa;
        transition: box-shadow 0.3s ease-in-out;
        cursor: pointer;
    }

    .card:hover {
        box-shadow: 0px 5px 5px #aaaaaa;
    }

    .logo {
        margin-top: 45px;
        height: 240px;
    }

    .text {
        font-size: 24px;
        font-weight: bold;
        position: relative;
        bottom: 0;
    }
</style>
