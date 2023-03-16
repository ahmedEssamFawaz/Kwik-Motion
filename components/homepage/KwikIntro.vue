<template>
  <v-row class="mt-12">
    <v-col md="6" cols="12" class="d-flex align-center">
      <img
        class="mx-auto img-holder"
        src="~/assets/imgs/kwik-intro-section/Mask-Group-38.png"
        alt="laptop"
      />
    </v-col>
    <v-col md="6" cols="12">
        <div class="productWrapper">
            <div class="productLogo">
              <img
                class="mx-auto"
                src="~/assets/imgs/kwik-intro-section/Group 792.png"
                alt="laptop"
              />
            </div>
            <h3>
                KWIKmotion™ is a complete online video solution used by broadcasters, content producers and media companies.
            </h3>
            <BaseMainButton text="book a meeting"/>

        </div>
      
    </v-col>
  </v-row>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({});
</script>

<style scoped lang="scss">
.img-holder{
    max-width: 100%;
}
.productWrapper {
  padding-top: 5.9375rem;
  padding-right: 22rem;
  h3{
    color: #333333;
    font-size: 20px;
    line-height: 30px;
  }
    
  > * {
    margin-bottom: 15px; 
    &:last-child {
      margin-bottom: 0;
    }
}
}
@media (max-width: 1400px){
  .productWrapper{
    padding-right: 6rem;
  }
  
}
@media (max-width: 960px){
  .productWrapper{
    padding-top: 0;
    padding-right: 0;
    text-align: center;
  }
  
}
</style>
