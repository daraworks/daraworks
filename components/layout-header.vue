<template>
<v-app-bar app color="white">
  
  <v-toolbar-items>
    <v-btn
      to="/"
      style="text-transform: none"
      depressed
      plain
      nuxt
    >
      {{ title }}
    </v-btn>
  </v-toolbar-items>
  
  <v-spacer />
  
  <v-toolbar-items>
    
    <template v-if="$vuetify.breakpoint.smAndUp">
      <template v-for="item in menu">
      <v-btn
        :to="item.to"
        color="white"
        depressed
        nuxt
      >
        {{ item.label }}
      </v-btn>
      </template>
    </template>
    
    <template v-else>
      <v-menu offset-y>
        
        <template v-slot:activator="{ on, attrs }">
        <v-btn
          v-bind="attrs"
          v-on="on"
          depressed
          icon
        >
          <v-icon large>mdi-menu</v-icon>
        </v-btn>
        </template>
        
        <v-list>
          <v-list-item
            v-for="item in menu"
            :key="item.to"
            :to="item.to"
            nuxt
          >
            <v-list-item-title>{{ item.label }}</v-list-item-title>
          </v-list-item>
        </v-list>
        
      </v-menu>
    </template>
    
  </v-toolbar-items>
  
</v-app-bar>
</template>

<script>
export default {
  data() {
  	return {
  	  title: 'DARA-Works@shitara',
  	  menu: [
  	    { label: '取り組み', to: 'work' },
  	    { label: 'メンバー', to: 'member' },
  	    { label: 'お問合せ', to: 'contactUs' }
  	  ]
  	}
  }
}
</script>