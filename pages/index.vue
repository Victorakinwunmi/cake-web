<template>
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

    <div class="pt-24 ">
        <CtaContainer>
          <template #headingbtn>
            <div class="hidden w-52 lg:block border bg-pink-200 p-5 rounded-md">
              <h1 class="text-pink-400 font-bold">More than delicious</h1>
            </div>
          </template>

          <template #title>
            <div class="text-6xl lg:text-7xl mt-10 w-full lg:w-10/12">
              <h1 class="text-black font-bold">We provide the best <span class="text-pink-500 font-bold">cakes</span> for you</h1>
            </div>
          </template>

          <template #description>
            <div class="text-xl mt-10 w-full lg:w-10/12">
              <p>Our job is filling your tummy with delicious cakes, chops and chinchin with fast and free delivery</p>
            </div>
          </template>

          <template #orderbtn>
            <button class=" w-32 lg:block border bg-pink-500 mt-16 p-5 rounded-md">
              <h1 class="text-pink-100 font-bold">Order now</h1>
            </button>
          </template>

          <template #picture>
            <CtaImage/>
          </template>

        </CtaContainer>
    </div>
  </div>
</template>

<script>
export default {};
</script>

