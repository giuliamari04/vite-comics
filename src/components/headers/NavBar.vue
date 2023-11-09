<template>
    
        <nav class="navbar navbar-expand-lg bg-body-tertiary d-flex justify-content-between container">
            <div>
                <img src="/src/assets/images/dc-logo.png" alt="logo" class="w-50 m-3">
            </div>
  <div class="container-fluid ">
    <div class="collapse navbar-collapse d-flex justify-content-end" id="navbarNavAltMarkup">
      <div class="navbar-nav text-uppercase fw-semibold" v-for="(text, index) in NavList">
        <a class="nav-link" href="#" :class="{ 'active': index === selectedItem }" @click="selectItem(index)">{{ NavList[index].text }}</a>
        <!-- <a class="nav-link active" aria-current="page" href="#">characters</a>
        <a class="nav-link" href="#">comics</a>
        <a class="nav-link" href="#">movies</a>
        <a class="nav-link" href="#">tv</a>
        <a class="nav-link" href="#">tv</a>
        <a class="nav-link" href="#">tv</a>
        <a class="nav-link" href="#">tv</a>
        <a class="nav-link" href="#">tv</a>
        <a class="nav-link" href="#">tv</a>
        <a class="nav-link" href="#">tv</a> -->
      </div>
    </div>
  </div>
</nav>
</template>

<script>
 export default{
    name:'NavBar',
    components:{
           
        },
        data(){
            return{
                NavList:[
                    {
                        text:'characters',
                        link:'#',
                    },
                    {
                        text:'comics',
                        link:'#',
                    },
                    {
                        text:'movies',
                        link:'#',
                    },
                    {
                        text:'tv',
                        link:'#',
                    },
                    {
                        text:'games',
                        link:'#',
                    },
                    {
                        text:'collectibles',
                        link:'#',
                    },
                    {
                        text:'videos',
                        link:'#',
                    },
                    {
                        text:'fans',
                        link:'#',
                    },
                    {
                        text:'news',
                        link:'#',
                    },
                    {
                        text:'shop',
                        link:'#',
                    },
                ],
                selectedItem: null,
            }
           
        },
        methods:{
            selectItem(index) {
    this.selectedItem = index;
  },
        },
 }
</script>

<style scoped>

.active{
    color:#0282f9 !important ;
    line-height: 4em;
    border-bottom: 5px solid #0282f9;

}
</style>
