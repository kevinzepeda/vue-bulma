<template lang="pug">
  #app
    Header
    Sidebar
    .section.margin-side
      .content
        .title.is-3.ml-5 {{title}}
        Tarjetas.mb-6
        .title.is-3.ml-5 {{title}}
        Tarjetas.mb-6
        .title.is-3.ml-5 {{title}}
        Tarjetas

</template>

<script>
import Registro from './components/Registro.vue'
import Header from './components/Header.vue'
import Sidebar from './components/Sidebar.vue'
import Tarjetas from './components/Tarjetas.vue'
export default {
  name: 'app',
  components: {
    Registro,
    Header,
    Sidebar,
    Tarjetas
  },
  data () {
    return {
      title: 'Hola'
    }
  }
}
</script>
<style media="screen">
.margin-side{
  margin-left: 100px;
}
</style>
