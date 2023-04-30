<script>
import axios from 'axios'
export default {
    data() {
        return {
            email: '',
            password: ''
        }
    },
    methods: {
        async login(event) {
            const resultado = await axios.post('http://localhost:8080/login')
            console.log(resultado);
        }
    }
}
</script>

<template>
    <div class="br-20">
        <div class="mb-3">
            <label for="email" class="form-label">E-mail de Acesso </label>
            <div class="input-group">
                <input class="form-control" type="email" name="email" id="email" placeholder="leonardo@seuprovedor.com"
                    v-model="email">
            </div>

        </div>
        <div class="mb-3">
            <label for="password" class="form-label">Senha: </label>
            <div class="input-group">
                <input class="form-control" type="password" name="password" id="password" v-model="password"
                    placeholder="Senha">
            </div>
        </div>
        <div class="mb-3">
            <button class="btn btn-primary mb-3" @click="login">Acessar</button>
        </div>
    </div>
</template>

<style>
    .corpo-login{
        margin: auto;
    }
</style>

