<template>
    <div class="py-10 px-8">
      <div class="bg-white border border-gray-400 md:shadow-xl py-8 px-10 lg:px-10 md:py-16 container mx-auto w-full">
         <div class="w-full block md:flex mx-auto justify-between">
            <div class="w-full md:w-2/6">
              <h1 class="text-black font-bold text-xl lg:text-2xl mb-6">ORGANIZATION</h1>
              <div class="text-black">
                <a href="service" class="block mb-4">Service</a>
                <a href="menupage"  class="block mb-4">Menu</a>
                <a href="contact" class="block mb-4">Contact</a>
              </div>
            </div>
            <div class="w-full md:w-2/6 mx-auto">
              <h1 class="text-black font-bold text-xl lg:text-2xl mb-6">FOLLOW US</h1>
              <div class="text-black">
                <a href="http://www.facebook.com/cake" target="_blank" class="block mb-4">Facebook</a>
                <a href="mailto:adedapoabosederahcaee@gmail.com?" target="_blank"  class="block mb-4">Email</a>
              </div>
            </div>
            <div class="w-full md:w-2/6">
              <h1 class="text-black font-bold text-xl lg:text-2xl mb-6">TELEPHONE</h1>
              <p class="text-black mb-4">Nigeria (call and WhatsApp)</p>
              <div class="text-black">
                    <div class=" mr-4 mb-2 block">08107546757</div>
                    <div class=" mb-2 block">08104782750</div>
              </div>
            </div>
         </div>   
      </div>
    </div>
</template>

<script>
export default {
methods:{
     scrollToTour(){
      window.scroll({top:1150 ,behavior:'smooth'})
    },
    scrollToService(){
      window.scroll({top:1700, behavior:'smooth'})
    },
    scrollToAbout(){
      window.scroll({top:200 ,behavior:'smooth'})
    },
    scrollToTourMobile(){
      window.scroll({top:700 ,behavior:'smooth'})
    },
    scrollToServiceMobile(){
      window.scroll({top:2720 ,behavior:'smooth'})
    }
}
}
</script>

<style>

</style>