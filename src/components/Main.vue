<script>
import ProductCard from './partials/ProductCard.vue';
import cardInfo from '../data/cardInfo'

export default {
  name: 'Main',
  components: {
    ProductCard
  },
  data() {
    return {
      cardInfo
    }
  }
}
</script>


<template>
  <main>
    <div class="container">
      <div class="cards">

        <ProductCard
          v-for="info in cardInfo"
          :key="info.id"
          :image="info.image" 
          :imageHover="info.imageHover"
          :sales="info.sales"
          :green="info.green"
          :brand="info.brand"
          :info="info.info"
          :salesPrice="info.salesPrice"
          :originalPrice="info.originalPrice" />

      </div>
    </div>
  </main>
</template>

<style lang="scss">

@use '../scss/main.scss' as *;

main {
  padding-top: 100px;
  .cards{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    .card {
      width: calc(100% / 3 - 40px);
      min-width: 250px;
      margin: 20px;
      &:hover {
        cursor:pointer;
      }
      top-card img {
        max-width: 100%;
      }
      
      .top-card {
        position: relative;
        .image-change {
          display: block;
        }

        .image-change2 {
          display: none;
        }

        &:hover .image-change {
          display: none;
        }

        &:hover .image-change2 {
          display: block;
        }

        .heart {
          font-size: 1.3rem;
          background-color: white;
          padding: 10px;
          position: absolute;
          top: 10px;
          right: 0;
          &:hover {
            color: red;
          }
        }
        .rectangle {
          position: absolute;
          bottom: 50px;
          color: white;
          font-size: 0.7rem;
        }

        .sales {
          background-color: red;
          padding: 3px 8px;
        }

        .eco-friendly {
          background-color: $green;
          padding: 3px 8px;
        }
      }
      .bottom-card {
        .font-small{
          font-weight: 400;
        }

        .brand {
          display: block;
          font-size: 0.8rem;
        }

        .price-new {
          color: red;
          margin-right: 10px;
        }
      }
    }
  }
}

</style>