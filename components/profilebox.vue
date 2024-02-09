<template>
    <div class="profile">
        <div class="profile-pic">
            <span class="circle"></span>
        </div>
        <div class="profile-info">
            <h1 class="username">Username</h1>
            <p class="quote">"Quote"</p>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
.profile{
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-top: 20px;
}
.profile-pic{
    display: flex;
    justify-content: center;
    margin-top: 20px;
}
.circle{
    width: 250px;
    height: 250px;
    border-radius: 50%;
    background-color: #2c2c2c;
    margin-right: auto;
    margin-left: 5%;
}
.username{
    font-size: 32px;
}
.quote{
    font-size: 18px;
    font-style: italic;
}
.profile-info{
    display: flex;
    flex-direction: column;
    margin-left: 20px;
}
</style>