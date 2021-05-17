<template>
<v-footer>
  
  <v-row no-gutters justify="center">
    
    <template v-for="item in menu">
    <v-btn
      :to="item.to"
      class="text-decoration-underline"
      plain
      nuxt
    >
      {{ item.label }}
    </v-btn>
    </template>
    
	  <v-col cols="12" class="text-center caption">
	    {{ copyright }}
	  </v-col>
	  
	</v-row>
	
</v-footer>
</template>

<script>
export default {
  data() {
  	return {
  	  menu: [
  	    { label: '取り組み', to: 'work' },
  	    { label: 'メンバー', to: 'member' },
  	    { label: 'お問合せ', to: 'contactUs' }
  	  ],
  	  copyright: `© ${new Date().getFullYear()} DARA-Works@shitara`
  	}
  }
}
</script>