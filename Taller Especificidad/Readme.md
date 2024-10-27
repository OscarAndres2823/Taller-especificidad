TALLER DE ESPECIFICIDAD

Objetivo:
El objetivo del taller es que los participantes comprendan como funciona la especificidad en CSS y aprendan a utilizarla de manera efectiva para resolver conflictos de estilos

PARTE 1:
1. ¿Que es la especificidad?
La especificidad es un concepto fundamental en CSS que determina qué reglas se aplican cuando hay conflictos entre varios selectores que afectan al mismo elemento. En otras palabras, es el mecanismo que usa el navegador para decidir cuál de las reglas definidas tiene mayor prioridad sobre otras.
     * Introduccion: En CSS, los selectores son patrones que se usan para seleccionar elementos HTML específicos y aplicarles estilos. Los diferentes tipos de selectores tienen pesos de especificidad distintos, lo que afecta qué reglas se aplican cuando varias coinciden con el mismo elemento
     * Como Afectan: Cuando varios selectores afectan al mismo elemento, el navegador calcula la especificidad con base en el tipo de selectores usados
2. Reglas de cálculo de especificidad:
     * Selectores de ID: Se utiliza para aplicar estilos a un elemento único identificado por un atributo id. Los ID son únicos en un documento HTML, lo que significa que cada iddebe asignarse solo a un elemento específico, lo que da a este tipo de selector una alta especificidad
     * Selectores de clase, atributos y pseudoclases: Estos selectores permiten seleccionar elementos específicos según ciertas características, como una clase asignada, un atributo presente, o un estado particular del elemento. A continuación, veremos cada uno en detalle, cómo se usan y cómo afecta la especificidad:
     * Selectores de clase: Los selectores de clase se utilizan para seleccionar uno o varios elementos con un atributo classespecífico. A diferencia del ID, que debe ser único en el documento, una clase puede aplicarse a múltiples elementos.
     * Selectores de atributos: Los selectores de atributo seleccionan elementos en función de los atributos que contienen. Son muy útiles para estilizar formularios o elementos dinámicos
     * Pseudoclases: Las pseudoclases seleccionan elementos en función de su estado dinámico o su posición en el árbol del DOM. Algunas comunes incluyen :hover, :nth-child(), y :focus.
* Selectores de elementos y pseudoelementos: 
     * Selectores de elementos: Un selector de elemento selecciona todas las instancias de un tipo de etiqueta HTML, como div, p, h1, etc. Son selectores genéricos y con la menor especificidad en CSS.
     * Pseudoelementos: Los pseudoelementos permiten seleccionar y aplicar estilos a partes específicas de un elemento, como la primera línea de un párrafo o un contenido insertado antes o después de otro elemento. Se indican con dos puntos dobles ( ::) , aunque algunos navegadores aceptan una sola (ej.: :before).
* !important y cómo afecta la cascad: En CSS, las reglas siguen un sistema de cascada , en el cual se aplican los estilos según su especificidad y orden de aparición . Sin embargo, la palabra clave !importantse utiliza para sobrescribir cualquier regla , independientemente de su especificidad o lugar en la hoja de estilos. Es una herramienta poderosa que debe usarse con precaución para evitar conflictos y complicar el mantenimiento del CSS.
     * Como Afecta a la cascada:
         * Sobrescribe cualquier regla sin importar la especificidad: Una regla con !importanttiene más prioridad que cualquier otra regla, incluso si esta última tiene mayor especificidad o aparece después en la hoja de estilos. 
         * Orden de aparición no importa: Normalmente, si dos reglas tienen la misma especificidad, se aplica la que aparece última en el CSS. Pero si una de las reglas usa !important, esa tendrá prioridad.

PARTE 2:
1. Ejemplo básico:
Demuestra cómo los diferentes selectores afectan la especificidad.
(evidencia1.png)
Resultado esperado: El color del texto será rojo, ya que el selector de ID tiene mayor
especificidad que los selectores de clase y etiqueta
2. Demostración de !important:
(evidencia2.png)
Resultado esperado: El color será azul, porque !important tiene prioridad,
independientemente de la especificidad.

PARTE 3:

Ejercicios Practicos:
     * Ejercicio 1:
         * Calculando la Especificidad: Dado el siguiente código, pide a los participantes que calculen la especificidad y determinen qué estilos se aplicarán
         (ejercisio1.png)
         Pregunta:
         ¿Qué color tendrá el título <h1> ?
         Respuesta: 
         El título va a ser rojo, ya que el estilo de ID tiene mayor especificidad
     * Ejercicio 2: 
         Resolviendo Conflictos de Especificidad: Modifica el siguiente código para que el párrafo tenga color amarillo, sin usar !important .
         (ejercisio2.png)

PARTE 4: 

Desafío Final
     * Desafío: Diseñando una Página Completa con Estilos Conflictivos
     Dales a los participantes un archivo HTML con múltiples elementos y clases, y pídeles que agreguen estilos CSS para lograr un diseño específico. Deberán aplicar todo lo aprendido sobre especificidad para resolver los conflictos y obtener el resultado correcto.
         *Desafío CSS:
             * El <h1> en el .header debe ser de color blanco.
                *Nota: En el primer desafio(El <h1> en el .header debe ser de color blanco) para que se pueda ver el resultado pedido por el taller, utilise el background-color para poder agregarle un color de fondo para que se pueda ver el resultado.
             * El texto del <p> en .content debe ser rojo.
             * El texto del <footer> debe ser gris.
         *Resultado Esperado:
         (DesafyFinally.png) 

PARTE 5:

Revisión y Discusión
     * Revisar las soluciones de los participantes.
     * Discutir errores comunes y cómo evitarlos.
     * Aclarar dudas sobre cómo calcular la especificidad y cómo usarla correctamente.

CONCLUSIÓN
Al final del taller, los participantes deberán:
     * Entender cómo se calcula la especificidad.
     * Resolver conflictos de estilo aplicando la especificidad correcta.
     * Conocer cómo y cuándo usar !important y otras técnicas avanzadas
