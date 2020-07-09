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
        font-weight: 400;
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

    @media (max-width: 900px) {
        .splashText {
            font-size: 60px;
        }

        .splash {
            height: 600px;
        }
    }

    @media (max-width: 750px) {
        .splashText {
            font-size: 50px;
        }

        .splash {
            height: 500px;
        }

        .joinButton {
            top: 200px;
        }
    }

    @media (max-width: 650px) {
        .splashText {
            font-size: 40px;
        }

        .splash {
            height: 400px;
        }

        .joinButton {
            top: 150px;
        }
    }

    @media (max-width: 580px) {
        .splashText {
            font-size: 35px;
        }

        .splash {
            height: 350px;
        }

        .joinButton {
            top: 150px;
        }
    }
</style>
