<template>
    <div class="profile-header">
        <h1>Profile</h1>
    </div>
    <div>
        <Profile />
    </div>
</template>

<script>
import Profile from '../components/profilebox.vue';
export default {
    components: {
        Profile
    }
}
</script>

<style>
.profile-header{
    display: flex;
    width: 100%;
    justify-content: center;
    font-size: 40px;
}
</style>