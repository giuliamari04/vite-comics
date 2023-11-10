<template>
  <main class="my-bg-primary d-flex  align-items-center ">
    <section class="container">
      <div class="d-inline-flex flex-row my-w d-flex justify-content-center align-items-center"  v-for="(elem, index) in icons">
        <div class="d-flex align-items-baseline text-uppercase px-3">
          <div  class="icon ">
            <img :src='icons[index].img' alt="icon" class="w-100" />
          </div>
          <div class="w-75 fw-light">
            <span>{{ icons[index].text }}</span>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: "MainComponent",
  components: {},
  data() {
    return {
        icons:[
            {
                img:'/images/buy-comics-digital-comics.png',
                text:'digital comics',
            },
            {
                img:'/images/buy-comics-merchandise.png',
                text:'dc merchandise',
            },
            {
                img:'/images/buy-comics-subscriptions.png',
                text:'subscription',
            },
            {
                img:'/images/buy-comics-shop-locator.png',
                text:'comic shop locator',
            },
            {
                img:'/images/buy-dc-power-visa.svg',
                text:'dc power visa',
            },
        ]
    };
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@use "../assets/styles/partials/variables.scss" as *;
.my-bg-primary {
  background-color: $blue_primary;
}
main {
  color: white;
  height: 15vh;
}

.icon{
    width: 30px;
    height: 30px;
    margin-right: 10px;
}
.my-w{
    width:calc(100% / 5 );
}
.fw-light{
    font-size: 0.8em;
}
@media screen and (max-width: 768px) {
  main {
    height: fit-content; 
  }

  .icon {
    width: 60px; 
    height: 80px;
    padding-top: 20px;
  }

  .my-w {
    width: 100%;
    padding: 10px;
  }
}

@media screen and (max-width: 576px) {
  main {
    height: fit-content; 
  }
}
</style>
