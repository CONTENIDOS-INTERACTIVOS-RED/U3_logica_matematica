<template lang="pug">
.curso-main-container.pb-3
  BannerInterno.text-uppercase(:titulo="'unidad 3: Lógica de predicados y aplicaciones en diferentes disciplinas'" :subTitulo="'Lógica de predicados: variables, funciones y predicados'")
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.overflow-hidden

    p.mb-4 La lógica de predicados, también conocida como lógica de primer orden, es una extensión de la lógica proposicional que permite representar afirmaciones más complejas mediante el uso de variables, predicados y funciones. Mientras que la lógica proposicional se limita a trabajar con proposiciones que son o verdaderas o falsas, la lógica de predicados permite hacer afirmaciones sobre elementos específicos y generalizar mediante variables.
    .row.mb-4
      .coil-12.col-xl-7(data-aos="fade-right")
        p.mb-4 Esta herramienta es fundamental en matemáticas, filosofía, informática y áreas de ingeniería para estructurar el razonamiento formal. A través de la lógica de predicados, podemos representar y razonar sobre propiedades de objetos, relaciones entre ellos y cuantificadores como "para todo" y "existe".
        span En esta unidad se entrará en el mundo de la lógica de predicados y conocerás su propio lenguaje, donde se verán las fórmulas. A través de este lenguaje se podrán formalizar razonamientos donde el lenguaje de enunciados no era suficiente. A continuación, lo que se verá no es nada distinto o desconocido se tiene que validar razonamientos, buscar contraejemplos, revisar las formas normales, aplicar la deducción natural y la resolución.
      .col-5.d-none.d-xl-block(data-aos="fade-left")
        img(src='@/assets/curso/unidad/img-2.png', alt='Texto que describa la imagen')

    h2.mb-4 Capacidad expresiva del lenguaje de enunciados es limitada
    .row.mb-0.mx-0
      .d-none.d-xl-block.col-4.px-0(data-aos="fade-right")
        img.h-100(src='@/assets/curso/unidad/img-3.png', alt='Texto que describa la imagen')
      .col-12.col-xl-8.d-flex.align-items-center.bg-rosa-claro.p-4(data-aos="fade-left")
        p.mb-0(data-aos="fade-up") La capacidad expresiva del lenguaje de enunciados es bastante limitada: no cualquier frase declarativa simple se puede formalizar convenientemente. Este hecho tiene como consecuencia que un gran número de razonamientos que se pueden expresar utilizando el lenguaje natural no se puedan validar utilizando las herramientas de la lógica de enunciados.

    .bg-amarillo.p-4.mb-5.pt-5
      .row
        .col-11.mx-auto
          p.text-bold Ejemplo de las limitaciones de la lógica de enunciados 
          p.mb-4 
          p.mb-4 
          .row.mb-4
            .col-12.col-xl-8(data-aos="fade-right")
              .bg-amarillo-oscuro.p-4
                div.d-flex
                  img.mt-2.me-2.d-flex.align-self-baseline(style="width: 20px" src='@/assets/curso/arrow.png', alt='Texto que describa la imagen')
                  p.mb-0 La formalización (correcta) sería la siguiente: si asignamos P a “los estudiantes son personas”, Q a “Juan es un estudiante” y R a “Juan es una persona”, entonces tenemos que: 
              .bg-white.px-4.py-3.text-center.mb-4
                span P, Q, R
              
              p.mb-4 No permite validar el razonamiento. 

              .bg-amarillo-oscuro.p-4
                div.d-flex
                  img.mt-2.me-2.d-flex.align-self-baseline(style="width: 20px" src='@/assets/curso/arrow.png', alt='Texto que describa la imagen')
                  p.mb-0 Otra formalización (que también se puede considerar correcta) es: si asignamos P a “ser estudiante”, Q a “ser persona”, R a “Juan es un estudiante” y S a “Juan es una persona”, entonces observamos que:  
              .bg-white.px-4.py-3.text-center.mb-4
                span P  → Q, R  S, 
              p.mb-4 Tampoco permite validar el razonamiento.
               
            .col-4.d-none.d-xl-block(data-aos="fade-left")
              img(src='@/assets/curso/unidad/img-4.png', alt='Texto que describa la imagen')

    #t_1_1.titulo-segundo
      div.d-flex
        span.me-3 1.1  
        h2 Predicados
    
    p.mb-4 Un predicado es una definición en un dominio que adquiere valores según un conjunto de enunciados. También se puede decir que son expresiones que afirman algo sobre una o más variables. Un predicado es una función booleana que toma un conjunto de variables y devuelve verdadero o falso dependiendo del valor de dichas variables.

    .row.mb-4
      .col-5.d-none.d-xl-block(data-aos="fade-right")
        img(src='@/assets/curso/unidad/img-5.png', alt='Texto que describa la imagen')
      .coil-12.col-xl-7(data-aos="fade-left")
        p.mb-4 Un predicado puede representarse con una letra mayúscula del alfabeto, seguida de sus variables, preferiblemente letras a partir de la "x" y separadas por comas. Por ejemplo, un predicado podría ser P(x), lo cual representa la formalización de "x es un estudiante".
        .d-flex.align-items-start.bg-azul.p-4.mb-4(data-aos="fade-left")
          img.me-3(style="width: 90px" src='@/assets/curso/unidad/img-6.svg', alt='Texto que describa la imagen')
          .d-flex.flex-column
            p.pe-xl-3.mb-0(data-aos="fade-up") Lo anterior indica que el predicado P(x) no es un enunciado por sí mismo, pero puede convertirse en uno si sustituimos la variable "x" por algún elemento específico del dominio. Si el dominio es el conjunto de personas, entonces P(José) sí sería un enunciado y representaría "José es un estudiante".

    p.mb-4 Una regla general es que no se habla de parámetros, sino de variables. Un predicado puede tener 0 o n cantidad de variables, y se clasifica según esta cantidad de la siguiente manera:

    .bg-amarillo.p-4.mb-4.d-flex
      .col-12.col-xl-7(data-aos="fade-right")
        .row
          .col-12
            ol.lista-ol--cuadro
              li.d-flex 
                .lista-ol--cuadro__vineta
                  span 1
                p.mb-0 Predicados con n = 0 variables son enunciados
              li.d-flex
                .lista-ol--cuadro__vineta
                  span 2
                p.mb-0 Predicados con n = 1 variable son propiedades o predicados unarios
              li.d-flex
                .lista-ol--cuadro__vineta
                  span 3
                p.mb-0 Predicados con n = 2 variables son relaciones o predicados binarios
              li.d-flex
                .lista-ol--cuadro__vineta
                  span 4
                p.mb-0 A partir de n = 3 variables son relaciones ternarias, cuaternarias, etc.
      .col-4.mx-auto.d-none.d-xl-block(data-aos="fade-left")
        img(src='@/assets/curso/unidad/img-7.png', alt='Texto que describa la imagen')

    .row.mb-4
      .col-5.d-none.d-xl-block(data-aos="fade-right")
        img(src='@/assets/curso/unidad/img-8.png', alt='Texto que describa la imagen')
      .coil-12.col-xl-7(data-aos="fade-left")
        p.mb-4 
        AcordionA(tipo="b")
          .div(titulo="Ejemplos de propiedades o predicados unarios")
            p P(x): “x es una persona”. <br> Q(x): “x es de color rojo”.
          .div(titulo="Ejemplos de relaciones o predicados binarios")
            p P(x,y): “x come y”. <br> Q(x,y): “El cuadrado de x es y”.
          .div(titulo="Ejemplos de relaciones ternarias")
            p  R(x,y,z): “x saluda a y en la calle z”. <br> S(x,y,z): “La suma de x y de y es z”.

    .row.mb-4
      .col-12.col-xl-7(data-aos="fade-right")
        p.mb-4 Un punto importante a recordar es que el dominio de una variable incluye todos los objetos que pueden sustituirla.
        p.mb-4 A continuación, algunos ejemplos de predicados:
        .bg-azul.p-4.mb-0
          p.text-bold.mb-4 Ejemplo: 
          p.mb-2 P(x): "x es mayor que 5".
          .ms-4
            p.mb-2 • Si x=7, P(7)) es verdadero.
            p.mb-2 • Si x=3, P(3) es falso.
      .col-5.d-none.d-xl-block(data-aos="fade-left")
        img.h-100(src='@/assets/curso/unidad/img-9.png', alt='Texto que describa la imagen')
    .row.mb-4
      .col-5.d-none.d-xl-block(data-aos="fade-right")
        img.h-100(src='@/assets/curso/unidad/img-10.png', alt='Texto que describa la imagen')
      .col-12.col-xl-7(data-aos="fade-left")
        p.mb-4 Los predicados pueden depender de varias variables. Por ejemplo, Q(x,y)Q(x, y)Q(x,y) puede representar "x es mayor que y". Aquí, el predicado relaciona dos variables.
        .bg-azul.p-4.mb-0
          p.text-bold.mb-4 Ejemplo: 
          p.mb-2 Q(x,y): x > y
          .ms-4
            p.mb-2 • Si x=7 y y=5, entonces Q(7,5) es verdadero.
            p.mb-2 • Si x=4 y y=6, Q(4,6) es falso.
        .bg-amarillo.p-4.mb-0
          p.text-bold.mb-4 Ejercicio:
          p.mb-0 Define un predicado R(a,b) que representa "a es divisible por b". Luego, determina si R(10,2) es verdadero o falso.

    h2 Funciones en la lógica de predicados
    .row.mb-4
      .col-12.col-xl-8(data-aos="fade-right")
        p.mb-4 En términos formales, una función en la lógica de predicados es una expresión que, dada una o más entradas, produce un resultado único. De este modo, una función de argumentos se interpreta como una asignación única de valores de salida para cada combinación posible de n entradas. Esto se diferencia de un predicado, que devuelve un valor de verdad (verdadero o falso). En cambio, las funciones devuelven un valor o un objeto específico.
        span Por ejemplo, consideremos la función PadreDe(x). En este caso, PadreDe(x) produce el padre de x como resultado. Así, si afirmamos que PadreDe(Juan) = Carlos, estamos indicando que Carlos es el padre de Juan. En contraste, un predicado podría ser EsPadre(x,y), el cual verifica si x es o no el padre de y en un contexto determinado.
      .col-4.mx-auto.d-none.d-xl-block(data-aos="fade-left")
        img(src='@/assets/curso/unidad/img-11.png', alt='Texto que describa la imagen')

    h2 Notación y uso de funciones
    p.mb-4 La notación en lógica de predicados permite distinguir entre predicados y funciones de una manera concisa y clara:
    .row.mb-4
      .col-4.d-none.d-xl-block(data-aos="fade-right")
        img(src='@/assets/curso/unidad/img-12.png', alt='Texto que describa la imagen')
      .col-12.col-xl-8(data-aos="fade-left")
        .bg-azul.p-4.mb-0
          div.d-flex
            img.mt-2.me-2.d-flex.align-self-baseline(style="width: 20px" src='@/assets/curso/arrow.png', alt='Texto que describa la imagen')
            p.mb-0 Un predicado se representa típicamente como P(x) o Q(x,y), donde el resultado es un valor de verdad.
        .bg-amarillo.p-4.mb-4
          div.d-flex
            img.mt-2.me-2.d-flex.align-self-baseline(style="width: 20px" src='@/assets/curso/arrow.png', alt='Texto que describa la imagen')
            p.mb-0 Una función, por otro lado, se representa como f(x), donde el resultado es un valor en un dominio particular.
        p.mb-0 Por ejemplo, si estamos trabajando con una función Multiplicación(x, y), podríamos escribir Multiplicación(2, 3) para representar la multiplicación de 2 y 3, cuyo resultado es 6.

    p.mb-4 Ejemplos prácticos de funciones en lógica de predicados: 
    .row.mb-5
      .col-12.col-lg-7(data-aos="fade-right")
        AcordionA(tipo="b")
          .div(titulo="Funciones matemáticas")
            p.mb-4 En contextos donde se representa conocimiento matemático, las funciones son fundamentales. Ejemplo:
            p.mb-2 • Suma(x, y) podría representar la operación de sumar dos números.
            p.mb-2 • Si afirmamos que Suma(2, 3) = 5, estamos diciendo que la función de suma aplicada a 2 y 3 da como resultado 5.
          .div(titulo="Relaciones familiares")
            p Las funciones son útiles para representar relaciones familiares, donde cada persona tiene solo un padre o una madre.
            p <strong>PadreDe(x)</strong> devuelve al padre de una persona. Si afirmamos que <strong>PadreDe(Juan) = Carlos</strong>, estamos utilizando una función para definir una relación específica y unívoca.
          .div(titulo="Ubicación y dirección")
            p En contextos espaciales o geográficos, las funciones pueden asignar ubicaciones exactas.
            p <strong>CiudadDe(x)</strong> podría devolver la ciudad de origen de una persona. Así, <strong>CiudadDe(Ana) = Madrid</strong> establece que Ana es de Madrid.
      .col-12.col-lg-5.d-none.d-lg-block(data-aos="fade-left")
        img(src='@/assets/curso/unidad/img-13.png', alt='Texto que describa la imagen')

    h2 Diferencia entre funciones y predicados
    p.mb-4 Es importante resaltar la diferencia entre funciones y predicados:

    .row.mb-5.justify-content-center(data-aos="zoom-in-up")
      .col-10.col-sm-9.col-md-6.mb-4(data-aos="fade-up-right")
        .custom-image-card.d-flex.p-3.h-100
          img.mb-3(src='@/assets/curso/unidad/img-14.svg', style="width: 68px")
          .d-flex.flex-column.ms-3
            p.text-bold.mb-2 Predicado
            p.mb-0.text-small Un predicado responde a preguntas de verdadero o falso. Por ejemplo, si tenemos MayorQue(x, y), podemos preguntarnos si un número es mayor que otro, obteniendo respuestas de verdadero o falso. 
      .col-10.col-sm-9.col-md-6.mb-4(data-aos="fade-up-right")
        .custom-image-card.d-flex.p-3.h-100
          img.mb-3(src='@/assets/curso/unidad/img-29.svg', style="width: 68px")
          .d-flex.flex-column
            p.text-bold.mb-2 Función
            p.mb-0.text-small Una función proporciona un valor o una entidad en particular. En el caso de Mayor(x, y), donde buscamos el mayor entre dos números, la función podría devolver uno de los dos números.
    
    #t_1_2.titulo-segundo
      div.d-flex
        span.me-3 1.2  
        h2 Cuantificadores en la Lógica de Predicados
    p.mb-4 Cuando se habla de cuantificadores en la lógica de predicados se hace referencia a los operadores que se añaden a las conexiones. Dichos operadores se relacionan y se corresponden, sería algo como todos y todas, unos y unas, etc.
    .row.mb-4
      .col-12.col-xl-10.mx-auto(data-aos="fade-up")
        p.mb-4 <strong>Tabla 1.</strong> Cuantificadores

        .tabla-a.mb-5
          table
            thead
              tr
                th.text-start.border-gris-right(width="15%") Símbolo
                th.text-start.border-gris-right(width="25%") Nombre
                th.text-start.border-gris-right(width="15%") Significado
                th.text-start.border-gris-right Correspondencia (aproximadamente)
            tbody
              tr
                td ∀
                td Cuantificador universal
                td '(para) todo'
                td todos los…, todas las…, cada…
              tr
                td ∃
                td Cuantificador existencial
                td 'existe (alguno)'
                td hay un…, existe un…, algún o algunos…
        p.mb-4 Cómo se puede observar en la tabla  hay dos tipos principales de cuantificadores:
        .row.mb-4
          .col-12.col-lg-6.bg-rosa.p-4(data-aos="fade-right")
            p.text-bold.mb-3 Cuantificador Universal ( ∀ )
            p.mb-4 Expresa que una proposición es verdadera para todos los elementos de un dominio.
            p.mb-1.text-bold Ejemplo:
            p.mb-0 ∀x (x+0=x) significa "para todo x, x+0=x", que es una verdad en el dominio de los números enteros.
          .col-12.col-lg-6.bg-azul.p-4(data-aos="fade-left")
            p.text-bold.mb-3 Cuantificador Existencial ( ∃ )
            p.mb-4 Expresa que existe al menos un elemento en el dominio para el cual la proposición es verdadera.
            p.mb-1.text-bold Ejemplo:
            p.mb-0 ∃x (x^2=4) significa "existe un x tal que x^2 = 4", lo cual es verdadero para x=2 y x=−2.

        .row.mb-4
          .d-flex.align-items-center.px-0
            div.d-flex.align-items-center.bg-amarillo.px-3.pt-4
              img.me-4(style="width: 140px" src='@/assets/curso/unidad/img-30.png', alt='Texto que describa la imagen')
              .d-flex.flex-column
                p.pe-xl-5.mb-0.text-bold Ejercicios
                ol.lista-ol--cuadro
                  li.d-flex 
                    .lista-ol--cuadro__vineta
                      span 1
                    p.mb-0 Escribe una proposición utilizando el cuantificador universal que exprese "todo número par es divisible por 2".
                  li.d-flex
                    .lista-ol--cuadro__vineta
                      span 2
                    p.mb-0 Escribe una proposición utilizando el cuantificador existencial que exprese "existe un número que es mayor que 10".

    #t_1_4.titulo-segundo
      div.d-flex
        span.me-3 1.4  
        h2 Aplicaciones de la Lógica de Predicados

    p.mb-4 La lógica de predicados tiene aplicaciones prácticas en una variedad de áreas:

    .row.mb-5.justify-content-center 
      .col-10.col-md-8.col-lg-6.col-xl-4.mb-4.mb-xl-0
        .custom-image-card.d-flex.flex-column.p-4.py-md-5.h-100
          img.mx-auto.mb-4(src='@/assets/curso/unidad/img-31.svg', style="width: 80px")
          p.text-bold.mb-4.text-center Informática
          p.px-1.text-small.mb-0.d-flex Es crucial para la creación de algoritmos, lenguajes de programación y sistemas de inteligencia artificial. Por ejemplo, en bases de datos relacionales, las consultas SQL pueden verse como predicados que seleccionan registros que cumplen ciertas condiciones. 
      .col-10.col-md-8.col-lg-6.col-xl-4.mb-4.mb-xl-0
        .custom-image-card.d-flex.flex-column.p-4.py-md-5.h-100
          img.mx-auto.mb-4(src='@/assets/curso/unidad/img-32.svg', style="width: 80px")
          p.text-bold.mb-4.text-center Ingeniería
          p.px-1.text-small.mb-0.d-flex Los sistemas de control automático usan predicados para verificar que los valores de los sensores cumplan con ciertas condiciones antes de ejecutar una acción.
      .col-10.col-md-8.col-lg-6.col-xl-4.mb-4.mb-xl-0
        .custom-image-card.d-flex.flex-column.p-4.py-md-5.h-100
          img.mx-auto.mb-4(src='@/assets/curso/unidad/img-33.svg', style="width: 80px")
          p.text-bold.mb-4.text-center Ciencias sociales
          p.px-1.text-small.mb-0.d-flex En la teoría de juegos, se utiliza la lógica de predicados para modelar decisiones estratégicas donde los agentes toman acciones basadas en reglas lógicas.

</template>

<script>
export default {
  name: 'Tema1',
  data: () => ({}),

  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
}
</script>

<style lang="sass"></style>
