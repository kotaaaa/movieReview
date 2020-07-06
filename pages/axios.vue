<template>
  <div style="text-align:center">
    <p> {{ ip }} </p>
    <button @click="getIp"> IP アドレスを取得 </button>
  </div>
</template>


<script>
export default {
  data: function(){
    return {
      ip: '0.0.0.0'
    }
  } ,
  methods: {
    async getIp(){
      this.ip = await this.$axios.$get('http://icanhazip.com')
      // this.ip = await this.$axios.$get('https://api.themoviedb.org/3/movie/now_playing?api_key=0534930d6692ebb101db3214a44bcfe7')
      
    }
  }
}
</script>