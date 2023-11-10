<template>
    <div >
        <JumbotronComponent />
    </div>
    <div class=" text-center py-2 my-tag">current series</div>
    <div class="  container py-4 pt-4">
    <div class="row gy-2">
        <div class="col-12 col-md-4 col-lg-2 mt-3" v-for="(comix, index) in comic" :key="index">
            <CardComponent :image="comix.thumb" :title="comix.series" :tipo="comix.type" :prezzo="comix.price" />
        </div>
    </div>
    <div class="d-flex justify-content-center ">
        <a href="#" class="btn btn-primary text-uppercase mt-5 ">load more</a>
    </div>
    </div>
</template>

<script>
import {comics} from '../../data/comics.js';
import CardComponent from './CardComponent.vue';
import JumbotronComponent from './JumbotronComponent.vue';
 export default{
    name:'HeaderContent',
    components:{
           CardComponent,
           JumbotronComponent,
        },
        data(){
            return{
                comic:comics,
            }
        },
        methods:{

        },
 }
</script>

<style lang="scss" scoped>
.my-h{
    height:15vh;
    margin-top: -12px;
}
.my-tag{
    width: 250px;
    margin-top: -30px;
    margin-left: 10%;
    color: white;
    text-transform: uppercase;
    font-size: 2em;
    font-weight: 800;
    background-color: #0282f9;
}
</style>
