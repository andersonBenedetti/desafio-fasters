<template>
  <div>
    <header>
      <nav class="menu-desktop">
        <div class="logo">
          <img src="/img/logo.png" alt="Logo" />
        </div>
        <img class="menu" src="/img/Vector5.png" alt="menu" @click="showMenu" />
        <ul>
          <li><a href="#empresa">Empresa</a></li>
          <li><a href="#camisaria">Camisaria</a></li>
          <li><a href="#alfaiataria">alfaiataria</a></li>
          <li><a href="#depoimentos">Depoimentos</a></li>
          <li><a href="#contato">Contato</a></li>
        </ul>
      </nav>
    </header>
    <MobileComponent :active="activeMenu" @closeMenu="activeMenu = false" />
  </div>
</template>

<script>
import MobileComponent from "./MobileComponent";
export default {
  name: "HeaderComponent",
  components: {
    MobileComponent,
  },
  data: function () {
    return {
      activeMenu: false,
    };
  },
  methods: {
    showMenu: function () {
      this.activeMenu = !this.activeMenu;
    },
  },
};
</script>

<style scoped>
header {
  max-width: 100%;
  height: 111px;
  display: flex;
  align-items: center;
  background: linear-gradient(180deg, #000000 29.73%, rgba(0, 0, 0, 0) 100%);
  position: absolute;
  z-index: 9999;
  width: 100%;
}

nav.menu-desktop {
  width: 1420px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: relative;
}
.logo {
  width: 121.8px;
  height: 54.26px;
}

.logo img {
  width: 100%;
}

.menu {
  display: none;
  cursor: pointer;
  height: 25px;
  width: 34.6px;
  position: absolute;
  right: 58px;
  bottom: 50px;
}

.menu img {
  width: 100%;
}

ul {
  display: flex;
  justify-content: space-between;
}

a {
  color: #949494;
}

li {
  font-size: 16px;
  line-height: 19px;
  text-transform: uppercase;
  margin-right: 29px;
  cursor: pointer;
  font-family: "Lato", sans-serif;
  transition: all 0.2s ease 0s;
}

li:hover {
  color: #014561;
}

@media screen and (max-width: 900px) {
  nav.menu-desktop ul {
    display: none;
  }

  nav.menu-desktop {
    display: flex;
    justify-content: center;
  }

  header {
    height: 160px;
    background-color: #0a0a0a;
  }
  .menu {
    display: block;
  }
}

@media screen and (max-width: 400px) {
  header {
    position: initial;
  }
  nav.menu-desktop {
    justify-content: left;
    padding-left: 20px;
  }
  .menu {
    bottom: initial;
  }
}
</style>