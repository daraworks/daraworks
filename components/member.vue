<template>
<v-row justify="center">
  
  <v-col cols="12" class="py-6 text-center">
    <h2>{{ data.name }}</h2>
  </v-col>
  
  <template v-for="item in data.contents">
    <intro :data="item" />
  </template>
  
  <v-col cols="10">
    <v-card outlined>
      <v-row no-gutters class="pa-3" align="center">
        
        <v-col cols="12" sm="auto" md="2">
          <v-img :src="data.image.url" width="100" height="100" />
        </v-col>
        
        <v-col cols="12" sm="auto" md="4" lg="3">
          
          <v-card-title>{{ data.name }}</v-card-title>
          
          <v-card-subtitle>{{ data.furigana }}</v-card-subtitle>
          
          <v-card-actions>
            <template v-for="item in data.sns">
            <sns :data="item" />
            </template>
          </v-card-actions>
          
        </v-col>
        
        <v-col cols="12" md="6" lg="7" v-html="data.profile" />
        
      </v-row>
    </v-card>
  </v-col>
  
</v-row>
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