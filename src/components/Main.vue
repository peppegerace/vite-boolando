<script>
export default {
  name: 'Main',
}
</script>


<template>
  <main>
    <div class="container">
      <div class="cards">

        <!-- card levi's -->
        <div class="card">
          <div class="top-card">
            <img class="image-change" src="../assets/img/1.webp" alt="t-shirt">
            <img class="image-change2" src="../assets/img/1b.webp" alt="">
            <span class="heart">&hearts;</span>
            <div class="rectangle">
              <span class="sales">-50%</span>
              <span class="eco-friendly">Sostenibilità</span>
            </div>
          </div>
          <div class="bottom-card">
            <span class="brand font-small">Levi's</span>
            <span>RELAXED FIT TEE UNISEX</span>
            <div>
              <span class="price-new">14,99 &euro;</span>
              <span class="font-small"><s>29,99 &euro;</s></span>
            </div>
          </div>
        </div>


        <!-- card guess -->
        <div class="card">
          <div class="top-card">
            <img class="image-change" src="../assets/img/2.webp" alt="t-shirt">
            <img class="image-change2" src="../assets/img/2b.webp" alt="">
            <span class="heart">&hearts;</span>
            <div class="rectangle">
              <span class="sales">-30%</span>
            </div>
          </div>
          <div class="bottom-card">
            <span class="brand font-small">Guess</span>
            <span>ROSES TEE</span>
            <div>
              <span class="price-new">20,99 &euro;</span>
              <span class="font-small"><s>29,99 &euro;</s></span>
            </div>
          </div>
        </div>

        <!-- card come zucchero filato -->
        <div class="card">
          <div class="top-card">
            <img class="image-change" src="../assets/img/3.webp" alt="t-shirt">
            <img class="image-change2" src="../assets/img/3b.webp" alt="">
            <span class="heart">&hearts;</span>
            <div class="rectangle">
              <span class="sales">-30%</span>
            </div>
          </div>
          <div class="bottom-card">
            <span class="brand font-small">Come Zucchero Filato</span>
            <span>VOGLIA DI COLORI PASTELLO</span>
            <div>
              <span class="price-new">129,99 &euro;</span>
              <span class="font-small"><s>184,99 &euro;</s></span>
            </div>
          </div>
        </div>

        <!-- card levi's -->
        <div class="card">
          <div class="top-card">
            <img class="image-change" src="../assets/img/4.webp" alt="t-shirt">
            <img class="image-change2" src="../assets/img/4b.webp" alt="">
            <span class="heart">&hearts;</span>
            <div class="rectangle">
              <span class="sales">-50%</span>
              <span class="eco-friendly">Sostenibilità</span>
            </div>
          </div>
          <div class="bottom-card">
            <span class="brand font-small">Levi's</span>
            <span>TEE UNISEX</span>
            <div>
              <span class="price-new">14,99 &euro;</span>
              <span class="font-small"><s>29,99 &euro;</s></span>
            </div>
          </div>
        </div>

        <!-- card maya deluxe -->
        <div class="card">
          <div class="top-card">
            <img class="image-change" src="../assets/img/5.webp" alt="t-shirt">
            <img class="image-change2" src="../assets/img/5b.webp" alt="">
            <span class="heart">&hearts;</span>
          </div>
          <div class="bottom-card">
            <span class="brand font-small">Maya Deluxe</span>
            <span>STRIPE BODICE</span>
            <div>
              <span class="price-new">99,99 &euro;</span>
            </div>
          </div>
        </div>

      <!-- card espirit -->
        <div class="card">
          <div class="top-card">
            <img class="image-change" src="../assets/img/6.webp" alt="t-shirt">
            <img class="image-change2" src="../assets/img/6b.webp" alt="">
            <span class="heart">&hearts;</span>
            <div class="rectangle">
              <span class="eco-friendly">Sostenibilità</span>
            </div>
          </div>
          <div class="bottom-card">
            <span class="brand font-small">Espirit</span>
            <span>MAGLIONE - BLACK</span>
            <div>
              <span class="price-new">29,99 &euro;</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>

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
        }
      }
    }
  }
}

</style>