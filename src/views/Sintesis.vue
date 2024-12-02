<template lang="pug">
.curso-main-container.creditos-vista
  BannerInterno(:titulo="'unidad 3: Lógica de predicados y aplicaciones en diferentes disciplinas'" :subTitulo="'SÍNTESIS'")
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5
    p.mb-4.mb-md-5 Esta unidad aborda tres pilares de la lógica matemática aplicados a problemas complejos: la lógica de predicados, las aplicaciones de la lógica en informática, ingeniería y ciencias sociales, y la resolución de problemas mediante sistemas formales. Aprenderemos a usar variables, predicados y funciones para representar y analizar propiedades de elementos y relaciones entre ellos. Además, exploraremos cómo la lógica matemática respalda decisiones en tecnología y ciencias sociales, y cómo los sistemas formales, con axiomas y reglas de inferencia, garantizan soluciones precisas en el desarrollo de algoritmos y programas.
    figure
      img(src='@/assets/componentes/sintesis.png', alt='Texto que describa la imagen')
    

</template>
<script>
import BannerInterno from '../components/plantilla/BannerInterno'
import Footer from '../components/plantilla/Footer'
export default {
  name: 'Creditos',
  components: {
    BannerInterno,
    Footer,
  },
  data: () => ({
    configTitulos: {
      liderEquipo: 'ECOSISTEMA DE RECURSOS EDUCATIVOS DIGITALES',
      contenidoInstruccional: 'CONTENIDO INSTRUCCIONAL',
      desarrolloProducto:
        'DISEÑO Y DESARROLLO DE RECURSOS EDUCATIVOS DIGITALES',
      gestoresRepositorio: 'GESTORES DE REPOSITORIO',
    },
  }),
  computed: {
    creditosData() {
      return this.$config.creditos
    },
    creditosAdicionales() {
      return this.$config.creditosAdicionales
    },
  },
  methods: {
    renderText(textObj) {
      let newText = ''
      if (Array.isArray(textObj)) {
        textObj.forEach((texto, index) => {
          newText += (index ? '<br/>' : '') + texto
        })
      } else {
        newText += textObj
      }
      return newText
    },
  },
}
</script>

<style lang="sass">
.creditos-vista
  .tarjeta.credito
    background-color: $color-sistema-d

.creditos
  color: $color-sistema-b
  overflow-x: auto

  &__item
    min-width: 490px

  p
    line-height: 1.3em
    margin-bottom: 0
    color: $color-sistema-b

  &__titulo
    font-weight: $base-bold-font-weight
    background-color: $color-sistema-d
    padding: 5px 10px
    border-top-radius: $base-border-radius
    border-top-left-radius: $base-border-radius
    border-top-right-radius: $base-border-radius
  table
    td, th
      border-color: $color-sistema-d
</style>
