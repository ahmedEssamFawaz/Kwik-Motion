<template>
  <v-app-bar color="white" dark max-height="140" height="123" elevation="1">
    <v-container fluid>
      <v-row no-gutters class="row-customization">
        <v-col cols="4" md="2" class="logo-container">
          <div class="logo text-center">
            <!-- Logo section -->
            <img
              :src="require('~/assets/imgs/main-logo/Group 6.svg')"
              alt="Logo"
              height="60"
              
            />
          </div>
        </v-col>
 
        <v-col cols="8" class="allLinksCol">
          <div class="allLinks">
            <div class="headLinks">
              <v-btn text class="custom-color text-capitalize" large>about</v-btn>
              <v-btn text class="custom-color text-capitalize" large>Partners</v-btn>
              <v-btn text class="custom-color text-capitalize" large>Success stories</v-btn>
            </div>
            <div class="bottomLinks">
              <v-btn text class="black--text text-capitalize" large>Products</v-btn>
              <v-btn text class="black--text text-capitalize" large>Blog</v-btn>
            </div>
          </div>

        </v-col>

        <v-col cols="2" class="loginLinksCol">
          <div class="loginLinks d-flex align-center">
            
            <v-btn text class="black--text text-capitalize" large>Login</v-btn>
            <BaseMainButton text="Request Demo"/>
            
          </div>
        </v-col>
        <v-col cols="8" class="navCol">
          <v-app-bar-nav-icon x-large color="black" @click="drawer = !drawer"/>

        </v-col>
      </v-row>
    </v-container>
  </v-app-bar>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({});
</script>

<style lang="scss">
.v-toolbar__content {
  padding: 0;
  height: 100% !important;
}
.container {
  height: 100%;
  padding: 0;
  margin: 0;
}
.row-customization {
  min-height: 100%;
}
.logo-container {
  border-right: 1px solid #e0e0e0;
  display: flex;
    justify-content: center;
    align-items: center;
}
.logo {

  img{
      max-width: 100%;
  }
}
.navCol{
  display: none;
}
.allLinks {
  height: 100%;
  .headLinks {
    border-bottom: 1px solid #e0e0e0;
  }
  .bottomLinks{
      padding-top: 20px;
  }
}
.loginLinks {
  border-left: 1px solid #e0e0e0;
  height: 100%;
}
.custom-color{
   color: #939393 !important;
}

@media(max-width: 1023px) {


  .allLinksCol{
    display: none;
  }
  .navCol{
    display: flex;
    justify-content: end;

  }
  .loginLinksCol{
    display: none;
  }

}

</style>
