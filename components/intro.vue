<template>
<v-col cols="12" :sm="data.column">
  
  <template v-if="data.fieldId==='contents'">
    <div v-html="data.body" />
  </template>
  
  <template v-else-if="data.fieldId==='image'">
      <v-card flat tile>
      <v-img :src="data.image.url" />
      <v-card-subtitle>{{ data.caption }}</v-card-subtitle>
    </v-card>
  </template>
  
</v-col>
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