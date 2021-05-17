<template>
<v-main>
  
  <layout-title>
    {{ title }}
  </layout-title>

  <v-container>
    
    <v-row justify="center">
      <template v-for="item in data">
      <v-btn :href="`/member#${item.id}`" class="ma-3" fab large>
        <v-avatar size="64">
          <v-img :src="item.image.url" />
        </v-avatar>
      </v-btn>
      </template>
    </v-row>
    
  	<template v-for="item in data">
  	
  	<v-divider :id="item.id" class="my-12" />
  	
  	<member :data="item" />
  	
  	</template>
	
  </v-container>
  
</v-main>
</template>

<script>
export default {
  async asyncData({ app, $config }) {
    const { contents } = await app.$axios.$get(
      `${$config.API_URL}/member`,
      { headers: { 'X-API-KEY': $config.API_KEY }}
    )
    return { data: contents }
  },
  data() {
  	return {
  	  title: 'メンバー'
  	}
  },
  head () {
    return {
      title: this.title,
      meta: [
          { hid: 'og:title', property: 'og:title', content: this.title },
      ]
    }
  }
}
</script>