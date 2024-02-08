<template>
    <body>
        <div id="app">
            <div class="login-box">
                <div class="login-form">
                    <Register />
                </div>
            </div>
        </div>
    </body>
</template>

<script>
import Register from "../components/register.vue";

export default {
    components: {
        Register
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
    align-items: center;
    justify-content: center;
    height: 100%;
}
</style>