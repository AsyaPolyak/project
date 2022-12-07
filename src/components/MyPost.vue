<!-- eslint-disable vue/require-v-for-key -->
<!--import {createApp} from 'vue';-->
<template>
    <div class="app">
            <form >
                <h1>Створити пост</h1>
                <input class="input" type="text" placeholder="post">
                <input class="input" type="text" placeholder="post">
                <button class="btn">Створити</button>
            </form>
        
        <div class="post" v-for="post in posts">
            <div><strong>Назва:</strong>{{post.title}}</div>
            <div><strong>Опис:</strong>{{post.body}}</div>
            <button> </button>
        </div>
    </div>
</template>
<script>
export default {
    data () {
        return {
            posts: [
                {id:1, title:'Java Script',body:'Опис поста'},
                {id:2, title:'Java',body:'Опис поста'},
                {id:3, title:'Python',body:'Опис поста'}
        ]
        }
    }
}
</script>
<style scoped>
*{
    margin:0;
    padding: 0;
    box-sizing: border-box;
}
.app {
    padding: 20px;
}
.post {
    padding: 15px;
    border: 2px solid teal;
    margin-top: 15px;

}
form {
    display: flex;
    flex-direction: column;
}
.input{
    width:100%;
    border: 1px solid teal;
    padding: 10px 15px;
    margin-top:15px;
}
.btn {
    align-self: flex-end;
    margin-top: 15px;
    padding: 10px 15px;
    background:none;
    border: 2px solid teal;
    color: teal;
}
</style>