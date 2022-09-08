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
    <div class="pt-24">
      <CtaContainer>
        <template #title>
          <div class="text-5xl md:text-6xl lg:text-7xl mt-10 lg:mt-0 w-full lg:w-10/12">
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
        </template>
        <template #picture>
          <div
            class="
              block
              w-96
              h-full
              bg-pink-100
              rounded-full
              border-2
              mt-10
              lg:mt-0
              mx-auto
              overflow-hidden
            "
          >
            <img
              :src="require('@/assets/images/cta_pic1.png')"
              class="w-full object-cover"
            />
          </div>
        </template>
      </CtaContainer>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>