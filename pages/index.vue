<template>
<div>
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

    <div class="pt-24 lg:py-44">
      <CtaContainer>
        <template #headingbtn>
          <div class="hidden w-52 lg:block border bg-pink-200 p-5 rounded-md">
            <h1 class="text-pink-400 font-bold">More than delicious</h1>
          </div>
        </template>

        <template #title>
          <div class="text-5xl md:text-6xl lg:text-7xl mt-10 w-full lg:w-10/12">
            <h1 class="text-black font-bold">
              We provide the best
              <span class="text-pink-500 font-bold">cakes</span> for you
            </h1>
          </div>
        </template>

        <template #description>
          <div class="text-base md:text-xl mt-10 w-full lg:w-10/12">
            <p>
              Our job is filling your tummy with delicious cakes, chops,
              cocktail and mocktail with fast and free delivery
            </p>
          </div>
        </template>

        <template #orderbtn>
            <button
              class="
                w-full
                md:w-52
                flex
                justify-center
                md:justify-between
                border
                items-center
                bg-pink-500
                mt-16
                p-5
                hover:bg-pink-600
                rounded-md
              "
              @click="scrollToOrder"
            >
              <h1 class="text-pink-100 mx-4 text-center font-bold">
                Order now
              </h1>
              <div>
                <img
                  :src="require('@/assets/icons/chevron.png')"
                  class="w-10 h-8"
                />
              </div>
            </button>
        </template>

        <template #picture>
          <CtaImage />
        </template>
      </CtaContainer>
    </div>

    <div class="py-16 lg:px-0 bg-gradient-to-t from-white to-pink-100">
      <div class="text-black text-center">
        <h1 class="text-4xl lg:text-6xl font-bold">How To Order</h1>
        <p class="mt-6 px-10 text-base lg:text-xl">
         Our job is filling your tummy with delicious cakes, chops, mocktail
         and cocktail with fast and free delivery
        </p>
      </div>

      <div
        class="
          flex-col
          lg:flex-row
          lg:px-28
          gap-1
          mt-10
          lg:mt-16
          flex 
          justify-center
          md:max-w-7xl
          mx-auto
        "
      >
        <div class="justify-center lg:max-w-lg mx-auto w-7/12 block md:flex items-center">
          <div>
            <div>
              <img
                :src="require('@/assets/icons/checkorder.png')"
                class="w-20 mx-auto h-20"
              />
            </div>
            <h1 class="text-center font-bold text-xl mt-4">Choose menu</h1>
            <p class="text-center text-sm md:text-base">
              Select the cake, chops, mocktail or cocktail you want, please do
            </p>
          </div>
          <div>
            <img
              :src="require('@/assets/icons/arrow2.png')"
              class="hidden lg:block w-12 h-10"
            />
          </div>
        </div>

        <div class="justify-center lg:max-w-lg mx-auto w-7/12 block md:flex items-center my-10 lg:m-0">
          <div>
            <div>
              <div>
                <img
                  :src="require('@/assets/icons/menu.png')"
                  class="w-20 mx-auto h-20"
                />
              </div>
            </div>
            <h1 class="text-center font-bold text-xl mt-4">checkout order</h1>
            <p class="text-center  text-sm md:text-base">
              Select the cake, chops, mocktail or cocktail you want, please do
            </p>
          </div>
          <div>
            <img
              :src="require('@/assets/icons/arrow2.png')"
              class="hidden lg:block w-12 h-10"
            />
          </div>
        </div>

        <div class="mx-auto w-7/12">
          <div>
            <div>
              <div>
                <img
                  :src="require('@/assets/icons/delivery.png')"
                  class="w-20 mx-auto h-20"
                />
              </div>
            </div>
            <h1 class="text-center font-bold text-xl mt-4">
              Wait for delivery
            </h1>
            <p class="text-center text-sm md:text-base">
              Select the cake, chops, mocktail or cocktail you want, please do
            </p>
          </div>
        </div>
      </div>
    </div>

    <div
      class="
        bg-gradient-to-t
        from-pink-200
        to-white
        block
        lg:flex
        justify-center
        pt-16
      "
    >
      <div>
        <div
          class="
            block
            w-10/12
            lg:w-full
            bg-pink-100
            rounded-full
            border-2
            mx-auto
            lg:mx-auto lg:mt-10
          "
        >
          <img :src="require('@/assets/images/ceo_pic.png')" class="w-full" />
        </div>
      </div>

      <div class="w-full lg:w-4/12 lg:ml-16 px-10 py-16">
        <h1 class="font-bold text-5xl mb-6 lg:mt-28">About Us</h1>
        <p class="text-base">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Magni
          inventore nostrum nulla commodi adipisci repellat, facilis iste dolore
          eum nobis fuga quis numquam tempore, voluptatem, culpa porro saepe
          quae fugit. orem ipsum dolor sit amet consectetur adipisicing elit.
          Magni inventore nostrum nulla commodi adipisci repellat, facilis iste
          dolore eum nobis fuga quis numquam tempore, voluptatem, culpa porro
          saepe quae fugit.
        </p>
      </div>
    </div>

    <div class=" bg-pink-100 mt-10 lg:mt-0 py-16">
      <div class="">
        <h1 class="px-8 font-bold mb-6 text-2xl lg:text-4xl md:px-52">Frequently Asked Questions??</h1>
      </div>
      <AccordionAppAccordion>
         <template #question>
           <div class="">What makes your product differrent?</div>
         </template>
         <template #content>
           <div class="">Well, you might have read once or twice that we are a scratch bakery and that alone make us unique from other bakeries.</div>
         </template>
      </AccordionAppAccordion>
      <AccordionAppAccordion>
         <template #question>
           <div>Are you a full service bakery?</div>
         </template>
         <template #content>
           <div>We are a full-service bakery. We do not make breads, but we make most other bakery products. please check our service at the top-bar</div>
         </template>
      </AccordionAppAccordion>
      <AccordionAppAccordion>
         <template #question>
           <div>Please how do i place order?</div>
         </template>
         <template #content>
           <div>How you can place order is explained above , you can simply choose menu at the top-bar and place an order</div>
         </template>
      </AccordionAppAccordion>
    </div>
    <BigModal :Show="poup" @cancel="closeModal">
      <template #title>
        <h1>Welcome</h1>
      </template>
      <template #desc>
         <h1>Kindly input your address and phone number to enhance your accessibilities on this website</h1>
      </template>
      <div class="mb-2 mt-5">
        <div class="w-full outline-none p-4 border-2 rounded-md border-gray-300">
            <div class="-mt-7 mb-4 rounded-full font-bold text-gray-400 w-16 text-center bg-pink-100">Address</div>
          <input type="text" placeholder="Please enter your Address" class="outline-none text-gray-400 bg-transparent w-full">
        </div>
      </div>

      <div class="mb-2 mt-5">
          <div class="w-full outline-none p-4 border-2 rounded-md border-gray-300">
            <div class="-mt-7 mb-4 font-bold text-gray-400 w-20 text-center bg-pink-100 rounded-full">Phone no</div>
            <input type="number" placeholder="Please enter your Phone number" class="outline-none text-gray-400 bg-transparent w-full">
          </div>
      </div>

      <button class="flex gap-2 items-center bg-pink-300 border duration-500 transition text-gray-100 ease-in-out hover:text-gray-300 hover:bg-gray-400 w-44 mx-auto justify-center p-4 mt-4 rounded-md">
        <h1 class="font-bold">Submit</h1>
      </button>
    </BigModal>
  </div>
  <Footer/>
</div>
</template>

<script>
export default {
  props:{
    popupPoint:{
      default:200,
      type:Number,
    }
  },
  data(){
    return{
      popup:false,
    };
  },
  methods:{
    closeModal(){
      this.popup=this.popup;
    },

    handleStickyNavigation() {
      if (window.pageYOffset > this.popupPoint) {
        this.popup = true;
      } else {
        this.popup = false;
      }
    },
    scrollToOrder(){
      window.scroll({top:800, behavior:'smooth'})
    }
  },

  beforeMount() {
    window.addEventListener("scroll", this.handleStickyNavigation);
  },

  beforeDestroy() {
    window.removeEventListener("scroll", this.handleStickyNavigation);
  },


};
</script>

