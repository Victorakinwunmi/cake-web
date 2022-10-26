<template>

    <AwareChild :active="true">
        <template #content="menu_props">
            Hello

            {{menu_props.send_props.message}}
        </template>
    </AwareChild>
  
</template>

<script>
export default {
    
}
</script>

<style>

</style>