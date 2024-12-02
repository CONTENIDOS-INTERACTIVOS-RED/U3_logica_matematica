<template lang="pug">
.curso-main-container.pb-3
  BannerInterno.text-uppercase(:titulo="'unidad 3: Lógica de predicados y aplicaciones en diferentes disciplinas'" :subTitulo="'3. Resolución de problemas mediante sistemas formales'")
  .container.tarjeta.tarjeta--blanca.px-4.pt-4.px-md-5.pt-md-5.pb-0

    .row.mb-5.mx-0
      .d-none.d-xl-block.col-4.px-0(data-aos="fade-right")
        img.h-100(src='@/assets/curso/unidad/img-26.png', alt='Texto que describa la imagen')
      .col-12.col-xl-8.d-flex.align-items-center.bg-azul-claro.p-4(data-aos="fade-left")
        p.mb-0(data-aos="fade-up") La resolución de problemas mediante sistemas formales es una metodología poderosa que permite abordar y resolver problemas complejos en diversas áreas del conocimiento, desde las matemáticas y la informática hasta la lingüística y la filosofía. Los sistemas formales consisten en conjuntos de reglas y estructuras que permiten realizar deducciones lógicas y derivar conclusiones a partir de axiomas o hechos iniciales. Este capítulo explora el concepto de sistema formal, su estructura y la forma en que se emplean para resolver problemas de manera efectiva en contextos variados.

    h2 ¿Qué es un sistema formal?
    p.mb-4 Un sistema formal es un conjunto de símbolos, axiomas, reglas de inferencia y, en algunos casos, una semántica definida, que permite la generación de expresiones lógicas y deducciones válidas. Estos sistemas son fundamentales para formalizar el razonamiento, ya que permiten expresar conocimientos y reglas de manera precisa y manipulable.

    .row.mb-5
      .col-12.col-lg-5.d-none.d-lg-block(data-aos="fade-right")
        img(src='@/assets/curso/unidad/img-27.png', alt='Texto que describa la imagen')
      .col-12.col-lg-7(data-aos="fade-left")
        p.mb-4 Un sistema formal típico está compuesto por:
        AcordionA(tipo="b")
          .div(titulo="Un conjunto de símbolos")
            p Son los elementos básicos (letras, números, operadores) que se combinan para formar expresiones o enunciados.
          .div(titulo="Axiomas")
            p Enunciados básicos que se consideran verdaderos dentro del sistema y sirven como puntos de partida para deducciones.
          .div(titulo="Reglas de inferencia")
            p Conjunto de reglas que permiten transformar o derivar nuevas expresiones a partir de las existentes.
          .div(titulo="Teoremas")
            p Enunciados que se pueden derivar a partir de los axiomas utilizando las reglas de inferencia.

    p.mb-4 Enunciados que se pueden derivar a partir de los axiomas utilizando las reglas de inferencia.

    .row.bg-rosa-1.bg-full-width.py-4
      div.px-5.pb-md-3.py-4.d-flex
        .col-12.col-xl-7.d-flex.pe-4.pe-xl-5.align-items-center.flex-column(data-aos="fade-right")
          h2.mb-4.pb-2.me-auto ¿Sabía que la ética es esencial en el desarrollo tecnológico?
          p.mb-5 En el documento Casos prácticos de ética en ingeniería, descubrirá cómo la ética influye en proyectos como el uso de inteligencia artificial en salud y la selección de personal mediante algoritmos. Estos ejemplos ilustran la importancia de principios como la transparencia y la equidad. Además, el documento destaca competencias y herramientas clave para que los ingenieros puedan actuar éticamente en un mundo tecnológico en constante cambio.
          a.d-flex.me-auto.bg-white.box-shadow.cursor-pointer(data-aos="zoom-in" :href="obtenerLink('/downloads/.pdf')" target="_blank")
            img.h-100(style="width: 48px" src='@/assets/componentes/pdf-icon-square.svg', alt='Texto que describa la imagen')
            p.text-small.fs-14px.my-auto.px-2 <strong>Anexo.</strong> Casos prácticos de ética en ingeniería
             
        .d-none.d-xl-block.col-xl-5.mx-auto.mt-4.mt-xl-0(data-aos="fade-left")
          img.h-100(src='@/assets/curso/unidad/img-28.png', alt='Texto que describa la imagen')

</template>

<script>
import BannerInterno from '../../components/plantilla/BannerInterno'
export default {
  name: 'Tema3',
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
