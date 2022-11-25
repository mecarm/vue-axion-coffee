<template>
  <div class="cardse">
    <img :src="dettaggliCoffe.image" alt="">
    <h1>{{dettaggliCoffe.title}}</h1>
    <p>{{dettaggliCoffe.description}}</p>
    <div>{{dettaggliCoffe.ingredients}}</div>
  </div>
</template>

<script>
export default {
  name: 'MainComp',
  props: {  
    dettaggliCoffe: Object
  }
}
</script>

<style scoped lang="scss">
.cardse{
  width: calc((100% / 4) - 40px);
  margin: 20px;

  p, div{
    text-align: start;
  }

  img{
    width: 100%;
    aspect-ratio: 1/1;
  }
}
</style>
