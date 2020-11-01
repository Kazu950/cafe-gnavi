<template>
  <header class="header">
    <a src="#" class="header__logo">Near Cafe</a>
    <nav class="nav">
      <ul class="nav__list">
        <li class="nav__item" v-for="item in navigation" :key="item.index"><a href="#">{{ item }}</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
    data() {
        return {
            navigation: ['ホーム', '検索', 'お気に入り']
        }
    }
}
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  height: 70px;
  background-color: #e9c79f;
  display: flex;
  align-items: center;
  padding: 0 50px;
  &__logo {
      font-family: "serif";
      font-size: 28px;
      justify-content: center;
  }
  .nav{
      margin: 0 0 0 auto;
      &__list {
        align-items: center;
        display: flex;
      }
      &__item {
        font-size: 25px;
        margin-left: 55px;
        &:hover {
            // TODO：カーソルを合わせると下線を表示させる
            border-bottom: solid 1px #2c3e50;;
        }
      }
  }
}
</style>