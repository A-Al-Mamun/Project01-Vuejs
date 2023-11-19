<template>
    <header>
        <Nav /> 
    </header>
     
    <h1>Home Component</h1>  
    <footer>
        <Footer />
    </footer>
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

<style>
header{
    width: 100%;
    margin-bottom: 50px;
    padding: 40px 0;
    display: flex;
    justify-content: center;
}

</style>