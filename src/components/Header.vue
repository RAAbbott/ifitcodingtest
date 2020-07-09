<template>
    <div class="header">
        <div class="buttons">
            <span class="button"><span class="text">BLOG</span></span>
            <span class="button"><span class="text">NOURISH</span></span>
            <span class="button"><span class="text">SHOP</span></span>
        </div>
        <div class="menu">
            <div class="logo">
                <img src="../assets/ifit-coach-logo.svg" alt="iFit Logo">
            </div>
            <div class="menuItems">
                <span class="menuItem">EXERCISE</span>
                <span class="menuItem">NUTRITION</span>
                <span class="menuItem">ACTIVITY</span>
                <span class="menuItem">SLEEP</span>
            </div>
            <div class="signUp">
                <span class="signUpButton">SIGN UP</span>
            </div>
        </div>
        <div class="small-menu">
            <div class="logo">
                <img src="../assets/ifit-coach-logo.svg" alt="iFit Logo">
            </div>
            <div class="dropdown-menu" @click="showMenu = true;">
                <img src="../assets/menu2.png" alt="" class="dropdown-img">
            </div>
        </div>
        <div class="popout-menu" :style="{display: showMenu ? '' : 'none'}">
            <span class="close" @click="showMenu = false">
                <img src="../assets/close2.png" alt="">
            </span>
            <div class="options">
                <span class="option">EXERCISE</span>    
                <span class="option">NUTRITION</span>
                <span class="option">ACTIVITY</span>
                <span class="option">SLEEP</span>
                <div class="signUp">
                    <span class="signUpButton">SIGN UP</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { EventBus as bus } from '../shared/eventBus.js';

export default {
    data() {
        return {
            showMenu: false,
        }
    },

    created() {
        bus.$on('bodyClick', (event) => {
            this.showMenu = event.target.classList.value.includes('dropdown-img') || event.target.classList.value.includes('popout-menu') || event.target.classList.value.includes('option');
        })
    },

    watch: {
        showMenu() {
            if (this.showMenu) {
                document.documentElement.style.overflow = 'hidden'
                document.documentElement.style.opacity = 0.7;
                return;
            }

            document.documentElement.style.overflow = 'auto';
            document.documentElement.style.opacity = 1;
        }
    }
};
</script>

<style scoped>
    .buttons {
        width: 100%;
        height: 47px;
        display: flex;
        flex-direction: row;
        border-bottom: solid rgba(0, 0, 0, 0.548) 0.4px;
        border-top: solid rgba(0, 0, 0, 0.548) 0.4px;
    }

    .button {
        border-right: solid rgba(0, 0, 0, 0.548) 0.4px;
        cursor: pointer;
    }
    
    .button:nth-child(1) {
        width: 122px;
    }

    .button:nth-child(2) {
        width: 150px;
    }

    .button:last-child {
        width: 124px;
    }

    .text {
        position: relative;
        top: 14px;
        text-decoration: none;
        color: inherit;
        transition: font-size 0.2s ease-in-out;
    }
    
     .text:hover {
        font-size: 15px;
    }

    .menu {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-content: space-between;
        height: 72px;
        border-bottom: solid rgba(0, 0, 0, 0.548) 0.4px;
    }

    .small-menu {
        display: none;
    }

    .popout-menu {
        display: none;
    }

    .logo {
        position: relative;
        top: 23px;
        margin-left: 23px;
    }

    .menuItems {
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        width: 387px;
        margin-right: 5%;
    }

    .menuItem {
        margin: 0 20px 0 20px;
        position: relative;
        top: 26px;
        cursor: pointer;
        transition: font-size 0.2s ease-in-out;
    }

    .menuItem:hover {
        font-size: 15px;
    }

    .signUpButton {
        background-color: #0069D2;
        padding: 8px 15px;
        color: white;
        font-weight: 900;
        position: relative;
        top: 26px;
        cursor: pointer;
        margin-right: 23px;
        border-radius: 5px;
        transition: font-size 0.2s ease-in-out;
    }

    .signUpButton:hover {
        font-size: 14px;
    }

    @media (max-width: 1000px) {
        .small-menu {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            align-content: space-between;
            height: 72px;
            border-bottom: solid rgba(0, 0, 0, 0.548) 0.4px;
        }

        .signUpButton {
            margin-left: 25px;
        }

        .dropdown-menu {
            margin-top: 18px;
            margin-right: 18px;
            cursor: pointer;
        }

        .menu {
            display: none;
        }

        .popout-menu {
            display: block;
            height: 120%;
            width: 40%;
            position: absolute;
            background-color: white;
            z-index: 1010;
            top: 0;
            right: 0;
            border-left: solid rgba(0, 0, 0, 0.548) 0.4px;
        }

        .popout-menu .options {
            margin-top: 100px;
            font-size: 18px;
            font-weight: bold;
        }

        .popout-menu .options span{
            margin-top: 40px;
            display: block;
            transition: font-size .2s ease-in-out;
            cursor: pointer;
        }

        .popout-menu .options span:hover {
            font-size: 22px;
        }

        .close {
            cursor: pointer;
            float: right;
            margin-right: 40px;
            margin-top: 20px;
        }
    }
</style>
