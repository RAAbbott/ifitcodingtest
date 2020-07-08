<template>
    <div class="header">
        <div class="buttons">
            <span class="button"><a href="https://www.google.com" target="_blank" class="text">BLOG</a></span>
            <span class="button"><a href="https://www.google.com" target="_blank" class="text">NOURISH</a></span>
            <span class="button"><a href="https://www.google.com" target="_blank" class="text">SHOP</a></span>
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
    </div>
</template>

<script>
export default {

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
</style>
