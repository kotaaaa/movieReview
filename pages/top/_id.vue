<template>
<div>
<h1> 映画チャンネル　detail page </h1>
<p>これは，{{ $route.params.id }} のエントリーです．</p>
</div>
</template>
<script> 
export default {
  validate( { params } ){
    return /^\d+$/.test(params.id)
  }
}
</script>
