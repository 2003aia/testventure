<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div class="wrapper-main">
    <header class="menu">

      <div class="logo-wrapper">
        <img alt="Venture logo" class="logo" src="@/assets/logo.svg" width="28" height="28" />
        VENTURE
        <!-- <HelloWorld msg="You did it!" /> -->
      </div>

      <nav class="menu-list">

        <RouterLink to="/">
          <div class="menu-item"><img src="@/assets/Vehicles.svg" alt="Vehicles">Транспортный</div>
        </RouterLink>
        <RouterLink to="/about">
          <div class="menu-item"><img src="@/assets/Database.svg" alt="Vehicles">Рейсовый</div>
        </RouterLink>
        <RouterLink to="/production">
          <div class="menu-item"><img src="@/assets/Buildings.svg" alt="Vehicles">Производство</div>
        </RouterLink>

      </nav>

    </header>
    <div class="content-wrapper">
      <div class="header">
        <div class="header-box">
          <h1 class="header-title">{{ currentRouteName }}</h1>
          <div class="btn-btx">Битрикс24</div>
        </div>

        <div class="header-box">
          <img src="@/assets/bell.svg" alt="bell" class="bell">
          <span class="name">Ярослав П.</span>
          <img src="@/assets/Avatars.png" alt="avatar" class="avatar">
        </div>
      </div>

      <div class="container">
        <RouterView />
      </div>

    </div>
  </div>

</template>
<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increment() {
      this.count++
    }
  },
  computed: {
    currentRouteName() {
      return this.$route.name;
    }
  },
  mounted() {
    console.log(`The initial count is ${this.count}.`)
  }
}
</script>
<style scoped>
.wrapper-main {
  background-color: #F6F6F8;
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: row;
}

.container {
  padding: 30px;
  /* background-color: #fff; */
  width: 100%;
}

.header {
  background: #fff;
  box-shadow: 0px -3px 26px 0px #16081E14;
  width: 100%;
  padding: 30px 15px;
  margin-bottom: 30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.header-box{
  display: flex;
  align-items: center;
}

.bell{
  margin-right: 30px;
}
.avatar{
margin-left: 10px;
}

.header-title {
  font-size: 16px;
  color: black;
  font-weight: 500;
  margin: 0;
}

.btn-btx {
  background-color: #41BBFF;
  border-radius: 15px;
  padding: 10px;
  text-align: center;
  margin-left: 10px;
  color: #fff;
}

.content-wrapper {
  width: 100%;
  display: flex;
  flex-direction: column;
}

.menu {
  background: #1E1E1E;
  padding: 15px;
  width: 30%;
}

.menu-list {
  display: flex;
  flex-direction: column;
}

.menu-item {
  padding: 8px;
  display: flex;
  flex-direction: row;
  font-weight: 500;
  font-size: 15px;
  color: #fff;
  align-items: center;

}

.menu-item img {
  margin-right: 5px;
}

a {
  text-decoration: none
}


.logo-wrapper {
  font-size: 20px;
  font-weight: 700;
  color: #fff;
  line-height: 23px;
  letter-spacing: 7%;
  display: flex;
  align-items: center;
  flex-direction: row;
  margin-bottom: 25px;
  margin-top: 10px;
}

.logo-wrapper img {
  margin-right: 10px;

}



@media (min-width: 1024px) {
  /* header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  } */
}
</style>
