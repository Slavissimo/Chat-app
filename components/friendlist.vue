<template>
    <div class="list">
        <h1 class="header">Friend List</h1>
        <div class="friend-chat">
            <h2 class="friend-name">Friend 1</h2>
            <p>Message</p>
        </div>
        <div class="friend-chat">
            <h2 class="friend-name">Friend 2</h2>
            <p>Message</p>
        </div>
        <div class="friend-chat">
            <h2 class="friend-name">Friend 3</h2>
            <p>Message</p>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
.list{
    display: flex;
    width: 100%;
    height: 98vh;
    flex-direction: column;
    margin-top: 15px;
    border: 1px solid #ccc;
}
.friend-chat{
    color: white;
    margin: 0;
    border: 1px solid #ccc;
    padding: 10px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 100px;
    width: 100%;
    background-color: #2c2c2c;
    cursor: pointer;
}
.friend-chat:hover{
    background-color: #4c4c4c;
}
.header{
    text-align: center;
    font-size: 28px;
}
.friend-name{
    font-size: 20px;
}
</style>