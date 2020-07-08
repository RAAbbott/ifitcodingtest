<template>
  <div class="card">
      <div class="logo"><img :src="require(`../assets/avatars/${this.workout.image}.png`)" alt="image" class="mainImage"></div>
      <div v-if="this.workout.workouts" class="mask">
          <div>{{this.workout.workouts}}</div>
          <div>WORKOUTS</div>
          <img src="../assets/avatars/workouts_icon.svg" alt="workout icon" class="icon">
      </div>
      <div class="body">
          <span class="header">
              {{this.workout.text}}
          </span>
          <span class="avatar">
              <img :src="require(`../assets/avatars/${this.workout.avatar}.png`)" alt="avatar">
          </span>
          <div v-if="this.workout.time" class="timeAndDistance">
              <img src="../assets/avatars/icn_timer_line.png" alt="timer"><span>{{this.workout.time}}</span><img src="../assets/avatars/icn_distance_line.png" alt="timer"><span> {{this.workout.distance}}</span>
          </div>
          <div :class="{'details': true, 'bottom': !this.workout.time}">
              <span href="https://google.com">VIEW DETAILS</span>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    props: ['workout'],


};
</script>

<style scoped>
    .card {
        min-height: 280px;
        min-width: 278px;
        border: 0.5px solid rgba(0,0,0,0.1);
        background-color: white;
        box-shadow: 0px 0px 1px #aaaaaa;
        transition: box-shadow 0.3s ease-in-out;
    }

    .card:hover {
        box-shadow: 0px 5px 5px #aaaaaa;
    }

    .card:hover .details {
        display: block;
    }

    .mask {
        width: 112px;
        height: 164px;
        background-color: rgba(0, 12, 40, 0.596);
        z-index: 1000;
        position: relative;
        top: -169px;
        margin-bottom: -164px;
        left: 176px;
        color: white;
        font-weight: bold;
    }

    .mask div:first-child {
        padding-top: 45px;
        font-size: 16px;
    }

    .mask div:nth-child(2) {
        font-size: 10px;
        padding-top: 10px;
    }

    .icon {
        padding-top: 15px;
        padding-left: 5px;
    }

    .timeAndDistance {
        float: left;
        width: 100%;
    }

    .body {
        margin-top: 10px;
        text-align: left;
        margin-left: 10px;
        width: 278px;
    }

    .header {
        font-weight: bold;
        font-size: 16px;
        float: left;
        width: 220px;
        line-height: 18px;
    }

    .avatar {
        float: right;
        margin-right: 15px;
    }

    .details {
        display: none;
        z-index: 1000;
    }

    .details span {
        position: relative;
        top:10px;
        color: #0069D2;
        font-weight: bold;
        transition: font-size 0.2s ease-in-out;
        cursor: pointer;
    }

    .details span:hover {
        font-size: 15px;
    }

    .bottom {
        position: relative;
        top: 32px;
    }

    .timeAndDistance img {
        margin-right: 5px;
        margin-top: 5px;
    }

    .timeAndDistance img:nth-child(3) {
        margin-left: 6px;
    }
</style>
