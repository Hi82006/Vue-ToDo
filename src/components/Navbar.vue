<template>
    <div class="navbar">
        <div @click="$router.push('/')"> Vue 3</div>
        <div class="navbar__btns">
            <my-button @click="$router.push('/posts')">Посты</my-button>
            <my-button @click="$router.push('/about')">О сайте</my-button>
        </div>
        <!-- <router-link to="/posts">Перейти на посты</router-link>
        <router-link to="/about">О сайте</router-link> -->
    </div>
</template>

<script>
import MyButton from './UI/MyButton.vue';
export default {
   
}
</script>

<style scoped>
.navbar {
    height: 50px;
    background-color: rgb(103, 103, 106);
    box-shadow: 2px 2px 4px gray;
    display: flex;
    align-items: center;
    padding:  0 15px;
}
.navbar__btns {
    display: flex;
    margin-left: auto;
    gap: 5px;
}
</style>