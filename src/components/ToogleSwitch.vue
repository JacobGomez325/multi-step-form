<template>
  <div class="flex space-x-2 items-center">
    <slot name="valueFalse"></slot>
    <label class="relative inline-flex items-center cursor-pointer">
      <input 
        type="checkbox" 
        value="" 
        class="sr-only peer">
      <div class="w-11 h-6 bg-gray-200 outline-none rounded-full peer dark:bg-gray-700 peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all dark:border-gray-600 peer-checked:bg-primary"></div>
    </label>
    <slot name="valueTrue"></slot>
  </div>

  

</template>

<script lang="ts" setup>

</script>

<style  scoped>


</style>