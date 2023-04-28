<template>
    <div>
        <input type="email" name="email" id="email" placeholder="joao@teste.com" v-model="email">
    </div>
    <div>
        <input type="password" name="password" id="password" v-model="password">
    </div>
    <button @click="login">Entrar</button>
</template>

<script>
export default{
    data() {
        return {
            email: '',
            password: ''
        }
    },
    methods: {
        login(event) {
            console.log(this.email)
        }
    }
}
</script>