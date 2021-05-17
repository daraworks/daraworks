<template>
<v-select
  v-model="data.value"
  :label="data.label"
  :items="data.items"
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