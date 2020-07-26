<template lang="pug">
  .section
    .container
      .column.is-6.is-offset-3
        .card
          .card-image.has-text-centered
            img( src="../assets/logo.jpg" )
          .card-content
            h1.title.has-text-weight-bold Registro estación Platzi
            form
              label Nombre
              input.input
              label Apellido
              input.input
              label Cargo
              input.input

</template>
<script>
export default {
  name: 'Registro'
}
</script>
<style lang="scss">
@import '../scss/main.scss';

</style>
