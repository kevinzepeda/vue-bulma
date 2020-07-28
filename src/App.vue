<template lang="pug">
  #app
    Header
    Sidebar
    .section.margin-side
      .content
        // Expresiones
        // Propiedades
        // Ariemtnticas
        // Concatenaciones
        // Llamados de objetos
        .title.is-3.ml-5 {{title}} mi nombre es {{person.name}} y tengo {{person.edad}} años
        .p {{ true ? 'e velda': 'false'}}
        // Directivas
        // Son pequeños marcadores o atributos para nuestro html
        // V-show V-if v-else v-else-if v-for v-text v-html
        p(v-show="showValue") {{ value }}
        p(v-if="showValue") {{ value }}
        p(v-else="showValue") {{ value + value}}
        ul
          li(v-for="i in items") {{ i }}
        p(v-text="value")
        p(v-html="html")
        Tarjetas.mb-6
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
      title: 'Hola Mundo',
      person: {
        name: 'Kevin',
        edad: '24'
      },
      showValue: true,
      value: 'El valor',
      html: '<ul><li>Hola</li></ul>',
      items: [1, 2, 3, 4, 5, 6, 7, 8, 9]
    }
  }
}
</script>
<style media="screen">
.margin-side{
  margin-left: 100px;
}
</style>
