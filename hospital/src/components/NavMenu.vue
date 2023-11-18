<template>
    <i class="fa-solid fa-bars openBar" v-on="openBtn"></i>
    <nav class="menu">
        <i class="fa-solid fa-xmark closeBar"></i>
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
    </nav>   
</template>

<script>
export default {
    name: 'NavMenu',
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