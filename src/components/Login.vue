<script>
export default {
    name: "Login",
    data() {
        return {
            email: "",
            senha: ""
        }
    },
    methods: {
  
        emitLogin() {
            
            console.log("Email: " + this.email);
            this.$emit("login", this.email);
        },
    }
}
</script>

<template>
    <div id="login" class="login-container">
        <h1>Login</h1>
        <form @submit.prevent="emitLogin" class="login-form">
            <div class="input-group">
                <label for="email">E-mail:</label>
                <input v-model="email" placeholder="Digite seu e-mail" id="email" />
            </div>
            <div class="input-group">
                <label for="senha">Senha:</label>
                <input v-model="senha" type="password" id="senha" name="senha" placeholder="Digite sua senha" />
            </div>
            <button type="submit" class="login-btn">Entrar</button>
        </form>
    </div>
</template>

<style scoped>
   
    .login-container {
        max-width: 400px;
        margin: 50px auto;
        padding: 20px;
        background: #fff;
        border-radius: 8px;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        text-align: center;
        background: linear-gradient(135deg, #ffcd00, #004b87);
    }

    h1 {
        font-size: 50px;
        font-weight: bolder;
        color: #ffcd00; 
        margin-bottom: 30px;
    }

   
    .login-form {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }

   
    .input-group {
        text-align: left;
    }

    .input-group label {
        font-size: 14px;
        font-weight: bold;
        color: #333;
        margin-bottom: 5px;
    }

    .input-group input {
        width: 100%;
        padding: 10px;
        border-radius: 5px;
        border: 2px solid #ddd;
        font-size: 16px;
    }

    .input-group input:focus {
        border-color: #004b87; 
        outline: none;
    }

    
    .login-btn {
        background: linear-gradient(45deg, #ffcd00, #ff4f00); 
        color: white;
        padding: 15px;
        font-size: 18px;
        font-weight: bold;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: background 0.3s ease, transform 0.3s ease;
    }

    .login-btn:hover {
        background: linear-gradient(45deg, #004b87, #00b5e2);
        transform: scale(1.05); 
    }

    .login-btn:active {
        transform: scale(0.98);
    }
</style>
