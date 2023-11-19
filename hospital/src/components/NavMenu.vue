<template>
    <div class="menu">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Doctors</a>
        <a href="#">Contact</a>
        <a href="#">Appoinment</a>
    </div>
    <div class="header-btn">
        <Log />
        <a href="#">log In</a>
    </div>
    <i class="fa-solid fa-bars openBar"></i>
    <nav class="menu">
        <i class="fa-solid fa-xmark closeBar"></i>
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
    </nav>   
</template>

<script>
import Log from './Log.vue'
export default {
    name: 'NavMenu',
    component: {
        Log,
    },
    methods: {
        openBtn(){
            let menu = document.getElementsByClassName('menu')[0];
            menu.style.tranform = 'translate(0px)';
        }
    }
}
</script>

<style scoped>
body{
    overflow: hidden;
    position: relative;
}

.menu{
    display: flex;
    flex-direction: row;
}
.menu a{
    display: inline-block;
    padding: 0 10px;
    text-decoration: none;
    color: #000;
    transition: 0.4s;
}
.menu a:hover{
    color: #00000040;
}
.openBar{
    position: absolute;
    top: 30px;
    left: 100px;
    color: #000;
    font-size: 35px;
}
nav{
    position: absolute;
    top: 0;
    left: 0;
    width: 200px;
    height: 100vh;
    background: #000;
    display: flex;
    flex-direction: column;
    align-items: end;
    padding-top: 100px;
    transform: translateX(-200px);
}
nav a{
    display: inline-block;
    color: #fff;
    padding: 10px 30px;
    text-decoration: none;
    transition: 0.4s;
}
nav a:hover{
    color: #ffffff50;
}
nav i{
    position: absolute;
    top: 20px;
    right: 28px;
    color: #fff;
    font-size: 35px;
}
</style>