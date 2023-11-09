<template>
   <header>
    <NavBar />
    <HeaderContent />
   </header>
</template>

<script>
import NavBar from './headers/NavBar.vue';
import HeaderContent from './headers/HeaderContent.vue';
 export default{
    name:'HeaderComponent',
    components:{
          NavBar,
          HeaderContent,
        },
        data(){
            return{

            }
        },
        methods:{

        },
 }
</script>

<style scoped>
</style>
