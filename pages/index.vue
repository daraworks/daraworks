<template>
<v-main>
  
  <v-img
    :height="`calc(100vh - ${margin}px)`"
    src="https://images.microcms-assets.io/protected/ap-northeast-1:95d1c7bf-ee89-447a-808e-a942fafcdb65/service/daraworks/media/bgImg.jpg"
  />
  
  <layout-title>
    {{ about_title }}
  </layout-title>
  
  <v-container class="pt-6 pb-16">
    <v-row justify="center">
      <v-col md="8" lg="6">
        DARA works(だらわーくす)とは、愛知県設楽町(したらちょう)に住んでいた人と移り住んできた人とが互いに手を取り合い、設楽町で新たな仕事づくりを目指す場です。
        <br>20~40代の働き盛り世代が、これからの設楽町の未来を考え、共に新しいものを生み出し、自分たちにしかできない「何か」を探し続けています。
      </v-col>
    </v-row>
  </v-container>
  
  <layout-title>
    {{ news_title }}
  </layout-title>
  
  <v-container class="pt-6 pb-16">
    <v-row justify="center">
      <v-col cols="auto">
        <iframe
          :src="`https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2FShitaraDaraWorks&tabs=timeline&width=${width}&height=${height}&small_header=true&adapt_container_width=true&hide_cover=false&show_facepile=true&appId=417872139569047`"
          style="border:none;overflow:hidden"
          :width="width"
          :height="height"
          scrolling="no"
          frameborder="0"
          allowfullscreen="true"
          allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"
        />
      </v-col>
    </v-row>
  </v-container>
  
</v-main>
</template>

<script>
export default {
  data() {
  	return {
  	  about_title: 'DARA-Works@shitaraとは？',
  	  news_title: '最新情報',
  	  height: 592
  	}
  },
  computed: {
    margin () {
      if (this.$vuetify.breakpoint.xs) {
        return 56
      }
      else {
        return 64
      }
    },
    width () {
      if (this.$vuetify.breakpoint.xs) {
        return 296
      }
      else {
        return 500
      }
    }
  },
  head () {
    return {
      titleTemplate: 'DARA-Works@shitara'
    }
  }
}
</script>