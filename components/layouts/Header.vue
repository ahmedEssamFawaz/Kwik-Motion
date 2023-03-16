<template>
  <v-app-bar color="white" dark max-height="140" height="123">
    <v-container fluid>
      <v-row no-gutters class="row-customization">
        <v-col cols="2" class="logo-container">
          <div class="logo">
            <!-- Logo section -->
            <img
              src="~/assets/imgs/main-logo/Group 6@2x.png"
              alt="Logo"
              height="60"
            />
          </div>
        </v-col>
        <v-col cols="8">
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

        <v-col cols="2">
          <div class="loginLinks d-flex align-center">
            
            <v-btn text class="black--text text-capitalize" large>Login</v-btn>
            <BaseMainButton text="Request Demo"/>

          </div>
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
}
.logo {
  padding: 30px;
  padding-bottom: 0;
  height: 100%;
  img{
      max-width: 100%;
  }
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
  padding: 18px 50px 18px 35px;
}
.custom-color{
   color: #939393 !important;
}
</style>
