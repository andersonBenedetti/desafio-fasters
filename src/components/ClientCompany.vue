<template>
  <section class="cliente">
    <div class="fundo">
      <div class="banner">
        <img src="/img/Tailor.png" alt="foto" />
      </div>
      <div class="foto">
        <img class="desktop" src="/img/MicrosoftTeams1.png" alt="foto" />
        <img class="mobile" src="/img/MicrosoftTeams2.png" alt="foto" />
      </div>
      <div class="foto2">
        <img src="/img/MicrosoftTeams.png" alt="foto" />
      </div>
    </div>
    <div class="container">
      <div class="text">
        <p>
          “Faço roupas com o Renee Trajar há mais de duas décadas, o serviço é
          impecável em todos os detalhes, desde a costura ao caimento. O Renee
          tem uma equipe de mestre!”
        </p>
      </div>
      <div class="info">
        <h2>Nelson Garey</h2>
        <span>Advogado | Nelson Garey Advogados Associados</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ClientCompany",
};
</script>

<style scoped>
.mobile {
  display: none;
}

.cliente {
  position: relative;
}

.fundo {
  display: flex;
  justify-content: space-between;
  max-height: 360px;
}

.banner {
  background: #eff7f9;
  width: 100%;
}
.banner img {
  width: 100%;
  height: 100%;
}

.fundo .foto {
  max-width: 313px;
  max-height: 360px;
  position: relative;
  background-color: #014561;
}

.fundo .foto img {
  width: 100%;
  height: 100%;
  filter: opacity(0.3);
}

.foto2 {
  position: absolute;
  right: 190px;
  max-height: 312.92px;
}

.foto2::before {
  content: "";
  position: absolute;
  border: 8px solid #ffffff;
  height: 310px;
  width: 218px;
  transform: rotate(7.42deg);
  top: 21px;
  left: 32px;
}

.foto2 img {
  height: 100%;
}

.container {
  height: 202px;
  max-width: 630px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  position: absolute;
  top: 90px;
  left: 168px;
}

.text {
  height: 102px;
  text-align: center;
}

.text p {
  font-size: 24px;
  line-height: 141.3%;
  color: #828282;
}

.info {
  text-align: center;
}

.info h2 {
  font-family: "Cormorant";
  font-style: italic;
  font-weight: 400;
  font-size: 28px;
  line-height: 141.3%;
  color: #014561;
}

.info span {
  font-size: 20px;
  line-height: 141.3%;
  color: #be9667;
}

@media screen and (max-width: 1200px) {
  .foto2 img {
    height: 290px;
  }
  .foto2::before {
    height: 239px;
    width: 166px;
    top: 15px;
    left: 23px;
  }
  .container {
    top: 65px;
    left: 3px;
  }
}

@media screen and (max-width: 950px) {
  .banner {
    display: none;
  }

  .container {
    position: initial;
    margin-top: 42px;
    margin-bottom: 80px;
    width: 100%;
    left: 0;
    top: 0;
    max-width: 100%;
    padding: 0 23px;
  }

  .text {
    height: auto;
  }

  .text p {
    font-size: 22px;
    line-height: 31px;
  }

  .info {
    margin-bottom: 42px;
  }

  .info h2 {
    margin-top: 21px;
  }

  .desktop {
    display: none;
  }

  .mobile {
    display: block;
    width: 100%;
  }

  .fundo .foto {
    max-width: 100%;
    width: 100%;
    max-height: 100%;
  }

  .foto2 {
    right: 0;
    width: 100%;
  }
}

@media screen and (max-width: 330px) {
  .container {
    margin-bottom: 165px;
    margin-top: 60px;
  }
}
</style>