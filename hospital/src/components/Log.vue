<template>
    <div class="log">
        <h1>Log In</h1>
        <input type="text" name="" placeholder="Name"><br>
        <input type="email" name="" placeholder="Email">
        <button>Log In</button>
    </div>
</template>

    
<script>
export default {
    name: 'Log',
}
</script>

    
<style scoped>
body{
    position: relative;
}
.log{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background: red;
}
.log h1{}
.log input{}
.log button{}
</style>
