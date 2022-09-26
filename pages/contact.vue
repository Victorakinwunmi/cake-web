<template>
  <div>
    <HeadersContainer>
      <template #logo>
        <HeadersLogo />
      </template>
      <template #hamburgermenuopen>
        <button>
          <img :src="require('@/assets/icons/hamburger.png')" class="w-8 h-8" />
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

    <div class="block lg:flex">
      <div class="w-6/12 hidden lg:block">
        <div
          class="bg-no-repeat bg-cover bg-center"
          :style="{
            backgroundRepeat: 'no-repeat' + ';',
            backgroundImage:
              'url(' + require('@/assets/images/Cake09.jpg') + ')',
          }"
        >
          <div class="bg-gray-300 px-10 h-screen py-72 bg-opacity-50 w-full">
            <div>
              <h1
                class="
                  font-bold
                  text-6xl text-gray-800
                  max-w-lg
                  mx-auto
                  leading-snug
                "
              >
                We would love to hear from you
              </h1>
            </div>
          </div>
        </div>
      </div>
    <div class="w-full lg:w-6/12 pt-40 px-12 lg:px-4 xl:px-16">
      <form
        @submit.prevent="handleMessage"
        class=""
      >
        <h1 class="font-bold text-4xl text-center lg:text-left mb-10 lg:mb-4">Contact Us</h1>
        <div class="block lg:flex">
          <div class="py-10 md:w-8/12 lg:w-full cursor-pointer mx-auto">
            <h1 class="font-semibold text-base">YOUR NAME</h1>
            <input
            v-model="customer_name"
              type="text"
              placeholder="Enter your name"
              class="
                outline-none
                border-b-2 border-gray-400
                hover:border-black
                w-full
                py-4
                text-xl
              "
            />
          </div>
        </div>

        <div class="block">
          <div class="py-10 w-full md:w-8/12 lg:w-full cursor-pointer mx-auto">
            <h1 class="font-semibold text-base">MESSAGE</h1>
            <textarea
              v-model="customer_message"
              class="
                outline-none
                border-b-2 border-gray-400
                hover:border-black
                w-full
                text-xl
              "
              rows="5"
            ></textarea>
          </div>
        </div>

        <button class="flex items-center gap-2 mt-4 mx-auto lg:mx-0">
          <p class="font-semibold text-base">SUBMIT</p>
          <img :src="require('@/assets/icons/Right.png')" class="w-4 h-3" />
        </button>

      </form>

      <button class="mt-16 text-center w-full lg:text-left">
          <div class="font-semibold">EMAIL US</div>
          <div> adedapoabosederachael@gmail.com</div>
      </button>

    </div>
    
  </div>
  </div>
</template>

<script>

export default {
  methods: {
    handleMessage(){
      if(this.customer_name == "" && this.customer_message ==""){
        return
      }else{
        window.location = 'https://api.whatsapp.com/send?phone=2348107546757&text=' + 'Hey, I\'m ' + this.customer_name + ', ' + this.customer_message
      }
    },
    
  },

  data() {
    return {
       customer_name:"",
       customer_message:"",
    };
  },
};
</script>