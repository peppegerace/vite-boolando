<script>
export default {
  name: 'Header'
}
</script>



<template>
  <header>
    <div class="top-bar container">
      <div class="menu">
        <ul>
          <li>
            <a href="#">Donna</a>
          </li>
          <li>
            <a href="#">Uomo</a>
          </li>
          <li>
            <a href="#">Bambini</a>
          </li>
      </ul>
      </div>
      <div class="logo">
        <img src="/boolean-logo.png" alt="boolean-logo">
      </div>
  
      <div class="shop">
        <ul>
          <li>
            <a href="#"><i class="fa-regular fa-user"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa-regular fa-heart"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa-solid fa-bag-shopping"></i></a>
          </li>
      </ul>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>

@use '../scss/main.scss' as *;

header {
  background-color: $bg-color-header;
  padding: 10px;
  box-shadow: 0 5px 5px $shadow;
  position: fixed;
  width: 100%;
  z-index: 999;

    .logo {
    width: 100px;
    }

    .top-bar{
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
    }

    ul {
      display: flex;
      flex-direction: row;
    }

    .menu {
      li {
      margin-right: 5px;
      }
    }

    .shop {
      li {
      margin-left: 5px;
      }
    }

    a {
    color: white;
    }
}
</style>