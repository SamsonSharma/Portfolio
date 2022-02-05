<template>
    <button @click="onClick()" class="btn">
        {{ text }}
    </button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        //color: String,
    },
    methods: {
        onClick(){
            console.log('BEPIS')
        }
    } 

}
</script>

<style scoped>



    button{
        background-color: #ffffff00;
        font-family: 'Roboto', sans-serif;
        margin-left: 0px;
        margin-right: 0px;
        border: 0px solid;
        width: 100px;
        font-size: 2vw;
        color: rgb(206, 205, 205);
        max-width: 100%;
    }
   
    
</style>
