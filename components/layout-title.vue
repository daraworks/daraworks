<template>
<v-container fluid>
  <v-row class="orange lighten-4">
    <v-col cols="12" class="py-6 py-md-10 text-center text-h6 text-md-h4">
        <slot />
    </v-col>
  </v-row>
</v-container>
</template>

<script>
export default {
  data() {
  	return {
  	}
  }
}
</script>