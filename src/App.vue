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
        // Data binding
        // Cambiar datos usando la reactividad
        // v-bind ayuda a enlazar un atributo con una propiedad
        // v-bind puede ser solo : como shortcut
        input(v-model="person.name")
        h1 Hello my name is {{ person.name }}
        a(v-bind:href="url") floups.com
        br
        //Computed properties
        input(v-model="person.lastName")
        h1 {{fullName}} y tengo {{ age }} años de edad
        br
        p Fecha de nacimiento
        input(v-model="person.fechaNaciemiento" type="date")
        // Watchers
        // Ejecuta código a partir que una propiedad cambia
        // Van en el objeto watch
        br
        p {{ value }}
        input(v-model="value")
        // Eventos
        // Es un objeto (methods) que nos ayuda a
        // tener funciones para nuestra app
        br
        button(v-on:click="format") Format
        p {{ formatedName }}
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
        lastName: 'Zepeda',
        edad: '24',
        fechaNaciemiento: '1996-03-23'
      },
      url: 'https://floups.com',
      showValue: true,
      value: 'El valor',
      html: '<ul><li>Hola</li></ul>',
      items: [1, 2, 3, 4, 5, 6, 7, 8, 9],
      formatedName: ''
    }
  },
  computed: {
    fullName () {
      return `Mi nombre es ${this.person.name} ${this.person.lastName}`
    },
    age () {
      const fecha = new Date()
      const year = fecha.getFullYear()
      const nacimiento = this.person.fechaNaciemiento.substr(0, 4)
      return year - nacimiento
    }
  },
  watch: {
    value (newVal, oldVal) {
      console.log(newVal, oldVal)
    }
  },
  methods: {
    format () {
      this.formatedName = this.value.split(' ').join('-')
    }
  }
}
</script>
<style media="screen">
.margin-side{
  margin-left: 100px;
}
</style>
