<template>
  <footer class="footer">
    <Logo />
  </footer>
</template>

<script>
export default {
  name: 'FooterItem'
}
</script>

<style lang="scss">
  .footer {
    width: 100%;
    background: rgba(0, 155, 144, 0.06);
    box-shadow: 0px 3px 58px rgba(0, 0, 0, 0.06);
    backdrop-filter: blur(22px);
    height: 5.5rem;

    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
