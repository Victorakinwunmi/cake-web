<template>
    <div>

        <div class="p-56">
            <input class="border p-4" type="text" placeholder="Hello" v-model="new_message" /> -->
            <button @click="submitMessage" class="bg-gray-500 p-4">Submit</button>

            
        </div>
        

        <slot name="content" :send_props="{is_active: active, message: new_message }"/>

        <hr />

        
    </div>
  
</template>

<script>
import Button from '../headers/Button.vue'
export default {
  components: { Button },
    props: {
        active: {
            type:Boolean,
            default:false
        }
    },

    data() {
        return {
            new_message: ''
        }
    },

    methods: {
        // submitMessage() {
        //     console.log('Hellodd')
        //     console.log(this.new_message)
        // }
    }


}
</script>

<style>

</style>