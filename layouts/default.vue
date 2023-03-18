<template>
  <v-app dark>
    <LayoutsHeader />
    <v-main>
      <v-container fluid>
        <Nuxt />
      </v-container>
    </v-main>

   <LayoutsFooter/>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',

}
</script>
<style lang="scss">
.v-application {
   font-family: $body-font-family, sans-serif !important;
    
 }
</style>