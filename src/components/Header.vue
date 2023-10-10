<script>
import chooseSection from '../data/chooseSection'
import iconList from '../data/iconList'

export default {
  name: 'Header',
  data() {
    return {
      chooseSection,
      iconList
    }
  }
}
</script>



<template>
  <header>
    <div class="top-bar container">
      <div class="menu">
        <ul>
          <li
            v-for="(item, index) in chooseSection"
            :key="index">
            <a :href="item.href">{{ item.text }}</a>
          </li>
      </ul>
      </div>
      <div class="logo">
        <img src="/boolean-logo.png" alt="boolean-logo">
      </div>
  
      <div class="shop">
        <ul>
          <li
            v-for="(item, index) in iconList"
            :key="index">
            <a :href="item.href"><i :class="item.icon"></i></a>
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