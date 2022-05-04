<template>
  <div class="details">
    <div class="infoContainer">
      <div class="infoSingle">
        <h2>60 mil</h2>
        <span>Transações suspeitas</span>
      </div>
      <div class="infoSingle">
        <h2>250 mil</h2>
        <span>Transações suspeitas</span>
      </div>
      <div class="infoSingle">
        <h2>45 mil</h2>
        <span>Transações suspeitas</span>
      </div>
    </div>

    <div class="aboutContainer">
      <div class="aboutDataLeft">
        <h2>
          Inteligência artificial que <br>
          <span>mantém você seguro</span>
        </h2>

        <div class="box">
          <p>
            Pix.IA é um Scrapper, ou seja, uma inteligência artificial que não necessita de
            API ou banco de dados para realizar consultas, pode extrair dados diretamente
            do ambiente web, visitando portais, filtrando informações para JSON ou
            transformando em tabelas csv, baixando e lendo documentos e planilhas.
          </p>
          <img src="~/static/hero_model_two.png" alt="Robo da Resolv">
        </div>
      </div>
      <div class="aboutDataRight">
        <p>
          Seu motor de cálculo terá a mesma potência, refinamento e confiança do
          CONSULTA ÓBITO, ou seja, Pix.IA irá validar as informações em mais de 30
          serviços e portais diferentes, que vão desde o reclame aqui, até o open data
          do governo federal, voltando e refinando a consulta a cada informação levantada.
        </p>

        <button>
          Saiba mais
        </button>

        <div class="linksContainer">
          <h2>Novos lançamentos</h2>
          <p>
            Lorem ipsum solor dolor monn
          </p>
        </div>
        <div class="linksContainer">
          <h2>Novos lançamentos</h2>
          <p>
            Lorem ipsum solor dolor monn
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'DetailsItem',
  data: () => {
    return {}
  },
  methods: {}
}
</script>

<style lang="scss">
  .details {
    background-color: white;
    border-radius: 5rem 5rem 0 0;

    padding: 2rem;

    .infoContainer {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      border-bottom: 1px solid #C4C4C4;
      padding-bottom: 2rem;

      .infoSingle {
        display: flex;
        flex-direction: column;
        align-items: center;

        padding: 2rem 0;

        &:nth-of-type(1),
        &:nth-of-type(2) {
          border-right: 1px solid #C4C4C4;
        }

        h2, span {
          color: #595959;
        }

        h2 {
          font-size: 2.7rem;
          font-weight: 600;
        }

        span {
          font-size: 1rem;
        }
      }
    }

    .aboutContainer {
      margin-top: 5rem;
      display: flex;
      align-items: center;
      padding: 0 1rem;

      .aboutDataLeft {
        flex: 1.2;

        h2 {
          font-size: 2rem;
          font-weight: 600;

          color: #595959;
          line-height: 37px;

          span {
            color: #009B90;
          }
        }

        .box {
          background-color: #009B90;
          color: white;

          margin-top: 2.2rem;
          margin-right: 9rem;
          padding: 1.2rem 4rem 1.2rem 1.2rem;

          border: 4px solid #40CEC3;
          position: relative;

          p {
            font-size: 1.1rem;
          }

          img {
            position: absolute;
            right: -155px;
            top: 50%;
            width: 230px;

            transform: translateY(-50%);
          }
        }
      }

      .aboutDataRight {
        flex: 1;

        p {
          font-size: 1rem;
          color: #595959;
        }

        button {
          margin-top: 2rem;
          background-color: #009B90;
          color: white;

          padding: 1rem 2rem;
          border-radius: 1.4rem;

          transition: filter 0.2s ease-in-out;

          &:hover {
            filter: brightness(0.9);
          }
        }

        .linksContainer {
          margin-top: 2rem;

          h2 {
            color: #009B90;
            font-size: 1rem;
            font-weight: 400;
          }

          p {
            font-size: 0.9rem;
            color: black;
            opacity: 0.45;
          }
        }
      }

    }
  }
</style>
