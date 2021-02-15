<template>
    
    <div class="messages">
        <div class="private-messages">
            <div>Личные сообщения</div>
            <div>+</div>
        </div>
        <ul 
         v-if="names.length">
            <li
            v-for="(name) in names" :key="name"
            :name = "name"
            >
            
            <div class="name">{{name}}</div>
            <span>X</span>
            </li>
            
        </ul>
        

    </div>
</template>
<script>
export default {
    data() {
        // <img :src=this.ava alt="ava">
        return {
            names:['Nurbakhyt', 'Nurkhan', 'John', 'David', 'Alex', 'Sarah', 'Lisa'],
            // ava: '../assets/images/discord.svg'
        }     
        
    },
    methods:{

    }
}
</script>







<style scoped>
    .messages{
        margin-top: 20px;
        
        overflow-x: auto;
        margin-bottom: 100px;
        
    }
    .private-messages{
        display: flex;
        justify-content: space-between;
        padding: 0 10px;
        cursor: pointer;
        
    }
    .private-messages:last-child{
        font-weight: 700;
    }
    .private-messages:hover{
        color: #fff;
    }
    ul,li{
        list-style: none;
    }
    ul{
        padding: 0;
    }
    li{
        position: relative;
        color: rgb(162, 161, 161);
        cursor: pointer;
        border: 1px solid transparent;
        border-radius: 4px ;
        padding: 2px 5px;
        padding-left: 50px;
        height: 35px;
        
    }
    li:hover{
        color: #f0f0f0;
        background-color: #8a8a8a;
    }
    li:hover span{
        display: block;
        color: #f0f0f0;
        background-color: #8a8a8a;
        position: absolute;
        right: 5px;
        bottom: 8px;
        
    }
    li::before{
        content: url('../assets/images/discord.svg');
        position: absolute;
        left: 0;
        
        object-fit: cover;
        
        
    }
    li + li {
        margin-top: 10px;
    }
    span{
        display: none;
        background-color: rgb(64, 65, 68);
        cursor: pointer;
        font-weight: bold;
        text-align: center;
        vertical-align: middle;
    }
    .name{
        padding-top: 5px;
    }
</style>