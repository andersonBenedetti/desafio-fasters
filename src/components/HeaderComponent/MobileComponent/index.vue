<template>
    <nav v-if="active" class="menu-mobile">
        <img src="img/close.svg" class="close" @click="closeMenu"/>
        <ul>
          <li><a href="#empresa" @click="closeMenu">Empresa</a></li>
          <li><a href="#camisaria" @click="closeMenu">Camisaria</a></li>
          <li><a href="#alfaiataria" @click="closeMenu">alfaiataria</a></li>
          <li><a href="#depoimentos" @click="closeMenu">Depoimentos</a></li>
         <li><a href="#contato" @click="closeMenu">Contato</a></li>
        </ul>

        <div class="infos">
            <p>Telefones</p>
            <span>
                <a href="tel:+551130880757">+55 (11) 3088-0757</a>
            </span>

            <p>E-mail</p>
            <span>
                <a href="malito:renee@reneetrajar.com.br">renee@reneetrajar.com.br</a>
            </span>
        </div>
    </nav>
</template>

<script>
export default {
  name: "MobileMenu",
  props: ["active"],
  emits: ['closeMenu'],
  methods: {
      closeMenu: function() {
          this.$emit('closeMenu');
      }
  }
};
</script>

<style scoped>
nav.menu-mobile img.close {
    position: absolute;
    right: 40px;
    cursor: pointer;
    top: 25px;
}

nav.menu-mobile {
    position: fixed;
    width: 100%;
    height: 100%;
    background-color: #024B68;
    z-index: 9999;
    left: 0;
    padding: 50px 20px;
    top: 0;
}
nav.menu-mobile li > a{
    color: #BE9667;
    font-family: 'Lato';
    font-style: normal;
    font-weight: 300;
    font-size: 26px;
    line-height: 31px;
    text-align: center;
    text-transform: uppercase;
}
nav.menu-mobile li {
    padding-bottom: 25px;
    text-align: center;
}
.infos {
    width: 100%;
    display: flex;
    align-items: center;
    flex-direction: column;
}
.infos p {
    font-family: 'Lato';
    font-style: normal;
    font-weight: 300;
    font-size: 18px;
    line-height: 22px;
    text-align: center;
    text-transform: uppercase;
    color: #1C86A4;
    margin-top: 15px;
    margin-bottom: 10px;
}
.infos a {
    font-family: 'Lato';
    font-style: normal;
    font-weight: 300;
    font-size: 18px;
    line-height: 22px;
    text-align: center;
    color: #828282;
}
</style>