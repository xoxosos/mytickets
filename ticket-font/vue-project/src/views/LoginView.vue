<template>
    <div  style="background-color: blue;" >

    <button @click="funclog">{{name[0]}}</button>
    <button @click="func">{{name[1]}}</button>
    
    </div>
</template>

<script lang="ts">
import { defineComponent , ref } from 'vue'

export default defineComponent({
    setup () {
        const name = ref(['注册','登录'])
        const func =function func() {
            alert('Hello vue3!')
        }
        const funclog  = ()=> {
            console.log("我是注册");
            
        }
        return {name,func,funclog}
    }
})
</script>

<style scoped>
 .button{
       size:10px 
 }
</style>