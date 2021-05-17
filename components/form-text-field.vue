<template>
<v-text-field
  v-model="data.value"
  :label="data.label"
  outlined
/>
</template>

<script>
export default {
  data() {
  	return {
  	}
  },
  props: ['data']
}
</script>