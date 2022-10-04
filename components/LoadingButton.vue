<template>
    <button 
    :class="color ? color : 'hover:bg-pink-100 border border-pink-200 text-black'" 
    :disabled="loading || disabled"
    class="font-bold rounded-md focus:text-pink-600 focus:text-black focus:outline-none outline-none my-10 py-4 px-2 w-56 ">
    
      <div class="flex items-center justify-center uppercase">
    
        <div v-if="loading" class="flex items-center">
          <div class="animate-pulse mr-2">
           <img :src="require('@/assets/icons/whatsapp.png')" width="30px" />
          </div>
          {{loadingText}}
        </div>
        <div v-if="!loading">
          <slot name="login" />
        </div>
        
      </div>
      
    </button>
</template>

<script>
  export default {
    name: "LoadingButton",
    props: {
      loading:Boolean,
      color: String,
      disabled: Boolean,
      loadingText: String,
    },
    data(){
      return{
       loading:true,
      }
    },

    methods:{
             
    }
  }
</script>
