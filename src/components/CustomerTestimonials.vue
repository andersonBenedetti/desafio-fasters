<template>
  <section id="depoimentos" class="depoimentos">
    <img class="banner" src="/img/image14.png" alt="Banner" />
    <div class="container">
      <div class="title">
        <h1>Depoimentos</h1>
      </div>
      <div class="foto">
        <img v-if="testimonials[currentIndex]" :src="testimonials[currentIndex].image" alt="foto" />
      </div>
      <div class="setas">
        <img
          class="seta seta-esquerda"
          src="/img/Vector4.png"
          alt="seta"
          @click="prev"
        />
        <div class="text">
          <p v-if="testimonials[currentIndex]">{{ testimonials[currentIndex].text }}</p>
        </div>
        <img
          class="seta seta-direita"
          src="/img/Vector4.png"
          alt="seta"
          @click="next"
        />
      </div>
      <div class="info">
        <p v-if="testimonials[currentIndex]">{{ testimonials[currentIndex].nome }}</p>
        <span>{{ testimonials[currentIndex].empresa }}</span>
      </div>
      <div class="ciculos">
        <div v-for="i in testimonials.length" :key="i">
          <div v-if="currentIndex + 1 === i" class="circulo active"></div>
          <div v-else class="circulo"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "CustomerTestimonials",
  data() {
    return {
      pos: 0,
      timer: null,
      currentIndex: 0,
      testimonials: [
        {
          image: "/img/Ellipse.png",
          text: "“Sou cliente do Renee há uns 12 anos. Nosso primeiro contato foi por intermédio de meu pai, que já tem uma história de décadas com oquerido Renee. O excelente atendimento antes e pós venda e a alta qualidade dos materiais usados colocam a Renee Trajar em um patamar acima dos demais do ramo.”",
          nome: "William H. M. Garey",
          empresa: "Advogado  |   Nelson Garey Advogados Associados",
        },
        {
          image: "/img/Ellipse2.png",
          text: "“Há mais de 10 anos sou cliente da Renee Trajar. A qualidade, caimento e possibilidade de customização das roupas, aliados ao excelente atendimento e prazo de entrega são fatores decisivos para mim.”",
          nome: "Josimar Henrique da Silva",
          empresa: "Diretor Presidente  |  Grupo Hebron",
        },
        {
          image: "/img/Ellipse3.png",
          text: "“Seu corte tanto de camisas, bem como de ternos são impecáveis, muitos dos meus amigos tem elogiado a vestimenta. Recomendo para quem gosta de perfeição. Estamos nos servindo do trabalho do Renee Trajar há mais de vinte anos.”",
          nome: "Domingos Orestes Chiomento",
          empresa: "DOC Contabilidade Empresarial",
        },
        {
          image: "/img/Ellipse4.png",
          text: "“Tenho a honra de afirmar que enquanto nossas vidas perdurarem o meu conceito é sempre melhor em relação ao Renee Trajar, sua pessoa, ao profissional competente e idôneo, sempre pontual, atencioso e preocupado em atender da melhor maneira os anseios de seus clientes, incluindo este signatário.”",
          nome: "José Mauro Marques",
          empresa: "Advogado",
        },
        {
          image: "/img/Ellipse5.png",
          text: "“Conheço o excelente e qualificado trabalho do Renee Trajar e sua equipe há décadas. Para camisas e ternos, o Renee é imbatível, sempre com preços justos, produtos de excelente qualidade e especialmente tudo é feito com muito cuidado e qualidade. Cumpre os prazos com atendimento de alto nível. O Renee trabalha com perfeição nos detalhes.”",
          nome: "Custódio Pereira",
          empresa:
            "Membro do CONSOCIAL - Conselho Superior de Responsabilidade Social da FIESP-SP",
        },
      ],
    };
  },
  methods: {
    startSlide: function () {
      this.timer = setInterval(this.next, 4000);
    },
    next: function () {
      this.currentIndex += 1;
    },
    prev: function () {
      this.currentIndex -= 1;
    },
  },
  mounted: function () {
    this.startSlide();
  },
};
</script>

<style scoped>
.depoimentos {
  position: relative;
  width: 100%;
}

.banner {
  width: 100%;
  background-color: rgba(12, 42, 56);
}

.container {
  max-width: 1064px;
  height: 462px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  position: absolute;
  top: 0px;
  transform: translate(-50%, -50%);
  top: 50%;
  left: 50%;
}

.title {
  display: flex;
  justify-content: center;

  position: relative;
}
.title::after {
  content: "";
  position: absolute;
  width: 53px;
  height: 1px;
  background-color: #70b0c4;
  top: 60px;
}

.title h1 {
  font-family: "Cormorant";
  font-weight: 300;
  font-size: 38px;
  line-height: 46px;
  color: #f2f2f2;
}

.foto {
  margin: 0 auto;
  align-items: center;
  height: 121px;
  width: 121px;
  position: relative;
  z-index: 2;
}

.foto::before {
  content: "";
  position: absolute;
  background-color: #be9667;
  border-radius: 50%;
  height: 125px;
  width: 125px;
  z-index: -1;
  right: -2px;
  top: -2px;
}

.text {
  width: 800px;
  height: 124px;
  margin: 0 auto;
}

.text p {
  font-family: "Cormorant";
  font-size: 26px;
  font-style: italic;
  font-weight: 300;
  line-height: 31px;
  text-align: center;
  color: #c4c4c4;
}

.setas {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
}

.seta {
  height: 51px;
  width: 17px;
  cursor: pointer;
}

.seta-esquerda {
  transform: rotate(180deg);
  position: absolute;
  left: -138px;
}

.seta-direita {
  position: absolute;
  right: -138px;
}

.info {
  text-align: center;
}

.info p {
  font-family: "Cormorant";
  font-size: 20px;
  font-weight: 400;
  line-height: 24px;
  color: #be9667;
}

.info span {
  font-family: "Lato";
  font-weight: 300;
  font-size: 14px;
  line-height: 16.8px;
  color: #949494;
}

.ciculos {
  display: flex;
  width: 124px;
  justify-content: space-between;
  margin: 0 auto;
}

.circulo {
  width: 10px;
  height: 10px;
  border-radius: 50px;
  border: 2px solid #014561;
}

.active {
  background-color: #014561;
}

@media screen and (max-width: 1200px) {
  .banner {
    width: none;
    height: 782px;
  }

  .container {
    height: 659px;
  }

  .seta-esquerda {
    left: 125px;
    bottom: -104px;
  }
  .seta-direita {
    right: 125px;
    bottom: -104px;
  }

  .text {
    width: 500px;
    height: 329px;
    margin-bottom: 27px;
    font-size: 24px;
    line-height: 29px;
  }

  .info {
    margin-bottom: 30px;
  }

  .info p {
    font-size: 20px;
    line-height: 24px;
  }

  .info span {
    font-size: 14px;
    line-height: 17px;
  }
  .title h1 {
    margin-bottom: 60px;
  }
}

@media screen and (max-width: 602px) {
  .text {
    width: 329px;
  }

  .seta-esquerda {
    left: 70px;
    bottom: -112px;
  }
  .seta-direita {
    right: 70px;
    bottom: -112px;
  }
}
</style>