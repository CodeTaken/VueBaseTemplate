<template>
  <div id="app">
    <div class="logo" v-if="logo">
      <div class="content">
        <img :src="logo" id="logo_imageUrl" />
      </div>
    </div>

    <router-view v-wechat-title="$route.meta.title" />

  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
      return {
        logo:'',
      }
  },
  components:{
  },
  watch:{
    logo(){
        this.logo = this.activityAllMessage.activityInfo.Banner?this.activityAllMessage.activityInfo.Banner:''
    }
  },
  mounted(){
  },
  computed:{
  }
}
</script>

<style>

</style>
