<template>
  <div style="text-align:center">
    <p> 放映中の映画一覧 </p>
    <p> {{ ip }} </p>
    <button @click="getIp"> 映画一覧を取得 </button>
  </div>
</template>


<script>
export default {
  data: function(){
    return {
      ip: 'リスト(json)'
    }
  } ,
  methods: {
    async getIp(){
      this.ip = await this.$axios.$get(`https://api.themoviedb.org/3/movie/now_playing?api_key=${process.env.MOVIEDB_KEY}`);
    }
  }
}
</script>