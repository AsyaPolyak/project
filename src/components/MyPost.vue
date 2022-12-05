<!-- eslint-disable vue/require-v-for-key -->
<!--import {createApp} from 'vue';-->
<template>
    <div>
        <div class="post" v-for="post in posts">
            <div><strong>Назва:</strong>{{post.title}}</div>
            <div><strong>Опис:</strong>{{post.body}}</div>
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
<style>

</style>