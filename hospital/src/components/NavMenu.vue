<template>
    <div class="menu">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Doctors</a>
        <a href="#">Contact</a>
        <a href="#">Appoinment</a>
    </div>
    <div class="header-btn">
        <a v-on:click="show=!show" href="#" id="login-btn">{{ data.name }}</a>
        <div v-if="show" class="log-active">
            <img src="../assets/logo.png" alt="">
            <h3>Log In</h3>
            <form action="#">
                <input v-model="email" type="email" name="email" placeholder="Enter email">
                <input v-model="pass" type="password" name="pass" placeholder="Enter password">
                <input type="submit" v-on:click="myLoginFunction()" name="sub" value="Log In">
            </form>
        </div>
    </div>
    <i class="fa-solid fa-bars openBar" v-on:click="myNavFunction()"></i>
    <nav id="menu2">
        <i class="fa-solid fa-xmark closeBar"></i>
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
    </nav>   
</template>

<script>
export default {
    name: 'NavMenu',
    props:{
        data:String,
    },
    component: {
        
    },
    data(){
        return{
            email: null,
            pass: null,
            show: false,
        }
    },
    methods: {
        myNavFunction(){
            let nav = document.getElementById('menu2');
            let closeNav = document.getElementsByClassName('closeBar')[0];
            nav.style.display = 'flex';
            closeNav.addEventListener('click', () => {
                nav.style.display = 'none';
            })
        },
        myLoginFunction(){
            let loginBtn = document.getElementById('login-btn');
            if((this.email == 'admin@gmail.com')&&(this.pass == 'admin')){
                loginBtn.innerText = 'Admin';
                let active = document.querySelector('.log-active');
                active.style.display = 'none';
            }else{
                alert('Not Matched the user and password');
            }
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
    display: none;
    flex-direction: column;
    align-items: end;
    padding-top: 100px;
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


.log-active{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background: #00000050;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}
.log-active h3{
    color: #fff;
}
.log-active form{
    display: flex;
    flex-direction: column;
}
.log-active form input{
    width:300px;
    font-size: 30px;
    padding: 5px;
    margin: 10px 0;
}
.log-active form input[type=submit]{
    background: #000;
    color: #fff;
}
</style>