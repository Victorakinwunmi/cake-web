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
        <div class="bg-no-repeat bg-cover bg-center" :style="{backgroundRepeat: 'no-repeat' + ';' , backgroundImage: 'url(' + require('@/assets/images/Cake04.jpg') +')'}">
          <div class="bg-gray-300 px-10 py-44 lg:py-60 bg-opacity-80 w-full">
             <div class="lg:px-16 max-w-3xl">
               <h1 class="font-bold text-5xl md:text-6xl lg:text-7xl">Find perfect <span class="text-pink-500">cakes</span> and <span class="text-pink-500">bakes</span> company near you</h1>
               <p class="text-xl lg:text-xl mt-10">Take a look at our menus below, choose your favorite products and place an order</p>
               <div class="border border-black rounded-full w-44 mt-8 justify-center p-2 flex">
                  <a href="https://wa.me/+2348107546757"><img :src="require('@/assets/icons/whatsapp.png')" class="lg:w-10 w-8"></a>
                  <a href=""> <img :src="require('@/assets/icons/facebook.png')" class="lg:w-10 w-8"></a>
                  <a href=""><img :src="require('@/assets/icons/instagram.png')" class="lg:w-10 w-8"></a>
                  <a href=""> <img :src="require('@/assets/icons/twitter.png')" class="lg:w-10 w-8"></a>     
               </div>
             </div>
          </div>
        </div>
      </div>

      <BigModal :Show="show_modal" @cancel="toggleModal" >
        <template #title>
          <div>Welcome</div>
        </template>
         <template #desc>
          <div>Kindly click on the button below to discuss more about your order request on whatsapp</div>
        </template>
         <div class="max-w-xl mx-auto">
          <div class="block">
            <input type="text" placeholder="Which of our products do you want?" class="w-full outline-none p-5 border-2 rounded-md border-gray-300 mb-2 truncate">
            <input type="text" placeholder="Description of the product?" class="w-full outline-none p-5 border-2 rounded-md border-gray-300 truncate">
          </div>
          <div class="block ">
            <input type="text" placeholder="Quantity of the product?" class="w-full outline-none p-5 border-2 rounded-md border-gray-300 mb-2 mt-2 truncate">
            <input type="text" placeholder="when do you want it to be delivered?" class="w-full outline-none p-5 border-2 rounded-md border-gray-300 truncate">
          </div>
         
          <a href="https://wa.me/+2348107546757">
            <div class="flex items-center mt-2 justify-center border border-gray-200 shadow-lg p-4 mt-6 bg-gray-100 rounded-md">
            <img :src="require('@/assets/icons/whatsapp.png')" class="lg:w-10 w-8 mr-4">
              <h1 class="truncate text-gray-400 font-semibold">Kindly leave us a message on whatsapp to discuss more about your order</h1>
            </div>
          </a>
         </div>
      </BigModal>

      <div class="bg-gradient-to-t from-pink-200 to-white py-16">
        <div class="text-center mb-4">
          <h1 class="font-bold text-2xl md:text-5xl">Choose your favorite flavour</h1>
          <p class="mt-4 text-sm font-bold md:text-xl">Try our best custom designed cakes</p>
          <p class="text-sm text-gray-500 ">Click on the cake to order</p>
        </div>
        <div
          class="
            px-8
            grid
            gap-6
            grid-cols-1
            md:grid-cols-2
            lg:grid-cols-3
          "
        >
          <MenuList @toggledialog="toggleModal"
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
export default {
  data() {
    return {
      menus: [
        {
          id: 1,
          title: "Naked Cake",
          pic: require("@/assets/images/naked.png"),
          desc:`Best cake for normal occasion parties and even
                after lunch you can have this light cake with cheese
                `
        },
        {
          id: 2,
          title: "Strawberry Cake",
          pic: require("@/assets/images/straw.png"),
          desc:`Our website is User-friendly you can order by just
                clicking on (Buy now) and 3 simple steps and you will
                receive your order within 24 hours
               `
        },
        {
          id: 3,
          title: "Custom Cake",
          pic: require("@/assets/images/chiffoncake.png"),
          desc:`We prepare custom cake as per clients requirements just 
                clicking on 3 simple steps and you will receive
               `
        },
      ],

      show_modal: false,
    }

  },

  methods : {
    toggleModal(){
      this.show_modal = !this.show_modal
    }
  }
};
</script>

<style>
</style>