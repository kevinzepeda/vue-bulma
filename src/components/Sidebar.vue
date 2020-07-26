<template lang="pug">
.column.is-1
  .panel.background-side
    ul.margin
      li
        a Dashboard
      li
        a Movies
      li
        a Settings
</template>

<script>
export default {
  name: 'Sidebar'
}
</script>

<style lang="scss">
@import '../scss/main.scss';
.panel.background-side {
  position: fixed;
  height: 100vh;
  width: 100px;
  top: 0px;
  left: 0px;
  background-color: #FEE140;
  background-image: linear-gradient(150deg, #FEE140 0%, #FA709A 100%);
}
.margin {
  margin-top: 100px;
}
</style>
