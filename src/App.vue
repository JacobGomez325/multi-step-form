
<template>
  <div>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem, fugit!


    <div class="flex space-x-4">
      <base-button template="default">defaut</base-button>
      <base-button template="next">next</base-button>
      <base-button template="back">back</base-button>
      <base-button template="confirm">confirm</base-button>
    </div>
    <toogle-switch>
      <template v-slot:valueFalse>
        <p class="ml-3 text-sm font-medium text-gray-900 "> false </p>
      </template>
      <template v-slot:valueTrue>
        <p class="ml-3 text-sm font-medium text-gray-900 "> true </p>
      </template>
    </toogle-switch>
    <br>
    <pre>
      ma donnée
      {{ data }}
    </pre>
    <BaseInput 
      type="text"
      base-placeholder="Label"
      @getData="getData"
    
    />
  </div>
</template>

<script lang="ts" setup>
  import BaseButton from './components/BaseButton.vue'
  import BaseInput from './components/BaseInput.vue'
  import ToogleSwitch from './components/ToogleSwitch.vue'

  import { ref } from 'vue'

  const data = ref<string>('')

  const getData = (dataInput:string) => {
    data.value = dataInput
  }

</script>

<style scoped>

</style>
