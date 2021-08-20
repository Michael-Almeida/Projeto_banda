<template>
  <div>
      aqui vai detalhe da noticia {{ $route.params.id}}
  </div>
</template>

<script>
export default {
    name: "NewsDetail",
    methods :{
        getUserById : function( id ){
            return id
        }
    }

}
</script>

<style>

</style>