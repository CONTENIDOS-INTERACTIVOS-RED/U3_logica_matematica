<template lang="pug">
.curso-main-container.pb-3
  BannerInterno.text-uppercase(:titulo="'unidad 3: Lógica de predicados y aplicaciones en diferentes disciplinas'" :subTitulo="'2. Aplicaciones de la lógica matemática en la informática, la ingeniería y las ciencias sociales'")
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5

    .row.mb-5.mx-0
      .col-12.col-xl-8.d-flex.align-items-center.bg-azul-claro.p-4(data-aos="fade-right")
        p.mb-0(data-aos="fade-up") La lógica matemática se ha convertido en una herramienta fundamental en múltiples disciplinas debido a su capacidad para representar y analizar problemas de manera estructurada. En campos tan diversos como la informática, la ingeniería y las ciencias sociales, la lógica matemática aporta rigor y claridad, facilitando la toma de decisiones y la resolución de problemas complejos. Este capítulo explora cómo los principios de la lógica matemática se aplican en estas áreas, resaltando su valor para construir sistemas eficientes y desarrollar teorías explicativas.
      .d-none.d-xl-block.col-4.px-0(data-aos="fade-left")
        img.h-100(src='@/assets/curso/unidad/img-20.png', alt='Texto que describa la imagen')

    #t_2_1.titulo-segundo
      div.d-flex
        span.me-3 2.1  
        h2 Aplicaciones de la lógica matemática en la informática

    .row.mb-4
      .col-12.col-xl-7(data-aos="fade-right")
        p.mb-4 En informática, la lógica matemática es la base de muchos conceptos y sistemas fundamentales:
        TarjetaAudio.color-primario.bg-white.mb-3(
          texto="Lógica Matemática: la base invisible de la tecnología moderna"
          tiempo
          :audio="require('../../assets/componentes/audios/Podcast - Lógica matemática und III_mezcla.mp3')"
          @audio-hover="mostrarIndicadorTarjetaAudio = false"
        )

      .col-5.d-none.d-xl-block(data-aos="fade-left")
        img.h-100(src='@/assets/curso/unidad/img-21.png', alt='Texto que describa la imagen')

    #t_2_2.titulo-segundo
      div.d-flex
        span.me-3 2.2  
        h2 Aplicaciones en ingeniería

    p.mb-5 La lógica matemática también es un pilar fundamental en diversas ramas de la ingeniería, proporcionando un marco para el análisis de sistemas y el control de procesos:

    ImagenInfografica.color-secundario.mb-5
      template(v-slot:imagen)
        figure
          img(src='@/assets/curso/unidad/img-22.png', alt='Texto que describa la imagen')

      .tarjeta.bg-rosa-claro.p-4(x="56.4%" y="36%" numero="+")
        .h5.mb-2 Automatización y control de procesos
        p La lógica matemática se utiliza para diseñar sistemas de control automático en áreas como la robótica y la manufactura. Mediante lógica difusa y lógica temporal, es posible modelar sistemas dinámicos que deben responder de manera flexible a cambios en el entorno. Esto es esencial en aplicaciones que requieren control preciso, como los sistemas de navegación autónoma y la automatización de líneas de producción.
      .tarjeta.bg-rosa-claro.p-4(x="56.4%" y="52.5%" numero="+")
        .h5.mb-2 Ingeniería de software
        p En ingeniería de software, la lógica matemática se aplica para formalizar el comportamiento de sistemas complejos. Las especificaciones formales basadas en lógica permiten diseñar y verificar programas antes de su implementación, reduciendo así la probabilidad de errores. Modelos como los autómatas finitos y las gramáticas formales representan secuencias de operaciones, facilitando el análisis y optimización de algoritmos.
      .tarjeta.bg-rosa-claro.p-4(x="56.4%" y="67.6%" numero="+")
        .h5.mb-2 Teoría de redes y sistemas de comunicación
        p La lógica matemática es crucial en el análisis de redes de comunicación y sistemas de transmisión de datos. La teoría de grafos, basada en principios lógicos, se emplea para modelar la estructura de redes de telecomunicaciones y redes de computadoras, facilitando el diseño de rutas eficientes y seguras para la transmisión de datos.

    #t_2_3.titulo-segundo
      div.d-flex
        span.me-3 2.3  
        h2 Aplicaciones en ciencias sociales

    p.mb-4 En el campo de las ciencias sociales, la lógica matemática ofrece un enfoque sistemático para analizar el comportamiento humano y la dinámica social:

    .row.position-relative.mb-5.py-4.bg-fondo-3.bg-full-width
      div.px-4.px-md-5.py-md-3
        SlyderA(tipo="b").bg-white
          .row.p-4.px-md-5.py-lg-5.justify-content-between
            .col-md-12.col-lg-7.mb-4.mb-md-0(data-aos="zoom-in-right")
              p.text-bold Modelado de decisiones racionales
              p En economía y psicología, la teoría de la decisión emplea lógica matemática para analizar y predecir el comportamiento de individuos y organizaciones. La lógica modal y la teoría de juegos son herramientas esenciales en este contexto, permitiendo modelar situaciones en las que los agentes toman decisiones bajo condiciones de incertidumbre o competencia.
            .d-none.d-lg-block.col-md-6.col-lg-4(data-aos="zoom-in-left")
              figure
                img(src='@/assets/curso/unidad/img-23.png', alt='Texto que describa la imagen')
          .row.p-4.px-md-5.py-lg-5.justify-content-between
            .col-md-12.col-lg-7.mb-4.mb-md-0
              p.text-bold Análisis de redes sociales
              p La lógica matemática, a través de la teoría de grafos, se utiliza para estudiar redes sociales y de influencia. Modelar interacciones sociales como redes permite analizar la propagación de información, la formación de opiniones y la estructura de comunidades en plataformas de medios sociales, facilitando la comprensión de fenómenos como la influencia de ciertos nodos y el alcance de la información en la red.
            .d-none.d-lg-block.col-md-6.col-lg-4
              figure
                img(src='@/assets/curso/unidad/img-24.png', alt='Texto que describa la imagen')
          .row.p-4.px-md-5.py-lg-5.justify-content-between
            .col-md-12.col-lg-7.mb-4.mb-md-0
              p.text-bold Investigación en ciencia política y sociología
              p La lógica matemática permite construir modelos que representan fenómenos sociales como el conflicto y la cooperación. Por ejemplo, la lógica difusa facilita el modelado de conceptos ambiguos, como la percepción de justicia o confianza, que no son directamente cuantificables, permitiendo un análisis más profundo y preciso de la dinámica social y política.
            .d-none.d-lg-block.col-md-6.col-lg-4
              figure
                img(src='@/assets/curso/unidad/img-25.png', alt='Texto que describa la imagen')

    .bg-full-width.border-top-9-azul
      .px-4.px-md-5.pt-5.pb-0
        h2 Material complementario
        .row
          .col-12.col-md-6.col-lg-8
            p.d-flex.my-4
              img.me-3.mb-auto.mt-1(src='@/assets/componentes/book.svg' :style="{'max-width':'16px'}")
              a.text-small.text-primary(target="_blank", href="https://elibro.net/es/ereader/tecnologicadeloriente/70065") Gutierrez, I. (2013). Matemáticas para informática. Universidad del Norte.
            p.d-flex.my-4
              img.me-3.mb-auto.mt-1(src='@/assets/componentes/book.svg' :style="{'max-width':'16px'}")
              a.text-small.text-primary(target="_blank", href="https://elibro.net/es/ereader/tecnologicadeloriente/35676") Kindelan U. (2007). Fundamentos matemáticos de la ingeniería. Dykinson.
          .col-12.col-md-6.col-lg-3
            figure
              img(src='@/assets/componentes/material-complementario.svg', alt='Imagen de material complementario')


</template>

<script>
import BannerInterno from '../../components/plantilla/BannerInterno'
export default {
  name: 'Tema2',
  components: {
    BannerInterno,
  },
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
}
</script>

<style lang="sass"></style>
