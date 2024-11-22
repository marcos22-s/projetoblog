<script>
    import { RouterLink } from 'vue-router';
    export default {
        props: {
            link: String,
            textoDoBotao: String
        }
    }
</script>

<template>
    <div class="olympic-button">
        <RouterLink :to="link">{{textoDoBotao}}</RouterLink>
    </div>
</template>

<style scoped>
 
    .olympic-button {
        padding: 20px;
        display: inline-block;
        margin-right: 15px;
        border-radius: 8px;
        background-color: #f0f0f0; 
    }

    
    a {
        font-size: 18px;
        color: #333; 
        text-decoration: none;
        padding: 10px 25px;
        border-radius: 5px;
        font-weight: bold;
        background: linear-gradient(45deg, #ffcd00, #ff4f00); 
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); 
        transition: background 0.3s ease, transform 0.3s ease;
    }
    
    
    a:hover {
        background: linear-gradient(45deg, #004b87, #00b5e2);
        color: white;
        transform: scale(1.05); 
    }

    a:focus {
        outline: none; 
        box-shadow: 0 0 10px 4px rgba(0, 75, 135, 0.7); 
    }
</style>
