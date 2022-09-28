<template>
<div>
    <div class="bg-gradient-to-t from-pink-200 to-white p-10 h-56 md:h-full">
        <h1 class="text-5xl font-bold">Welcome</h1>
        <p class="text-black font-semibold m-2">Kindly proceed to the Login</p>
        <div class="relative bg-gray-100 shadow-xl max-w-2xl p-10 mx-auto h-80 md:h-96 top-16 md:top-56 rounded-2xl">
            <div class="absolute mx-auto right-0 px-10 w-full">
                <form @submit.prevent="userValidation" class="md:px-10">
                    <div class="flex justify-center items-center gap-2">
                        <img :src="require('@/assets/icons/Cupcake.svg')" class="w-8 hidden md:block">
                         <h1 class="text-center font-bold text-2xl">LOGIN</h1>
                    </div>
                   <div class="pt-4 md:pt-10">
                        <div class=" flex justify-center w-full md:ml-10">
                            <div class="relative w-full">
                                <div class="flex items-center w-full">
                                    <label :class="is_focused ? 'transform -translate-y-7 absolute transition duration-500 ease-in-out ml-4 font-bold text-sm px-2 bg-gray-100 ':'text-sm transition duration-500 ease-in-out ml-4 cursor-text font-bold absolute px-2'" for="text" >EMAIL</label>
                                    <input @focus="focus()" @blur="blur()" type="text" v-model="user_email" class="py-4 px-2 w-full md:w-10/12 bg-transparent border font-semibold border-black rounded-md outline-none">
                                </div>
                                
                            </div>
                        </div>
                        <div class="flex justify-center mt-6 w-full md:ml-10">
                            <div class="relative w-full">
                                <div class="flex items-center w-full">
                                    <label :class="password_focus ? 'transform -translate-y-7 absolute transition duration-500 bg-gray-100 ease-in-out ml-4 font-bold text-sm px-2':'text-sm transition duration-500  ease-in-out ml-4 cursor-text font-bold absolute px-2'" for="text" >PASSWORD</label>
                                   <div class=" border-black rounded-md border w-full md:w-10/12 flex items-center">
                                     <input type="password" @focus="passwordFocus()" @blur="passwordBlur()" v-model="user_password" class="py-4 font-semibold w-full px-2 bg-transparent outline-none">
                                     <img :src="require('@/assets/icons/Visible.png')" class="w-6 h-5 mr-4 cursor-pointer">
                                   </div>
                                </div>
                                
                            </div>
                        </div>
                   </div>
                   
                    <button class="block py-2 px-5 mx-auto bg-gray-300 rounded-md border shadow-md text-black font-bold mt-6 hover:bg-gray-400">ENTER</button>
                </form>
            </div>
        </div>
    </div>
    <BigModal :Show="popup" @cancel="userValidation">
      <template #title>
        <h1>Welcome</h1>
      </template>
      <template #desc>
         <h1 class="">Congratulations, You've successfully login.</h1>
         <div class="mt-4 lg:mt-10">
           <i class="">note: The dashboard is currently not available. coming soon!!</i>
         </div>
        
      </template>
    </BigModal>
    <BigModal :Show="wrong_pass" @cancel="userValidation">
      <template #desc>
         <h1 class="text-base lg:text-xl text-red-500 text-center">Wrong password!</h1>
      </template>
    </BigModal>
    <BigModal :Show="doesnt_exist" @cancel="userValidation">
      <template #desc>
         <h1 class="text-base lg:text-xl text-red-500 text-center">User does not exist!!</h1>
      </template>
    </BigModal>
    
    <div class="pt-80 lg:pt-72 px-4 flex gap-2 items-center justify-center">
        <nuxt-link to="/" class="font-bold">Go back to Homepage</nuxt-link>
        <img :src="require('@/assets/icons/Exit.png')" class="w-6">
    </div>
   
</div> 
</template>

<script>
export default {

  data() {
    return{
      user_email: "",
      user_password: "",
      popup:false,
      wrong_pass:false,
      doesnt_exist:false,
      is_focused:false,
      password_focus:false,
    };
  },
  methods: {
    userValidation() {

      let userAccount = {
        email: "adexvictor94@gmail.com",
        password: "victor",
      };
    
      if(this.user_email =="" && this.user_password ==""){
        return
      }else{
        
      }

      if (this.user_email == userAccount.email) {
            if (userAccount.password == this.user_password) {
                this.popup=!this.popup;
            } else {
                this.wrong_pass=!this.wrong_pass
            }
        }else {
                this.doesnt_exist=!this.doesnt_exist
        }
    
    },
    
   focus(){
    if (this.user_email=="") {
         this.is_focused = !this.is_focused
    } else {
        
    }
    
   },
   
   passwordFocus(){
    if (this.user_password=="") {
         this. password_focus = !this. password_focus
    } else {
        
    }
   },
   passwordBlur(){
     if (this.user_password==""  ) {
       this.password_focus = !this.password_focus
     } else {
       
     }
   },

   blur(){
     if (this.user_email==""  ) {
       this.is_focused = !this.is_focused
     } else {
       
     }
   }
  },
};
</script>

<style>
</style>