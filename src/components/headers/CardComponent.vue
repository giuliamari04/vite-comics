<template>
   <!-- <div class="card bg-transparent text-light mt-3" >
  <img :src="image" class="card-img-top" :alt="title">
  <div class="card-body">
    <h4 class="card-title">{{ title }}</h4>
  </div>
</div> -->

<div class="flip-card">
  <div class="flip-card-inner">
    <div class="flip-card-front">
      <div class="card bg-transparent text-light mt-3 border-0 " >
  <img :src="image" class="card-img-top" :alt="title">
  <div class="card-body border-0 ">
    <h4 class="card-title">{{ title }}</h4>
  </div>
</div>
    </div>
    <div class="flip-card-back">
      <h5>{{title }}</h5> 
      <p>{{ tipo }}</p> 
      <p>{{ prezzo }}</p>
    </div>
  </div>
</div>
</template>



<script>
export default{
    name:'CardComponent',
    props:[
        'image',
        'title',
        'tipo',
        'prezzo',
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
.card{
  cursor: pointer;
  transition: 1s;
}
.card-title{
  font-size: 1em;
}

.flip-card {
  background-color: transparent;
  height: 300px;
  perspective: 1000px;
}

.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.6s;
  transform-style: preserve-3d;
}

.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
}

.flip-card-front {
  background-color:transparent;
}

.flip-card-back {
  background-color:transparent;
  border-radius: 10px;
  color: white;
  transform: rotateY(180deg);
  display: flex;
  flex-direction: column;
  align-items: center;
  align-content: center;
  justify-content: center;
  box-shadow: 0px 0px 10px #0282f9;
 
}
</style>