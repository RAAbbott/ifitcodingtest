<template>
  <div class="footer">
      <div class="links">
          <div class="column">
            <div class="header">Company</div>
            <div>About</div>
            <div>Contact Us</div>
            <div>Careers</div>
          </div>
           <div class="column">
            <div class="header">Account</div>
            <div>Log In</div>
            <div>Create Account</div>
          </div>
          <div class="column">
            <div class="header">Support</div>
            <div>Help Center</div>
            <div>Accessibility</div>
          </div>
      </div>
      <div class="social">
          <img src="../assets/Social/Social Media/youtube.png" alt="">
          <img src="../assets/Fill-16-path.png" alt="">
          <img src="../assets/Social/Social Media/pinterest.png" alt="">
          <img src="../assets/Fill-16-path.png" alt="">
          <img src="../assets/Social/Social Media/facebook.png" alt="">
          <img src="../assets/Fill-16-path.png" alt="">
          <img src="../assets/Social/Social Media/twitter.png" alt="">
          <img src="../assets/Fill-16-path.png" alt="">
          <img src="../assets/Social/Social Media/instagram.png" alt="">
          <img src="../assets/Fill-16-path.png" alt="">
      </div>
      <div class="bottom">
          <div class="language" @click="toggleDropdown">{{language}} <img src="../assets/avatars/line.png" alt=""></div>
          <div ref="dropdown" class="dropdown" :style="{'display': isDropdownOpen ? '' : 'none'}">
              <ul>
                  <li v-for="item in languages" :key="item" @click="setLanguage(item)">{{item}}</li>
              </ul>
          </div>
          <div class="copyright">
              <span>© iFit.com All Rights Reserved.</span>
              <span>Privacy Policy</span>
              <span>Terms and Conditions</span>
          </div>
          <div></div>
      </div>
  </div>
</template>

<script>
import { EventBus as bus } from '../shared/eventBus.js';

export default {
    data() {
        return {
            language: 'English',
            languages: ['English', 'Spanish', 'Dutch', 'Spanglish', 'Español'],
            isDropdownOpen: false
        }
    },

    methods: {
        toggleDropdown() {
            this.isDropdownOpen = !this.isDropdownOpen;
        },

        setLanguage(val) {
            this.language = val;
        }
    },

    created() {
        bus.$on('bodyClick', (event) => {
            this.isDropdownOpen = event.target.classList.value.includes('language') ? true : false;
        })
    }
};
</script>

<style scoped>
    .footer {
        height: 348px;
        border: solid black 1px;
        background-color: #2E3134;
        color: white;
        font-size: 14px;
    }

    .links {
        height: 208px;
        width: 950px;
        margin: auto;
        text-align: justify;
    }

    .column {
        float: left;
        width: 33%;
        margin-left: 0px;
        margin-top: 25px;
    }

    .column:last-child {
        width: 10%;
    }

    .column:first-child {
        margin-left: 120px;
    }

    .column div:not(:first-child) {
        margin-top: 15px;
        opacity: .7;
    }

    .social {
        height: 76px;
        border-bottom: solid rgba(255, 255, 255, 0.8) .5px;
        border-top: solid rgba(255, 255, 255, 0.8) .5px;
    }

    .social img {
        margin: 15px 8px;
    }

    .social img:nth-child(odd) {
        margin-bottom: 25px;
        position:relative;
        left: 40px;
    }

    .social img:first-child {
        margin-bottom: 28px;
    }

    .social img:nth-child(odd):not(:nth-child(5)) {
        left: 46px;
    }

    .header {
        font-weight: bolder;
    }

    .bottom {
        margin-top: 20px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }

    .language {
        margin-left: 20px;
        cursor: pointer;
    }

    .language img {
        margin-left: 20px;
    }
    
    .dropdown {
        position: fixed;
        bottom: 50px;
        text-align: left;
        border: solid white 1px;
        background-color: rgb(110, 110, 110);
    }

    .dropdown ul{
        list-style-type: none;
        margin-right: 40px;
    }

    .dropdown ul li {
        padding: 5px 0 5px 0;
        border-bottom: solid white 1px;
        cursor: pointer;
        transition: font-size 0.2s ease-in-out;
    }

    .dropdown ul li:hover {
        font-size: 16px;
    }

    .copyright span{
        margin-right: 20px;
    }

    .copyright span:first-child {
        margin-left: -60px;
    }
</style>
