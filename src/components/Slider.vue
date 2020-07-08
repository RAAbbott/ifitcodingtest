<template>
    <div>
        <img src="../assets/slide_left_btn.png" alt="" class="sliderButtonLeft">
        <div class="sliderContainer">
            <SliderCard class="card" v-for="review in reviews" :key="review.text" :review="review"/>
        </div>
        <img src="../assets/slide_right_btn.png" alt="" class="sliderButtonRight">
    </div>
</template>

<script>
import SliderCard from './SliderCard.vue';

export default {
    data() {
        return {
            reviews: [
                {logo: 'mashable-logo', text: '"Breathes new life into a tired, old running routine"'},
                {logo: 'wired-logo', text: '"Literally transports you from home to wherever you choose to run"'},
                {logo: 'gear-junkie-logo', text: '"You focus on putting in the work, and the technology handles the rest"'},
                {logo: 'mashable-logo', text: '"Breathes new life into a tired, old running routine"'},
                {logo: 'wired-logo', text: '"Literally transports you from home to wherever you choose to run"'}
            ]
        }
    },

    components: {
        SliderCard
    },

    methods: {
        nextReview() {

        },

        previouseReview() {

        }
    }
};
</script>

<style scoped>
    .img {
        display: inline; 
    }

    .sliderContainer {
        background-color: #F4F5F7;
        height: 232px;
        overflow: hidden;
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        justify-content: space-around;
        margin-top: -10px;
    }

    .card {
        margin: 25px 15px;
        float: left;
    }

    .sliderButtonRight {
        position: relative;
        bottom: 40px;
        margin-top: -100px;
        float: right;
    }

    .sliderButtonLeft {
        position: relative;
        top: 90px;
        margin-bottom: -140px;
        float: left;
    }
</style>
