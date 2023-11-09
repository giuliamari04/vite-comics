<template>
  <main class="bg-primary">
    <section class="container">
      <div class="d-inline-flex flex-row my-w py-4" v-for="(elem, index) in icons">
        <div class="d-flex justify-content-center align-items-center text-uppercase px-4">
          <div  class="w-25 px-2 ">
            <img :src='icons[index].img' alt="icon" class="card-img" />
          </div>
          <div>
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
                img:'/src/assets/images/buy-comics-digital-comics.png',
                text:'digital comics',
            },
            {
                img:'/src/assets/images/buy-comics-merchandise.png',
                text:'dc merchandise',
            },
            {
                img:'/src/assets/images/buy-comics-subscriptions.png',
                text:'subscription',
            },
            {
                img:'/src/assets/images/buy-comics-shop-locator.png',
                text:'comic shop locator',
            },
            {
                img:'/src/assets/images/buy-dc-power-visa.svg',
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
.bg-primary {
  background-color: $blue_primary;
}
main {
  color: white;
  height: 15vh;
}
.my-w{
    width:calc(100% / 5 - 10px);
}
</style>
