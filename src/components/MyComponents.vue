<!--<template>
    <div class="root">
        {{text}}
    </div>
</template>
<script>
export default {
    name: 'MyComponents',
    data() {
        return {
            text: 'hello'
        }
    }
}

</script>
-->
<template>
    <div class="root">
        <label >
            Введіть email:
            <input type="email" v-bind:value="asd">
        </label>
        <label >
            Введіть пароль:
            <input type="password" value="asd">
        </label>
    </div>
</template>
<script>
export default {
    name: 'MyComponents',
    data() {
        return {
            email:'nastia195@gmail.com',
            password: '123455'
        }
    }
}
</script>