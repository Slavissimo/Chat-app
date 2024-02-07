<template>
    <head>
        <title>Vue.js</title>
    </head>
    <body>
        <div id="app">
            <div class="login-box">
                <div class="login-form">
                    <Login />
                </div>
            </div>
        </div>
    </body>
</template>

<script>
import Login from "/components/login.vue";

export default {
    components: {
        Login
    }
}
</script>
<style scoped>
#app{
    display: flex;
    align-items: center;
    justify-content: center;
    height: 98vh;
}
.login-box{
    width: 30%;
    height: 60vh;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
}
.login-form{
    display: flex;
    width: 100%;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
}
</style>