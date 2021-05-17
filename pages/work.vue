<template>
<v-main>
  
  <layout-title>
    {{ title }}
  </layout-title>

  <v-container>
    
    <layout-subtitle>
      活動内容
    </layout-subtitle>
    
    <layout-content>
      <v-row no-gutters>
        
        <v-col cols="12" sm="8">
          月に1回、メンバーで集まり、情報共有などの定例会を行います。
          <br>メンバーの協働で事業を行うこともあります。
        </v-col>
        
        <v-col cols="12" sm="4">
          <v-img
            src="https://images.microcms-assets.io/protected/ap-northeast-1:95d1c7bf-ee89-447a-808e-a942fafcdb65/service/daraworks/media/meeting.jpg"
          />
        </v-col>
        
      </v-row>
    </layout-content>
    
    <v-row justify="center" class="py-12">
      <v-col md="10" lg="8">
        <v-divider />
      </v-col>
    </v-row>
    
    <layout-subtitle>
      活動拠点
    </layout-subtitle>
    
    <layout-content class="pb-16">
      <v-row no-gutters>
        <v-col cols="12">
          メンバーは基本的に各々の拠点で活動します。
          <br>
          <br>ミーティングの時は主に<a href="https://www.google.com/maps/dir/?api=1&destination=ふれあい広場スイスイパーク" target="_blank">ふれあい広場スイスイパーク会議室</a>に集まります。
          <br>現在は無料で利用できるコワーキングスペースとなっています。
          <br>
          <br>以前は<a href="https://www.google.com/maps/dir/?api=1&destination=35.098254,137.571639" target="_blank">やまだ屋別棟</a>に集まっていました。
          <br>やまだ屋はメンバーの横山倫也さんの実家が営む衣料や福祉用具のお店です。
          <br>
          <br><a href="https://www.google.com/maps/dir/?api=1&destination=Kamomilla" target="_blank">Kamomilla（カモミッラ）</a>に集まることもあります。
          <br>Kamomillaはメンバーの橋本エレナさんが営むモザイクアートのお店です。
        </v-col>
      </v-row>
    </layout-content>
  	
  </v-container>
  
</v-main>
</template>

<script>
export default {
  data() {
  	return {
  	  title: '取り組み'
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