<template>
  <section class="discografia">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h2>Discografia</h2>
        </div>
      </div>
      <div class="row">
        <div v-for="album in albuns" :key="album.name" class="col-md-3"> 
          <div class="discografia__card">
            <img :src="album.img" :alt="album.name">
            <h5 v-text="album.name"></h5>
            <a :href="album.link" target="__blank">Ouvir</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

export default {
    name: "Discografia",
    data: function(){
        return {
            albuns : [
                {
                    name: "Nada Pra Fazer",
                    img: require ("../assets/nada_pra_fazer.jpg"),
                    link: "https://www.youtube.com/watch?v=G5Atr7XmFN4"
                },
                {
                    name: "A Força do Som",
                    img: require("../assets/a_forca_do_som.jpg"),
                    link: "https://www.youtube.com/watch?v=F68KkgwP5F8"
                },
                {
                    name: "Novelas",
                    img: require("../assets/novelas.jpg"),
                    link: "https://www.youtube.com/watch?v=k_eqQGzPH1k"
                },
                {
                    name: "Eu volto para almoçar",
                    img: require("../assets/eu_volto_para_almocar.jpg"),
                    link: "https://www.youtube.com/watch?v=k_eqQGzPH1k"
                }
            ]
        }
    }
}
</script>
<style>
.discografia { 
    padding : 56px 0; 
    background-color: #212121; 
    color: #e2e2e2; 
  } 
 
  .discografia h2 { 
    padding-bottom : 30px; 
  } 
 
  .discografia__card{ 
    display: flex; 
    flex-direction : column; 
    justify-content: center; 
    align-items: center; 
    height: 340px; 
  } 
 
  .discografia__card img{ 
    width: 100%; 
    max-width: 193px; 
    height: 193px; 
  } 
 
  .discografia__card a{ 
    display: block; 
    width: 70px; 
    height : 30px; 
    background-color: #e2e2e2; 
    color: #212121; 
    text-align: center; 
    text-decoration : none; 
    line-height: 31px; 
    margin-top: 10px; 
    margin-bottom: 30px; 
    border-radius: 6px; 
    font-size: 14px; 
    font-weight: 900; 
  } 
 
  .discografia__card h5{ 
    font-size: 16px; 
    text-align: center; 
    padding: 0px; 
    display: inline-block; 
    max-width : 120px; 
    margin: auto 
  } 
</style>
