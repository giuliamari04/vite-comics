<template>
   <header>
    <div class="bg-navbar">
        <NavBar />
    </div>
    <div class="bg-headercontent">
         <HeaderContent />
    </div>
   
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
.bg-navbar{
    background-color:#ffffff ;
}

.bg-headercontent{
    background-color:#1c1c1c ;
}
</style>
