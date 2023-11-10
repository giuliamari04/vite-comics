<template>
   <div class="card bg-transparent text-light" >
  <img :src="image" class="card-img-top" :alt="title">
  <div class="card-body">
    <h4 class="card-title">{{ title }}</h4>
  </div>
</div>
</template>
<script>
export default{
    name:'CardComponent',
    props:[
        'image',
        'title'
    ],
    data(){
        return{

        }
    }
}

</script>
<style lang="scss" scoped>
img{
  height: 250px;
}

.card-title{
  font-size: 1em;
}
</style>