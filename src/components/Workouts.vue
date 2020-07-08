<template>
  <div class="workoutSection">
      <div class="workoutsContainer">
            <WorkoutCard v-for="workout in workouts" :key="workout.text" :workout="workout" class="card"/>
      </div>
      <img src="../assets/slide_right_btn.png" alt="" class="sliderButtonRight">
  </div>
</template>

<script>
import WorkoutCard from './WorkoutCard.vue'

export default {
    data() {
        return {
            workouts: [
                {image: 'img5', text: 'Lake Inniscarra, Ireland--Pyramid', avatar: 'a1', time: '30:53', distance: '6.238 M'},
                {image: 'img1', text: 'Performance Series', avatar: 'a2', workouts: 9},
                {image: 'img6', text: 'Slow Pulls and Fast Intervals', avatar: 'a3', time: '44:13', distance: '9.948 M'},
                {image: 'img2', text: '20 Minutes to Toned', avatar: 'a4', workouts: 12},
                {image: 'img7', text: 'Charles Race, Boston, Massachusetts', avatar: 'a5', time: '36:22', distance: '8.648 M'},
                {image: 'img3', text: 'Full-Body HIIT Series', avatar: 'a6', workouts: 12},
                {image: 'img8', text: 'Kafue River, Zambia--Power Stroke Pyramid', avatar: 'a7', time: '22:22', distance: '4.660 M'},
                {image: 'img4', text: 'Shred & Burn Series', avatar: 'a8', workouts: 16}
            ]
        }
    },

    components: {
        WorkoutCard
    }
};
</script>

<style scoped>
    .workoutSection {
        height: 684px;
        width: 100%;
        overflow-x: auto;
    }

    .workoutsContainer {
        height: 584px;
        width: 1248px;
        margin: auto;
        margin-top: 50px;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: space-around;
        align-content: space-around;
    }

    .card:nth-child(n+5) {
        margin-top: 20px;
    }

    .sliderButtonRight {
        display: none;
    }

    @media (max-width: 1200px){
        .sliderButtonRight {
            position: absolute;
            top: 1450px;
            right: 10px;
            float: right;
            display: block;
        }
    }

    @media (max-width: 900px) {
        .sliderButtonRight {
            top: 1249px;
        }
    }

    @media (max-width: 750px) {
        .sliderButtonRight {
            top: 1149px;
        }
    }

    @media (max-width: 650px) {
        .sliderButtonRight {
            top: 1049px;
        }
    }

    @media (max-width: 580px) {
        .sliderButtonRight {
            top: 999px;
        }
    }
</style>
