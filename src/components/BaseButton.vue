<template>
  <button 
		v-if="template === 'default'" 
		key="default"
		class="bg-gray-600 text-gray-300 px-4 py-2 rounded-md shadow outline-none border-gray-600 font-semibold "
		>			
		<slot></slot>
	</button>

	<button 
		v-else-if="template === 'next'" 
		key="next"
		class="bg-primary text-white px-4 py-2 rounded-md shadow outline-none border-primary font-semibold "
		>
		<slot></slot>
	</button>

	<button 
		v-else-if="template === 'back'" 
		key="back"
		class="text-gray-900 px-4 py-2 rounded-md shadow outline-none border-blue-100 font-semibold "
		>
		<slot></slot>
	</button>

	<button 
		v-else 
		key="confirm"
		class="bg-primary text-white px-4 py-2 rounded-md shadow outline-none border-primary font-semibold "
		>
		<slot></slot>
	</button>
</template>

<script lang="ts" setup>
	import type { PropType } from 'vue';

	const {template} = defineProps({
		template: {
      type: String as PropType<string>,
			required: true
    }
	})
	
</script>

<style  scoped>

</style>