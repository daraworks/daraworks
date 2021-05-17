<template>
<v-btn :href="data.url" icon>
  <v-icon>mdi-{{ data.type[0] }}</v-icon>
</v-btn>
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