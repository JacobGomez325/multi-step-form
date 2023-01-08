<template>
  <div>
    <div class="flex justify-between items-center">
      <label 
      for=""
      class="text-gray-900 text-sm"
      >Nom</label>
      <p class="text-red-500 text-sm font-bold"> champs requis</p>
    </div>
    <input 
    type="text"
    placeholder="ex:"
    v-model="data"
    @keyup="getData"
    class="form-input text-gray-900 px-4 py-2 rounded-md border-gray-400 w-full"
    >
  </div>
</template>

<script lang="ts" setup>
  //les imports
  import type { PropType } from 'vue';
  import { ref ,defineEmits} from 'vue';

  //les emits
  const emits = defineEmits(['getData'])

  // les props
  const {type,basePlaceholder} = defineProps({
    type: {
      type: String as PropType<string>,
      required: true
    },
    basePlaceholder: {
      type: String as PropType<string>,
      required: false
    }
  })

  //les datas

  const data = ref<string>('')

  // les methods
  const getData = function() {
    emits('getData', data.value)
  }

</script>

<style lang="scss" scoped>

</style>