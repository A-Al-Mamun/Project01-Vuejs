<template>
    <header>
        <Nav /> 
    </header>
     
    <main>
        <h1>Home Component</h1>  

        <footer>
            <Footer />
        </footer>
    </main>
    
</template>

<script>
import Nav from './NavMenu.vue'
import Footer from './Footer.vue'

export default {
    name: 'Home',
    components: {
        Nav, 
        Footer,
    }
}
</script>

<style scoped>
header{
    width: 100%;
    margin-bottom: 50px;
    padding: 40px 0;
    display: flex;
    justify-content: center;
}
body{
    position: relative;
}
main{
    position: absolute;
    left: 0;
    top: 0;
    background: red;
    width:100%;
    height: 100vh;
    padding-top: 80px;
    z-index: -2;
}
footer{
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
}

</style>