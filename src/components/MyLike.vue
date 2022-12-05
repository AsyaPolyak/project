<template>
    <div class="root">
        <button @click="addLikes">likes</button>
        <button @click="addDislikes">dislikes</button>
        <div>Кіл-сть лайків <strong>{{likes}}</strong></div>
        <div>Кіл-сть дізлайків<strong>{{dislikes}}</strong></div>
    </div>
</template>
<script>
export default{
    data() {
        return {
            likes:0,
            dislikes:5,
        }
    },
    methods: {
        addLikes() {
            this.likes+=1;
        },
        addDislikes() {
            this.dislikes+=1;
        }
    }
}
</script>

<style>
</style>