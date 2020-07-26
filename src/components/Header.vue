<template lang="pug">
nav.navbar(role="navigation")
  .navbar-brand
    a.navbar-item
      img(src="../assets/logo-es.jpg")
  .navbar-menu
    .navbar-start
      a.navbar-item Home
    .navbar-end
      .navbar-item
        .buttons
          a.button.is-primary
            strong Sign up
          a.button.is-ligth
            strong Log in
</template>
<script>
export default {
  name: 'Header'
}
</script>
<style lang="scss">
@import '../scss/main.scss';
.navbar{
  position: fixed !important;
  width: 100%;
}
</style>
