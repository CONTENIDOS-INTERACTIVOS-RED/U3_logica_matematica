<template lang="pug">
.curso-main-container.introduccion
  BannerInterno.text-uppercase(:titulo="'unidad 3: Lógica de predicados y aplicaciones en diferentes disciplinas'" :subTitulo="'INTRODUCCIÓN'")
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5

    p.mb-4 La lógica de predicados extiende la lógica proposicional, incorporando variables, funciones y predicados para representar relaciones y propiedades con mayor precisión. A diferencia de la lógica proposicional, que se limita a proposiciones verdaderas o falsas, la lógica de predicados descompone las proposiciones en partes específicas, lo que facilita la expresión de propiedades sobre objetos y permite analizar su estructura interna. Este enfoque potencia la capacidad de representación lógica, especialmente útil en sistemas complejos.
    .row.mb-4
      .col-5.d-none.d-xl-block(data-aos="fade-right")
        img(src='@/assets/curso/unidad/img-1.png', alt='Texto que describa la imagen')
      .col-12.col-xl-7(data-aos="fade-left")
        .bg-azul.p-4.mb-4
          span En informática, la lógica matemática es clave en el diseño y verificación de software y hardware, brindando una base teórica para asegurar el correcto funcionamiento de los sistemas. En inteligencia artificial, permite representar conocimiento y razonamiento automático, lo cual es esencial para la toma de decisiones en sistemas de IA. En ingeniería, facilita el análisis de circuitos y sistemas de control, mientras que en ciencias sociales se aplica en la teoría de juegos y la toma de decisiones, estructurando problemas de manera rigurosa y racional.
        p La resolución de problemas mediante sistemas formales permite abordar complejidades mediante reglas lógicas bien definidas. Los sistemas formales utilizan axiomas, reglas de inferencia y proposiciones para derivar conclusiones con rigor, siendo fundamentales en el desarrollo de algoritmos y la verificación de programas informáticos. Estas herramientas estructuran el razonamiento y modelan el mundo, apoyando el avance en disciplinas como la informática, la ingeniería y las ciencias sociales.

    

</template>

<script>
import BannerInterno from '../components/plantilla/BannerInterno'
import Muestras from '../components/muestras/Muestras.vue'

export default {
  name: 'Introduccion',
  components: {
    BannerInterno,
    Muestras,
  },
  data: () => ({
    globalData: global,
  }),
}
</script>

<style lang="sass"></style>
