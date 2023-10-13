<script>

  export default{
    name: "cardSection",

    props: {
    nameObj: String,
    typeObj: String,
    imageObj: String
  }
  }
</script>

<template>
    <!-- carte -->
    <div class="card yugiCard text-center">
      <img :src="imageObj" 
      alt="nameObj">
      <h6>{{nameObj}}</h6>
      <p>{{typeObj}}</p>
    </div>

</template>

<style lang="scss" scoped>
  @use '../../scss/cardSection.scss' as *;
</style>