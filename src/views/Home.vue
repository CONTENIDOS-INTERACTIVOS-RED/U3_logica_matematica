<template lang="pug">
.curso-container.d-flex.flex-column.min-vh-100
  .container.d-flex.flex-column.justify-content-center.flex-grow-1.px-0.px-md-2
    div.home-content.d-flex.flex-column-reverse.flex-lg-column.p-4.p-lg-0
      .bg-white
        .row.g-0
          //- Columna izquierda con imagen
          .d-none.d-xl-block.d-xl-flex.mb-4.mb-md-0.col-md-4.col-xl-5.imagen-section
            img.img-fluid.h-full(
              src="@/assets/portada/banner.png"
              alt="Estudiante virtual"
              style="max-width: 672px;"
            )
          .d-block.d-lg-none.mx-auto.mb-4.mb-lg-0.col-md-8.col-lg-6.imagen-section
            img.img-fluid.h-full(
              src="@/assets/portada/banner-mobile.png"
              alt="Estudiante virtual"
              style="max-width: 672px;"
            )
          //- Columna derecha con información
          .col-xl-7.info-section
            .content-wrapper.px-lg-4.pt-lg-4.px-xxl-5.py-xxl-5.text-start
              p.home-main-title.text-uppercase UNIDAD 3
              h1.home-title.mb-4 Lógica de predicados y aplicaciones en diferentes disciplinas
              p.descripcion.mb-4 La lógica de predicados o lógica de primer orden amplía la lógica proposicional mediante el uso de variables, funciones y predicados, permitiendo representaciones detalladas y razonamientos complejos. Con variables y cuantificadores como para todo (∀) y existe (∃), es posible expresar relaciones y propiedades específicas de objetos. Sus aplicaciones incluyen diseño de algoritmos, verificación de software y modelado de decisiones. Además, permite formalizar razonamientos matemáticos, ingeniería y ciencias sociales, donde contribuye al análisis de sistemas, el diseño de redes y la investigación de fenómenos sociales.
            
              p.descripcion.mb-4.text-bold El poder del conocimiento está en transformar ideas en realidad; cada aprendizaje es un paso hacia la creación de un futuro mejor.

              .button-container.mt-auto
                router-link.btn-iniciar.w-100.w-md-auto(:to="{ name: 'introduccion' }")
                  div.iniciar-btn-container.w-100.w-md-auto
                    span.iniciar-btn-text INICIAR
                    div.icon
                      i.fas.fa-chevron-right

      //- Footer
      footer.footer.bg-white
        .container.px-4.py-3
          .row.justify-content-start.align-items-center
            .col-lg-auto
              img.logo-footer(
                src="@/assets/portada/logo-footer.png"
                alt="Logo Tecnológica del Oriente"
              )
            .col-lg.px-0.d-none.d-lg-block
              p.footer-text.mb-0 Todo el contenido de este curso es propiedad intelectual de Corporación Tecnológica del Oriente y está protegido por derechos de autor. No puede ser reproducido, distribuido, modificado ni compartido sin su autorización por escrito.
              
</template>

<script>
export default {
  name: 'Home',
}
</script>

<style lang="sass">
.curso-container
  .container
    @media (min-width: 1400px)
      max-width: 1378px
  .home-title
    font-size: 26px !important
    @media (min-width: 992px)
      font-size: 38px !important
  .home-main-title
    font-size: 18px
    font-weight: bold
    color: $color-institucional
  .home-content
    background-color: white
  .info-section
    position: relative
    min-height: 100%
    display: flex
    flex-direction: column
    @media (min-width: 1200px)
      border-bottom: 1px solid $color-sistema-f

  .content-wrapper
    display: flex
    flex-direction: column
    height: 100%

  .button-container
    margin-top: auto
    text-align: right

  .btn-iniciar
    display: flex
    align-items: center
    width: calc(100% - 48px)
    @media (min-width: 576px)
      margin-left: auto
      width: fit-content !important
    .iniciar-btn-container
      text-align: center
      display: flex
      .iniciar-btn-text
        background-color: $color-sistema-d
        padding: 12px 42px 12px 32px
        width: 100%
        color: #fff
    .icon
      background-color: $color-sistema-e
      padding: 0px 20px
      color: #fff
      display: flex
      align-items: center
    /* Aquí tus estilos existentes para el botón */

  .home
    padding: 20px
    text-align: center

  h1
    color: #2c3e50

  .logo
    height: 40px
    width: auto
    margin-bottom: 1.5rem
    object-fit: contain
    align-self: flex-start /* Asegura alineación izquierda incluso en contenedor flex */

  .logo-footer
    width: 250px
    object-fit: contain

  .footer
    margin-top: auto /* Empuja el footer al fondo */
    width: 100%
    .footer-text
      font-size: 14px
      border-left: solid 1px #707070
      padding-left: 20px

  .footer p
    font-size: 14px

.iniciar-btn-container
  .iniciar-btn-text
    transition: all 0.25s ease-in-out
    background-color: #F8C624 !important
    color: #0B0A0A !important
  .icon
    transition: all 0.25s ease-in-out
    background-color: #886C13 !important
    color: $white !important
  &:hover
    .icon
      transform: scale(1.06)
</style>
