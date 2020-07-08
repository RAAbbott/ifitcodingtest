<template>
  <div class="equipmentSection">
      <span class="text">Interested in our exciting iFit-enabled equipment?</span>
      <div class="equipmentContainer">
          <EquipmentCard v-for="item in equipment" :key="item.text" :equipment="item" class="card"/>
      </div>
      <img src="../assets/slide_right_btn.png" alt="" class="sliderButtonRight">
  </div>
</template>

<script>
import EquipmentCard from './EquipmentCard.vue';

export default {
    data() {
        return {
            equipment: [
                {image: 'treadmill', text: 'Treadmills'},
                {image: 'bike', text: 'Bikes'},
                {image: 'eliptical', text: 'Elipticals'},
                {image: 'pulley', text: 'Strength'},
            ]
        }
    },

    components: {
        EquipmentCard
    }
};
</script>

<style scoped>
    .equipmentSection {
        height: 450px;
    }

    .equipmentContainer {
        display: flex;
        flex-direction: row;
        max-width: 1400px;
        justify-content: space-between;
        margin: auto;
        margin-top: 10px;
        padding: 10px;
        overflow-x:auto;
    }

    .text {
        font-size: 24px;
        opacity: .8;
    }

    .sliderButtonRight {
        display: none;
    }

    @media (max-width: 1200px){
        .sliderButtonRight {
            position: absolute;
            top: 2020px;
            right: 10px;
            float: right;
            display: block;
        }
    }


    @media (max-width: 900px) {
        .sliderButtonRight {
            top: 1819px;
        }
    }

    @media (max-width: 750px) {
        .sliderButtonRight {
            top: 1719px;
        }
    }

    @media (max-width: 650px) {
        .sliderButtonRight {
            top: 1619px;
        }
    }

    @media (max-width: 580px) {
        .sliderButtonRight {
            top: 1569px;
        }

        .text {
            font-size: 20px;
        }
    }
</style>
