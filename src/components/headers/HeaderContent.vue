<template>
    <div class=" text-light container my-h d-flex align-items-center">
     <h4>{{ text }}</h4>
    </div>
</template>

<script>
 export default{
    name:'HeaderContent',
    components:{
           
        },
        data(){
            return{
                text: '--> Content goes here <--',
            }
        },
        methods:{

        },
 }
</script>

<style scoped>
.my-h{
    height:15vh;
    margin-top: -12px;
}
</style>
