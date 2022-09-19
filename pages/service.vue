<template>
  <div class="">
    <div class="bg-gradient-to-t from-pink-200 to-white">
      <div>
        <HeadersContainer>
          <template #logo>
            <HeadersLogo />
          </template>
          <template #hamburgermenuopen>
            <button>
              <img
                :src="require('@/assets/icons/hamburger.png')"
                class="w-8 h-8"
              />
            </button>
          </template>
          <template #hamburgermenuclose>
            <button>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                class="fill-current text-black w-10 h-8"
                viewBox="0 0 50 50"
                version="1.1"
              >
                <g id="surface1">
                  <path
                    style="stroke: none; fill-opacity: 1"
                    d="M 9.15625 6.3125 L 6.3125 9.15625 L 22.15625 25 L 6.21875 40.96875 L 9.03125 43.78125 L 25 27.84375 L 40.9375 43.78125 L 43.78125 40.9375 L 27.84375 25 L 43.6875 9.15625 L 40.84375 6.3125 L 25 22.15625 Z "
                  />
                </g>
              </svg>
            </button>
          </template>
          <template #menu>
            <HeadersMenu>
              <template #hometext>Home</template>
              <template #servicetext>Service</template>
              <template #menutext>Menu</template>
              <template #contacttext>Contact</template>
            </HeadersMenu>
          </template>
          <template #search>
            <HeadersSearch />
          </template>
          <template #shop>
            <HeadersShop />
          </template>
          <template #button>
            <HeadersButton />
          </template>
        </HeadersContainer>
      </div>
      <div class="pt-24">
        <CtaContainer>
          <template #title>
            <div
              class="
                text-5xl
                md:text-6xl
                lg:text-7xl
                mt-10
                lg:mt-0
                w-full
                lg:w-10/12
              "
            >
              <h1 class="text-black font-bold leading-tight">
                Designer Cakes Delivered
                <span class="text-pink-500 font-bold">To your door steps</span>
              </h1>
            </div>
          </template>
          <template #description>
            <div class="text-base md:text-xl mt-10 w-full lg:w-10/12">
              <p>
                Cake lover is an award winning. Cakes and Bakes company in
                Nigeria. Founded in 2022
              </p>
            </div>
          </template>
          <template #orderbtn>
            <a href="./menupage">
              <button
                class="
                  border border-black
                  w-full
                  md:w-52
                  flex
                  justify-center
                  border
                  items-center
                  mt-16
                  p-5
                  rounded-md
                  hover:bg-white hover:text-black hover:border-white
                "
              >
                <h1>Learn More</h1>
                <img
                  :src="require('@/assets/icons/Right.png')"
                  class="w-6 h-4 ml-2"
                />
              </button>
            </a>
          </template>
          <template #picture>
            <div
              class="
                block
                lg:w-full
                h-full
                bg-pink-100
                rounded-full
                border-2
                mt-10
                lg:mt-0
                mx-auto
              "
            >
              <img
                :src="require('@/assets/images/cake.png')"
                class="w-full -mt-10"
              />
            </div>
          </template>
        </CtaContainer>
      </div>
    </div>

    <div class="">
      <div class="-mt-8 mx-auto max-w-sm rounded-md p-10 bg-white shadow-xl">
        <h1 class="text-center font-bold text-2xl md:text-4xl">
          Our Best Selling Categories
        </h1>
      </div>

      <div>
        <div class="mt-10 px-8 lg:px-16">
          <h1 class="font-bold text-3xl lg:text-4xl">Cupcakes</h1>
        </div>
        <div
          class="
            px-8
            xl:px-16
            grid
            gap-6
            grid-cols-1
            md:grid-cols-2
            lg:grid-cols-3
          "
        >
          <ServicesList
            v-for="item in cupcakes"
            :key="item.id"
            :title="item.title"
            :pic="item.pic"
            :price="item.price"
          />
        </div>
      </div>
      <div>
        <div class="mt-10 px-8 lg:px-16">
          <h1 class="font-bold text-3xl lg:text-4xl">Birthday Cakes</h1>
        </div>
        <div
          class="
            px-8
            xl:px-16
            grid
            gap-6
            grid-cols-1
            md:grid-cols-2
            lg:grid-cols-3
          "
        >
          <ServicesList
            v-for="item in birthdayCakes"
            :key="item.id"
            :title="item.title"
            :pic="item.pic"
            :price="item.price"
          />
        </div>
      </div>
      <div>
        <div class="mt-10 px-8 lg:px-16">
          <h1 class="font-bold text-3xl lg:text-4xl">Wedding Cakes</h1>
        </div>
        <div
          class="
            px-8
            xl:px-16
            grid
            gap-6
            grid-cols-1
            md:grid-cols-2
            lg:grid-cols-3
          "
        >
          <ServicesList
            v-for="item in weddingCakes"
            :key="item.id"
            :title="item.title"
            :pic="item.pic"
            :price="item.price"
          />
        </div>
      </div>
      <div>
        <div class="mt-10 px-8 lg:px-16">
          <h1 class="font-bold text-3xl lg:text-4xl">Cocktail and Moctail</h1>
        </div>
        <div
          class="
            px-8
            xl:px-16
            grid
            gap-6
            grid-cols-1
            md:grid-cols-2
            lg:grid-cols-3
          "
        >
          <ServicesList
            v-for="item in cocktailMocktail"
            :key="item.id"
            :title="item.title"
            :pic="item.pic"
            :price="item.price"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cupcakes: [
        {
          id: 1,
          title: "Strawberry",
          pic: require("@/assets/images/strawberry.png"),
          price:20,
        },
        {
          id: 2,
          title: "Caramel Apple pie",
          pic: require("@/assets/images/caramel.png"),
          price:50,
        },
        {
          id: 3,
          title: "Red velvet",
          pic: require("@/assets/images/velvet.png"),
          price:15,
        },
      ],

      birthdayCakes: [
        {
          id: 1,
          title: "Chiffon cake",
          pic: require("@/assets/images/chiffoncake.png"),
          price:350,
        },
        {
          id: 2,
          title: "pound cake",
          pic: require("@/assets/images/poundcake.png"),
          price:155,
        },
        {
          id: 3,
          title: "sponge cake",
          pic: require("@/assets/images/spongecake.png"),
          price:100,
        },
      ],

      weddingCakes: [
        {
          id: 1,
          title: "Carved cake",
          pic: require("@/assets/images/carved.png"),
          price:500,
        },
        {
          id: 2,
          title: "Fondant Covered Cakes",
          pic: require("@/assets/images/carved.png"),
          price:460.5,
        },
      ],

      cocktailMocktail: [
        {
          id: 1,
          title: "Apple Fizz",
          pic: require("@/assets/images/applefizz.png"),
          price:51.6,
        },
        {
          id: 2,
          title: "Mojito",
          pic: require("@/assets/images/mojito.png"),
          price:30,
        },
        {
          id: 3,
          title: "Manhattan",
          pic: require("@/assets/images/manhattan.png"),
          price:45.9,
        },
      ],
    };
  },
};
</script>

<style>
</style>