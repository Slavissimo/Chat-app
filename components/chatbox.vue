<template>
    <div class="chat">
        <h1 class="headerchat">Chat</h1>
        <div class="chat-box">
            <div class="chat-message-sent">
                <p>Message</p>
            </div>
            <div class="chat-message-received">
                <p>Message</p>
            </div>
            <div class="chat-message-sent">
                <p>Message</p>
            </div>
        </div>
        <div class="message-input">
            <UInput class="sent-input" placeholder="Write a nice message" />
            <UButton class="button-sent" type="submit"><UIcon name="i-heroicons-paper-airplane-20-solid" /></UButton>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>
.chat{
    display: flex;
    width: 100%;
    flex-direction: column;
    height: 98vh;
}
.headerchat{
    text-align: center;
    font-size: 28px;
}
.message-input{
    display: flex;
    width: 100%;
    margin-top: auto;
}
.sent-input{
    width: 100%;
}
.button-sent{
    margin-left: 5px;
}
.chat-box{
    display: flex;
    width: 100%;
    flex-direction: column;
    overflow-y: auto;
}
.chat-message-sent{
    display: flex;
    width: fit-content;
    height: fit-content;
    padding: 10px;
    border-radius: 30%;
    margin-left: auto;
    background-color: rgb(44, 83, 83);
}
.chat-message-received{
    display: flex;
    width: fit-content;
    height: fit-content;
    padding: 10px;
    border-radius: 30%;
    margin-right: auto;
    background-color: rgb(68, 75, 49);
}
</style>