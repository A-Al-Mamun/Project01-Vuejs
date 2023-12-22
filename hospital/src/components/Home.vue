<template>
    <header>
        <Nav />
    </header>

    <main>

        <div class="reuse">
            <ul>
                <li v-for="item in user" :key="item">
                    <img v-bind:src="item.url">
                </li>
            </ul>
        </div>
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
    },
    data() {
        return {
            name: "Mamun",
            user: [{
                    email: "admin@gmail.com",
                    name: "admin",
                    url: "../assets/logo.png"
                },
                {
                    email: "user@gmail.com",
                    name: "user"
                },
            ]
        }
    },
    methods: {

    }
}
</script>

<style scoped>
header {
    width: 100%;
    margin-bottom: 50px;
    padding: 40px 0;
    display: flex;
    justify-content: center;
}

body {
    position: relative;
}

main {
    position: absolute;
    left: 0;
    top: 0;
    background: rgba(165, 22, 153, 0.76);
    width: 100%;
    height: 100vh;
    padding-top: 80px;
    z-index: -2;
}

footer {
    position: absolute;
    bottom: 5px;
    left: 0;
    width: 100%;
}
</style>
