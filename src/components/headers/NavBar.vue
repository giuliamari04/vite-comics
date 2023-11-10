<template>
    
        <nav class="navbar navbar-expand-lg d-flex justify-content-between container">
            <div>
                <img src="/images/dc-logo.png" alt="logo" class="icon">
            </div>
           
  <div class="container-fluid">
    <div class="collapse navbar-collapse d-flex justify-content-end" id="navbarNavAltMarkup">
      <div class="navbar-nav text-uppercase fw-semibold" v-for="(text, index) in NavList">
        <a class="nav-link" href="#" :class="{ 'active': index === selectedItem }" @click="selectItem(index)">{{ NavList[index].text }}</a>
      </div>
    </div>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
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
    // border-bottom: 7px solid $blue_primary;

}
.navbar-toggler {
  display: none;
}
.dropdown{
    display: none;
}
.icon{
    width: 80%;
    
}
nav{
    height: 15vh;
}
.nav-link {
    position: relative;
  }
.nav-link.active::after {
    content: '';
    display: block;
    width: 100%;
    height: 7px;
    background-color: $blue_primary;
    position: absolute;
    bottom: -15px;
    left: 0;
  }

  @media screen and (max-width: 768px) {
  nav {
    height: 10vh; 
  }
 .nav-bar{
    display: flex;
    flex-wrap: nowrap;
 }
  .navbar-nav{
    width: 20%;
    font-size: small;
    padding: 5px;
  }
  .nav-link.active::after {
    bottom: 5px; 
  }
  .icon{
    width: 40%;
  }
}

@media screen and (max-width: 576px) {
  .navbar-toggler {
    display: block; 
    font-size: 0.8em;
  }

  .navbar-nav {
    display: none; 
  }
    nav {
    height: 8vh; 
  }
  nav {
    height: 10vh; 
  }
 .nav-bar{
    display: flex;
    flex-wrap: nowrap;
 }
  .nav-link.active::after {
    bottom: 5px; 
  }
  .icon{
    width: 40%;
  }
 
}
</style>
