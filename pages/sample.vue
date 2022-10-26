<template>
<div class="bg-black h-full p-10 ">
     <div class="flex flex-col-reverse ">
        <div class="block w-full h-full" v-for="item in messages" :key="item.id">
            <form @submit.prevent="deleteMessage(item.id)" class="flex items-center mt-2 lg:mt-0 justify-center mb-2">
                <div class="bg-gray-600 p-4 w-72 rounded-xl">
                    <h1 class="font-semibold text-white text-center text-base">{{item.message}}</h1>
                </div>
                <button class="ml-2">
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" class="fill-current w-5 text-white" viewBox="0 0 50 50" version="1.1">
                        <g id="surface1">
                        <path style=" stroke:none;fill-rule:nonzero;" d="M 9.15625 6.3125 L 6.3125 9.15625 L 22.15625 25 L 6.21875 40.96875 L 9.03125 43.78125 L 25 27.84375 L 40.9375 43.78125 L 43.78125 40.9375 L 27.84375 25 L 43.6875 9.15625 L 40.84375 6.3125 L 25 22.15625 Z "/>
                        </g>
                    </svg>
                </button>
            </form>
        </div> 
        <form @submit.prevent="addMessage">
            <input type="text" v-model="user_message" class="w-72 p-3 outline-none rounded-md">
            <button class="mt-2 md:mt-0 bg-gray-600 text-gray-200 py-3 px-6 font-black outline-none rounded-md">Add</button>
        </form>
    </div>

     <div class="bg-gray-200 rounded-md mt-10 h-60 w-full p-10 ">
           <h1 class="font-black text-gray-600 text-2xl md:text-5xl">Menus</h1>
           <p class="text-gray-600 mt-1 md:mt-4">Welcome to our menus</p>
           <h1 class="font-black text-center mt-2 md:mt-0 text-gray-600 text-xl md:text-4xl">Birthday cakes</h1>
     </div>
     <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 px-10 md:px-28 cursor-pointer gap-2 -mt-10">
        <div class="bg-gray-600 rounded-xl p-10 max-w-xl">
            <img :src="require('@/assets/images/chiffoncake.png')" class="mx-auto">
            <h1 class="font-bold text-center text-2xl text-gray-300">Cake</h1>
        </div>
        <div class="bg-gray-600 rounded-xl p-10 max-w-xl">
            <img :src="require('@/assets/images/chiffoncake.png')" class="mx-auto">
            <h1 class="font-bold text-center text-2xl text-gray-300">Cake</h1>
        </div>
        <div class="bg-gray-600 rounded-xl p-10 max-w-xl">
            <img :src="require('@/assets/images/chiffoncake.png')" class="mx-auto">
            <h1 class="font-bold text-center text-2xl text-gray-300">Cake</h1>
        </div>
     </div>

    
</div>
  
</template>

<script>
export default {
  data(){
    return{
        counter: 1,
        user_message:"",
        messages:[]
         
    };
  },
  methods:{
    addMessage(){

      if(this.user_message ==""){
        return
      }else{
        this.counter++
         this.messages.push({
            id: this.counter,
            message: this.user_message
         })
      }
    },

    deleteMessage(id){
        const findObj = this.messages.findIndex((obj) => {
            return obj.id === id
        })   
        this.messages.splice(findObj, 1)
    },
    
    messageDuration(){
        setInterval(() => {
            this.messages.shift()
        },10000)
    }

  },

  created(){
    this.messageDuration()
  }
}
</script>

<style>

</style>