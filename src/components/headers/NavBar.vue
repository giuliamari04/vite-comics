<template>
    
        <nav class="navbar navbar-expand-lg d-flex justify-content-between container mb-0">
            <div>
                <img src="/images/dc-logo.png" alt="logo" class="w-50 m-3">
            </div>
  <div class="container-fluid">
    <div class="collapse navbar-collapse d-flex justify-content-end" id="navbarNavAltMarkup">
      <div class="navbar-nav text-uppercase fw-semibold" v-for="(text, index) in NavList">
        <a class="nav-link" href="#" :class="{ 'active': index === selectedItem }" @click="selectItem(index)">{{ NavList[index].text }}</a>
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
                selectedItem: 1,
            }
           
        },
        methods:{
            selectItem(index) {
    this.selectedItem = index;
  },
        },
 }
</script>

<style lang="scss" scoped>
@use '/src/assets/styles/partials/variables.scss' as *;
.active{
    color: $blue_primary !important;
    line-height: 3.8em;
    border-bottom: 7px solid $blue_primary;

}
nav{
    height: 15vh;
}
</style>
