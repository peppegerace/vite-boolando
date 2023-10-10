<script>
export default {
  name: 'Footer'
}
</script>



<template>
  <footer>
    <div class="container">
      <div class="info">
        <h4>Boolando s.r.l</h4>
        <ul>
          <li>
            <a href="#">Infomazioni legali</a>
          </li>
          <ul>
            <li>
              <a href="#">Informazioni sulla privacy</a>
            </li>
            <li>
              <a href="#">Diritto di recesso</a>
            </li>
          </ul>
        </ul>
      </div>

      <div class="social">
        <h6>Trovaci anche su</h6>
        <ul>
          <li>
            <a href="#"><i class="fa-brands fa-twitter"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa-brands fa-square-facebook"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa-brands fa-square-instagram"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa-brands fa-square-pinterest"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa-brands fa-square-youtube"></i></a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>

@use '../scss/main.scss' as *;


footer{
  background-color: $bg-color-footer;
  color: white;
  padding: 20px 0;
  .container{
    display: flex;
    justify-content: space-between;
    .info {
      ul {
        display: flex;
        li {
          font-size: 0.7rem;
        }
      }
    }
    
    li {
      display: inline;
      margin-right: 10px;
      a {
        color: white;
      }
    }
  }
}

</style>