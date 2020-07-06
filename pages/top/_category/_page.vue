<template>
<div>
<p>これは，{{ $route.params.category}} の {{ $route.params.page }} ページ目です．</p>
</div>
</template>


<script> 
export default {
  validate( { params } ){
    return /^\d+$/.test(params.page)
  }
}
</script>