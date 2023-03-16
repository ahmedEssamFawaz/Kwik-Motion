<template>
   <h2 class="rightContent" :style="{'background':backGround}">
        <span>{{text}}</span>
      </h2>
</template>

<script lang="ts">
    import Vue from 'vue'

    export default Vue.extend({
        props:{
            backGround:{
                type:String,
                required:true
            },
            text:{
                type:String,
                required:false
            }
        }
    })
</script>

<style scoped lang="scss">
.rightContent {
  background: url("~/assets/imgs/presentation-section/Group-791.png");
  line-height: 1.4;
  padding: 20px 107px 121px 50px;
  width: 400px;
  margin: 20px auto;
  background-repeat: no-repeat;
  position: relative;
  span{
    font-size: 20px;
  color: #333;
  text-transform: uppercase;
  font-weight: bold;
  position: relative;
    right: 29px;
    top: 25px;
  }
}
</style>