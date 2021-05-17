<template>
<v-main>
  
  <layout-title>
    {{ title }}
  </layout-title>
  
  <v-container class="pt-6 pb-16">
    <v-row justify="center">
      <v-col md="8" lg="6">
        活動に興味をお持ちの方は、以下の電話またはフォームよりお問合せください
      </v-col>
      <v-col cols="12" class="text-center">
        <h3>0536-62-0514</h3>
        設楽町役場 企画ダム対策課
      </v-col>
    </v-row>
  	<v-row justify="center">
  	  <v-col md="8" lg="6">
  	    <v-form>
  	      
  	      <template v-for="item in data">
  	        
    	      <template v-if="item.type==='select'">
    	        <form-select :data="item" />
    	      </template>
    	      
    	      <template v-else-if="item.type==='textarea'">
    	        <form-textarea :data="item" />
    	      </template>
    	      
    	      <template v-else>
    	        <form-text-field :data="item" />
    	      </template>
    	      
  	      </template>
  	      
          <v-btn
            type="submit"
            color="primary"
            block
            large
          >
            送信
          </v-btn>
  	      
  	    </v-form>
  	  </v-col>
  	</v-row>
  </v-container>
  
</v-main>
</template>

<script>
export default {
  data() {
  	return {
  	  title: 'お問合せ',
  	  data: [
  	    { label: 'お問合せ項目', value: null, type: 'select', items: ['質問したい', '見学したい', '仕事を依頼したい'] },
  	    { label: '名前', value: null, type: 'text' },
  	    { label: 'メールアドレス', value: null, type: 'text' },
  	    { label: '内容', value: null, type: 'textarea' },
  	  ]
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