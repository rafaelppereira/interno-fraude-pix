<template>
  <header>
    <div class="container">
      <Logo />
      <div class="menu">
        <li class="active">
          Home
        </li>
        <li>Parceiros</li>
        <li>Sobre</li>
        <li>Contato</li>
      </div>
      <div class="buttonContainer">
        <button>
          Conhecer a Resolv
        </button>
      </div>
    </div>
  </header>
</template>

<script>

export default {
  name: 'HeaderItem',
  data () {
    return {

    }
  },
  methods: {}
}
</script>

<style lang="scss">
  header {
    width: 100%;
    background: rgba(0, 155, 144, 0.06);
    box-shadow: 0px 3px 58px rgba(0, 0, 0, 0.06);
    backdrop-filter: blur(22px);
    height: 5.5rem;

    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 2rem;
      height: inherit;

      display: flex;
      align-items: center;
      justify-content: space-between;

      .menu {
        display: flex;
        list-style: none;

        li {
          padding: 0 0.6rem;
          opacity: 0.6;
          color: white;

          font-weight: 300;
          font-size: 0.95rem;

          cursor: pointer;

          transition: opacity 0.2s;
          &:hover {
            opacity: 0.3;
          }

          &.active {
            color: #009B90;
            font-weight: 500;
          }
        }
      }

      button {
        background-color: #009B90;
        color: white;

        padding: 0 1.2rem;
        height: 2.6rem;
        line-height: 2.6rem;

        margin: 0.2rem;
        display: inline-flex;

        border-radius: 0.5rem;
        border-bottom: 4px solid #0C7169;
        transition: filter 0.2s ease-in-out;

        &:hover {
          filter: brightness(0.9);
        }
      }
    }
  }
</style>
