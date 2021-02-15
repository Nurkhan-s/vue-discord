<template>
<div class="navigation">
    <input type="text" placeholder="Найти или начать беседу">
    <hr >
    <button class="friends active">Друзья</button>
    <button class="nitro">Nitro</button>
    <messages/>
    <settings/>
</div>
</template>

<script>

import messages from './messages.vue';
import settings from './settings.vue';
export default {
    name: "navigation",
    components: {
        messages,
        settings
    },
    data() {

    },
    methods:{

    }
}
</script>

<style scoped>
    input{
        margin: 3px;
        border: 1px solid;
        cursor: pointer;
        border-radius: 4px;
        line-height: 22px;
        font-size: 14px;
        padding: 3px;
        background-color: rgba(17, 24, 39, 1);
    }
    .navigation{
        display: flex;
        flex-direction: column;
        flex: none;
        background-color: rgb(64, 65, 68);
        width: 14rem;
        min-height: 96vh;
        max-height: 100vh;
        height: 100%;
        padding: 0.5rem;
        position: relative;
    }
    hr{
        width: 100%;
        color: #000;
        margin: 1rem 0;
        padding: 0;
    
    }

    button{
        font-size: 16px;
        line-height: 26px;
        color: rgb(162, 161, 161);
        cursor: pointer;
        border: 1px solid transparent;
        border-radius: 4px ;
        background-color: rgb(64, 65, 68);
        padding: 8px;
        
    }
    .friends{
        background-image: url('../assets/images/emoji_people.svg');
        
        background-size: contain;
        background-position: left;
        background-repeat: no-repeat;
    }
    .nitro{
        background-image: url('../assets/images/rocket.svg');
        
        background-size: contain;
        background-position: left left;
        background-repeat: no-repeat;
    }
    .active{
        background-color: #8a8a8a;
        color: #fff;
        margin-bottom: 2px;
    }
    button:hover{
        color: #f0f0f0;
        background-color: #8a8a8a;
    }
    button + button {
        margin-top: 4px;
    }
    
</style>
<style >
.navigation{
    color: rgb(162, 161, 161);
}
.settings{
    width: 100%;
}
</style>