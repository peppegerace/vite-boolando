<script>
export default {
  name: 'ProductCard',
  props: {
    image: String,
    imageHover: String,
    sales: String,
    green: String,
    brand: String,
    info: String,
    salesPrice: String,
    originalPrice: String
  }
}

</script>


<template>

  <div class="card">
    <div class="top-card">
      <img class="image-change" :src="image" alt="">
      <img class="image-change2" :src="imageHover" alt="">
      <span class="heart">&hearts;</span>
      <div class="rectangle">
        <span class="sales" v-if="sales !== ''">{{ sales }}</span>
        <span class="eco-friendly" v-if="green !== ''">{{ green }}</span>
      </div>
    </div>
    <div class="bottom-card">
       <span class="brand font-small">{{ brand }}</span>
       <span>{{ info }}</span>
        <div>
           <span class="price-new">{{ salesPrice }}</span>
           <span class="font-small"><s>{{ originalPrice }}</s></span>
        </div>
    </div>
  </div>

</template>


<style>

</style>