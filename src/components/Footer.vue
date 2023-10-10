<script>
import infoFooter from '../data/infoFooter'
import iconFooter from '../data/iconFooter'

export default {
  name: 'Footer',
  data() {
    return {
      infoFooter,
      iconFooter
    }
  }
}
</script>



<template>
  <footer>
    <div class="container">
      <div class="info">
        <h4>Boolando s.r.l</h4>
        <ul>
          <li
            v-for="(item, index) in infoFooter"
            :key="index">
            <a :href="item.href">{{ item.text }}</a>
          </li>
        </ul>
      </div>

      <div class="social">
        <h6>Trovaci anche su</h6>
        <ul>
          <li
            v-for="(item, index) in iconFooter"
            :key="index">
            <a :href="item.href"><i :class="item.icon"></i></a>
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