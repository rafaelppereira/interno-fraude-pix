<template>
  <div class="banner">
    <div class="bannerData">
      <h2>
        Fraude pix veio para<br>
        <span>resolver</span> o risco de <br>
        <b>golpes e fraudes</b>
      </h2>
      <p>
        O meio de pagamento surgiu em 2020 e atualmente, 2 anos depois, o BACEN
        já registrou mais de 60 mil transações suspeitas e fraudulentas/mês. O sistema
        financeiro nacional ainda estuda métodos.
      </p>
      <div class="buttonContainer">
        <button>Data de lançamento</button>
      </div>

      <span>A mais de 8 anos no mercado que a Resolv trás soluções de segurança</span>
    </div>

    <div class="bannerImage">
      <img src="~/static/hero.png" alt="Fraude Pix Robo">
    </div>
  </div>
</template>

<script>

export default {
  name: 'BannerItem',
  data: () => ({

  }),
  methods: {}
}
</script>

<style lang="scss">
  .banner {
    width: 100%;
    height: calc(100vh - 5.5rem);

    display: flex;
    align-items: center;

    .bannerData {
      flex: 1;
      color: white;

      h2 {
        font-size: 3.1rem;
        line-height: 65px;
        font-weight: 600;

        span {
          color: #009B90;
          font-weight: 700;
        }
      }

      b {
        font-weight: 600;
        position: relative;

        &:before {
          content: '';
          position: absolute;
          left: 0;
          bottom: -12px;

          width: 100%;
          height: 3px;
          background-color: #009B90;

          border-radius: 10rem;
        }
      }

      p {
        margin-top: 2.3rem;
        font-weight: 300;
        font-size: 0.9rem;
      }

      .buttonContainer {
        display: flex;
        align-items: center;
        gap: 20px;
        margin-top: 3rem;

        button {
          background-color: #009B90;
          color: white;

          padding: 0.8rem 2rem;
          border-radius: 0.5rem;
          transition: filter 0.2s;

          &:hover {
            filter: brightness(0.9);
          }
        }
      }

      > span {
        font-weight: 200;
        opacity: 0.3;
        margin-top: 3rem;
        display: inline-flex;
      }
    }

    .bannerImage {
      flex: 1;
      display: flex;
      justify-content: center;

      img {
        width: 90%;
      }
    }

    @media (max-width: 1100px) {
      flex-direction: column;
      height: auto;
      padding: 5rem 0;

      .bannerData {
        h2 {
          font-size: 2.8rem;
          line-height: 60px;
        }
      }

      .bannerImage img {
        width: 100%;

        margin-top: 2rem;
      }
    }

    @media (max-width: 462px) {
      .bannerData {
        h2 {
          font-size: 2.4rem;
          line-height: 50px;
        }
      }
    }

    @media (max-width: 404px) {
      .bannerData h2 {
        font-size: 2.2rem;
        line-height: 45px;
      }
    }

  }
</style>
