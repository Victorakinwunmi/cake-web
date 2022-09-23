<template>
<div>
    <div class="bg-gradient-to-t from-pink-200 to-white p-10">
        <h1 class="text-5xl font-bold">Welcome</h1>
        <p class="text-black font-semibold m-2">Kindly proceed to the Login</p>
        <div class="relative bg-gray-100 shadow-xl max-w-2xl p-10 mx-auto h-80 top-56">
        <div class="absolute mx-auto right-0 px-10 w-full">
            <form @submit.prevent="userValidation" class="md:px-10">
            <h1 class="text-center font-bold text-2xl">LOGIN</h1>
            <label class="block mb-2 font-semibold">EMAIL</label>
            <input type="email" v-model="user_email" class="w-full mb-2 outline-none block mx-auto p-2"/>
            <label class="block mb-2 font-semibold">PASSWORD</label>
            <input type="password" v-model="user_password" class="w-full block outline-none mb-2 p-2" />
            <button class="block py-2 px-5 mx-auto bg-gray-400 rounded-md border shadow-md text-black font-semibold mt-6">enter</button>
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
         <div class="mt-10">
           <i class="">note: The dashboard is currently not available. coming soon!!</i>
         </div>
        
      </template>
    </BigModal>
    <BigModal :Show="wrong_pass" @cancel="userValidation">
      <template #desc>
         <h1 class="text-lg lg:text-2xl text-center">The passsword you typed is incorrect!</h1>
      </template>
    </BigModal>
    <BigModal :Show="doesnt_exist" @cancel="userValidation">
      <template #desc>
         <h1 class="text-lg lg:text-2xl text-center">User does not exist!!</h1>
      </template>
    </BigModal>
</div>
   
</template>

<script>
export default {
  data() {
    return {
      user_email: "",
      user_password: "",
      popup:false,
      wrong_pass:false,
      doesnt_exist:false,
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
        } else {
                this.doesnt_exist=!this.doesnt_exist
        }
    },

    
     

  },
};
</script>

<style>
</style>