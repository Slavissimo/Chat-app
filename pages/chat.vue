<template>
    <body>
        <div id="app">
            <div class="friend-list">
                <List />
            </div>
            <div class="chat-box-site">
                <Chat />
            </div>
        </div>
    </body>
</template>

<script>
import List from "../components/friendlist.vue";
import Chat from "../components/chatbox.vue";

export default {
    components: {
        List,
        Chat
    }
}
</script>

<style>
#app{
    display: flex;
    flex-direction: row;
    width: 100%;
}
.friend-list{
    display: flex;
    width: 20%;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-left: 10px;
    margin-right: 10px;
}
.chat-box-site{
    display: flex;
    width: 79%;
    flex-direction: column;
}
</style>