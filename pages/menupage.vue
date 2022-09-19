<template>
  <div>
    <div class="">
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

      <div>
        <div
          class="bg-no-repeat bg-cover bg-center"
          :style="{
            backgroundRepeat: 'no-repeat' + ';',
            backgroundImage:
              'url(' + require('@/assets/images/Cake04.jpg') + ')',
          }"
        >
          <div class="bg-gray-300 px-10 py-44 lg:py-60 bg-opacity-80 w-full">
            <div class="lg:px-16 max-w-3xl">
              <h1 class="font-bold text-5xl md:text-6xl lg:text-7xl">
                Find perfect <span class="text-pink-500">cakes</span> and
                <span class="text-pink-500">bakes</span> company near you
              </h1>
              <p class="text-xl lg:text-xl mt-10">
                Take a look at our menus below, choose your favorite products
                and place an order
              </p>
              <div
                class="
                  border border-black
                  rounded-full
                  w-44
                  mt-8
                  justify-center
                  p-2
                  flex
                "
              >
                <a href="https://wa.me/+2348107546757"
                  ><img
                    :src="require('@/assets/icons/whatsapp.png')"
                    class="lg:w-10 w-8"
                /></a>
                <a href="">
                  <img
                    :src="require('@/assets/icons/facebook.png')"
                    class="lg:w-10 w-8"
                /></a>
                <a href=""
                  ><img
                    :src="require('@/assets/icons/instagram.png')"
                    class="lg:w-10 w-8"
                /></a>
                <a href="">
                  <img
                    :src="require('@/assets/icons/twitter.png')"
                    class="lg:w-10 w-8"
                /></a>
              </div>
            </div>
          </div>
        </div>
      </div>

      <BigModal :Show="show_modal" @cancel="toggleModal">
        <template #title>
          <div>Welcome</div>
        </template>
        <template #desc>
          <h1>
           Kindly select the options below to place an order
          </h1>
        </template>

        <form @submit.prevent="handleChoicePicked">
          <div class="w-full outline-none p-4 border-2 rounded-md border-gray-300 mb-2 mt-2">
            <h1 class="text-gray-400 font-bold">Which of our products do you want?</h1>
            <select class="text-gray-400 outline-none py-2 bg-white" v-model="customer_product">
              <option value="Naked cake" class="font-bold">Naked cake</option>
              <option value="Strawberry cake" class="font-bold">Strawberry cake</option>
              <optgroup label="Custom cake">
                <option value="Wedding cake" >Wedding cake</option>
                 <option value="Birthday cake">Birthday cake</option>
              </optgroup>
              <option value="Cupcakes" class="font-bold">Cupcakes</option>
              <option value="mocktail/Cocktail" class="font-bold">mocktail/Cocktail</option>
            </select>
          </div>
          <div class="w-full outline-none p-4 border-2 rounded-md border-gray-300 mb-2 mt-2">
            <h1 class="text-gray-400 font-bold">Quantity of the product</h1>
            <select class="text-gray-400 outline-none py-2 bg-white" v-model="product_quantity">
              <option value="One" class="font-bold">One</option>
              <option value="Two" class="font-bold">Two</option>
              <option value="Three" class="font-bold">Three</option>
              <option value="Other" class="font-bold">Some</option>
            </select>
          </div>

            <button
              class="
                flex
                items-center
                mt-2
                justify-center
                border border-gray-400
                shadow-lg
                p-4
                w-44
                mx-auto
                mt-6
                bg-gray-400
                rounded-md
              "
            >
              <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" class="w-4 md:w-5 mr-2 fill-current text-gray-200" viewBox="0 0 50 50" version="1.1">
              <g id="surface1">
              <path style=" stroke:none; fill-opacity:1;" d="M 25 1 C 19.484375 1 15 5.484375 15 11 L 15 13 L 7.09375 13 
              L 2.875 50 L 47.125 50 L 42.90625 13 L 37 13 L 37 19 C 37 20.65625 35.65625 22 34 22 C 33.777344 22 33.550781 21.984375 33.34375 21.9375 C 
              32.003906 21.636719 31 20.433594 31 19 C 31 17.699219 31.839844 16.601563 33 16.1875 L 33 19 C 33 19.550781 33.445313 20 34 20 C 34.554688 20 
              35 19.550781 35 19 L 35 11 C 35 5.484375 30.515625 1 25 1 Z M 25 3 C 29.410156 3 33 6.589844 33 11 L 33 13 L 19 13 L 19 19 C 19 20.65625 17.65625 
              22 16 22 C 15.777344 22 15.550781 21.984375 15.34375 21.9375 C 14 21.636719 13 20.433594 13 19 C 13 17.699219 13.839844 16.601563 15 16.1875 L 15 19 
              C 15 19.550781 15.449219 20 16 20 C 16.550781 20 17 19.550781 17 19 L 17 11 C 17 6.589844 20.589844 3 25 3 Z "/>
              </g>
              </svg>

              <h1 class="text-gray-100 text-base md:text-xl font-bold">
                   Order !
              </h1>
            </button>
          
        </form>
      </BigModal>

      <div class="bg-gradient-to-t from-pink-200 to-white py-16">
        <div class="text-center mb-4">
          <h1 class="font-bold text-2xl md:text-5xl">
            Choose your favorite flavour
          </h1>
          <p class="mt-4 text-sm font-bold md:text-xl">
            Try our best custom designed cakes
          </p>
          <p class="text-sm text-gray-500">Click on the cake to order</p>
        </div>
        <div class="px-8 grid gap-6 grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
          <MenuList
            @toggledialog="toggleModal"
            v-for="item in menus"
            :key="item.id"
            :title="item.title"
            :pic="item.pic"
            :desc="item.desc"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Button from '../components/headers/Button.vue';
export default {
  components: { Button },
  data() {
    return {
       customer_product:"",
       product_quantity:"",

      menus: [
        {
          id: 1,
          title: "Naked Cake",
          pic: require("@/assets/images/naked.png"),
          desc: `Best cake for normal occasion parties and even
                after lunch you can have this light cake with cheese
                `,
        },
        {
          id: 2,
          title: "Strawberry Cake",
          pic: require("@/assets/images/straw.png"),
          desc: `Our website is User-friendly you can order by just
                clicking on (Buy now) and 3 simple steps and you will
                receive your order within 24 hours
               `,
        },
        {
          id: 3,
          title: "Custom Cake",
          pic: require("@/assets/images/chiffoncake.png"),
          desc: `We prepare custom cake as per clients requirements just 
                clicking on 3 simple steps and you will receive
               `,
        },
      ],

      show_modal: false,
    };
  },

  methods: {
    toggleModal() {
      this.show_modal = !this.show_modal;
    },

    handleChoicePicked(){
       window.location = 'https://api.whatsapp.com/send?phone=2348107546757&text=' + 'Hey, I would like to order for' + this.product_quantity + ' ' + this.customer_product 
    }
  },
};
</script>

<style>
</style>