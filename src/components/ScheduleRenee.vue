<template>
  <section id="empresa" class="agenda">
    <div class="nome-empresa mobile">
        <img src="/img/Empresa.png" alt="Empresa" />
      </div>
    <div class="renee-img">
      <img src="/img/depositphotos.png" alt="" />
    </div>
    <div class="agendamento">
      <div class="nome-empresa desktop">
        <img src="/img/Empresa.png" alt="Empresa" />
      </div>
      <div class="content-text">
        <div class="text">
          <p>
            Com mais de 35 anos de experiência em camisas, calças e ternos sob
            medida, possuímos profissionais experientes e altamente
            qualificados.
          </p>
          <br>
          <p>
            Cada cliente tem seu molde exclusivamente desenvolvido para seu
            biotipo através das medidas tiradas pelo próprio Sr. Renee, no
            escritório ou residência do cliente.
          </p>
        </div>
        <div class="frase">
          <p>
            “Nosso objetivo é superar a expectativa do cliente
            proporcionando-lhe satisfação ao usar nossos produtos, aliado a um
            relacionamento franco e honesto, valorizando o ser humano.”
          </p>
        </div>
        <div class="aspas">
          <img src="/img/aspas.png" alt="aspas" />
        </div>
        <span class="text-desktop">Renee Trajar</span>
      </div>
      <div class="container-button">
        <ButtonComponent title="Agende uma visita!" link="#" />
      </div>
    </div>
    <div class="whats">
      <a href="#">
        <img src="/img/path4.png" alt="whats" />
      </a>
    </div>
  </section>
</template>

<script>
import ButtonComponent from "@/components/ButtonComponent";
export default {
  name: "ScheduleRenee",
  components: {
    ButtonComponent,
  },
};
</script>

<style scoped>
.agenda {
  display: flex;
  justify-content: space-around;
  margin: 52px auto;
  position: relative;
}

.renee-img {
  max-width: 370px;
  max-height: 439px;
}

.renee-img img {
  width: 100%;
}

.agendamento {
  max-width: 700px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.nome-empresa {
  max-width: 189px;
  max-height: 86px;
  position: relative;
}

.nome-empresa::after {
  content: "";
  position: absolute;
  width: 53px;
  height: 1px;
  background-color: #70b0c4;
  top: 50px;
  left: 70px;
}

.nome-empresa img {
  width: 100%;
}

.content-text {
  position: relative;
}

.content-text span {
  display: flex;
  justify-content: right;
  padding-right: 50px;
  width: 100%;
}

.agendamento .text {
  height: 135px;
  width: 700px;
  left: 568px;
  top: 779px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-top: 40px;
  margin-bottom: 27px;
}

.agendamento .text p {
  font-family: 'Lato';
  font-style: normal;
  font-weight: 300;
  font-size: 19px;
  line-height: 141.3%;
  color: #4F4F4F;
}

.agendamento .frase {
  width: 678px;
  height: 102px;
}

.agendamento .frase p {
  width: 100%;
  font-family: "Cormorant";
  font-size: 24px;
  font-style: italic;
  font-weight: 400;
  color: #1c86a4;
}

.agendamento span {
  font-family: "Cormorant";
  font-size: 20px;
  font-weight: 500;
  line-height: 28px;
  color: #828282;
}

.agende-btn {
  width: 300px;
}

.aspas {
  position: absolute;
  right: 0;
  z-index: -1;
  bottom: 50px;
}

.aspas img {
  height: 123px;
  width: 156px;
  left: 1168px;
  top: 902px;
}
.whats {
  position: absolute;
  width: 60px;
  height: 60px;
  background: #25d366;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  right: 38px;
  bottom: 445px;
  cursor: pointer;
}

.whats img {
  width: 31.81px;
  height: 32px;
}

.mobile {
  display: none;
}

@media screen and (max-width: 1200px) {
  .agenda {
    flex-direction: column;
    align-items: center;
  }
}

@media screen and (max-width: 999px) {
  .desktop, .aspas {
    display: none;
  }
  .mobile {
    display: block;
  }
  .nome-empresa {
    margin-bottom: 50px;
  }
  .whats {
    top: -80px;
  }
  .container-button {
    margin: 0 auto;
    display: table;
  }
  .renee-img {
    width: 100%;
    max-width: 100%;
    max-height: 100%;
  }
  .content-text, .renee-img {
    padding: 0 20px;
  }
  .content-text span {
    justify-content: center;
    margin-top: 20px;
    margin-bottom: 20px;
    padding: 0;
  }
  .agendamento .text {
    width: 100%;
    height: auto;
  }
  .agendamento .frase {
    width: 100%;
    height: auto;
  }
}
</style>