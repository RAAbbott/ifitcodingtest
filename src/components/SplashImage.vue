<template>
  <div class="splash">
      <div class="splashText">
          The best personal training, <br>right in your own home
      </div>
      <span class="joinButton">JOIN IFIT COACH</span>
  </div>
</template>

<script>
export default {

};
</script>

<style scoped>
    .splash {
        height: 801px;
        background: linear-gradient( rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.4) ), url('../assets/gmapsinworkout.png');
        background-size: cover;
    }

    .splashText {
        font-size: 72px;
        color: white;
        top: 25%;
        position: relative;
    }

    .joinButton {
        position: relative;
        top: 260px;
        background-color: #0069D2;
        padding: 20px 140px;
        color: white;
        font-weight: 900;
        cursor: pointer;
        border-radius: 5px;
        transition: font-size 0.2s ease-in-out;
    }

    .joinButton:hover {
        font-size: 14px;
    }
</style>
