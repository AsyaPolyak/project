<!-- eslint-disable vue/require-v-for-key -->
<!--import {createApp} from 'vue';-->

<template>
    <div class="app">
            <form @submit.prevent>
                <h1>Створити пост</h1>
                <!-- 
                  v-bind:value="title"
                  @input="title = $event.target.value"  
                -->
                <input
                  v-model="title"
                  class="input"
                  type="text"
                  placeholder="post"
                >
                <!-- 
                  v-bind:value="body"
                  @input="body = $event.target.value" 
                -->
                <input
                  v-model="body"
                  class="input"
                  type="text"
                  placeholder="post"
                >
                <my-button 
                  @click="createPost">
                    Створити
                </my-button>
            </form>
        
        <div class="post" v-for="post in posts">
            <div><strong>Назва:</strong>{{post.title}}</div>
            <div><strong>Опис:</strong>{{post.body}}</div>
            <my-button >Видалити</my-button>
        </div>
    </div>
</template>
<script>
//import MyButton from './UI/MyButton.vue'
export default {

    data () {
        return {
            posts: [
                {id:1, title:'Java Script',body:'Опис поста'},
                {id:2, title:'Java',body:'Опис поста'},
                {id:3, title:'Python',body:'Опис поста'}
            ],
            title: '',
            body:  ''
        }
    },
    methods: {
        createPost() {
            const newPost ={
                id: Date.now(),
                title:this.title,
                body:this.body
            }
            this.posts.push(newPost);
            //this.$emit('create', this.post);
            //this.post = {this.title = '',this.body = ''}
            this.title = '',
            this.body = ''
        },
    }/*,
    components: {
        MyButton
    }*/
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