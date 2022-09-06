<template>
   <div class="block lg:flex p-10 lg:p-20 items-center">
     <div class="w-full">
        <div><slot name="headingbtn"/></div>
        <div><slot name="title"/></div>
        <div><slot name="description"/></div>
        <div><slot name="orderbtn"/></div>
     </div>

     <div class="w-full">
        <div><slot name="picture"/></div>
     </div>
   </div>
</template>

<script>
export default {

}
</script>

<style>

</style>