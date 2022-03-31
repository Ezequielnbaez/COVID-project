# COVID-project
1.Introducción

En el siguiente informe se desarrollarán las prácticas de distintas estrategias frente al COVID-19 y sus resultados en la población de distintos países con el fin de determinar una política pública eficiente frente a la propagación del virus. Se tomarán en cuenta las características generales de la pandemia y se realizará un algoritmo que permita entender el efecto de las estrategias analizadas. Para alcanzar lo propuesto se recurrirá a un dataset proporcionado por OurWorldInData, actualizado diariamente por la Universidad Johns Hopkins.
El dataset contiene información sobre el COVID-19 en distintos países, algunos aspectos que se tomarán en cuenta son: Cantidad total de casos, nuevos casos, cantidad total de muertes, tasa de reproducción, Índice de rigurosidad de respuesta del gobierno, población y gdp per cápita.

Además se tomará información adicional sobre qué países aplicaron la política pública en cuestión en un determinado tiempo para poder realizar una comparación. Las estrategias a analizar serán el uso obligatorio de máscaras y el grado de cuarentena aplicado.
Para éste análisis se eligieron ocho países, entre ellos Finlandia, España, Canadá, Suecia, Francia, Noruega, Reino Unido y Estados Unidos que se encuentran entre los mejores posicionados frente al COVID-19 hoy en día, algunos de ellos aplicaron cuarentena más estricta que otros y uso de máscaras obligatorio en el período a analizar y aun así todos se encuentran con una buena respuesta.

Fuente: Bloomberg https://www.bloomberg.com/graphics/covid-resilience-ranking




2.Comienzo de pandemia

El COVID-19 no se destacó tanto por su mortalidad sino por su capacidad de propagación ya que frente a otros virus como ébola y H5N1 queda atrás:




Fuente: https://www.statista.com/statistics/1095129/worldwide-fatality-rate-of-major-virus-outbreaks-in-the-last-50-years/





Por otro lado, lo que sí provocó que el COVID-19 sea un problema fue la tasa de infección que tenía, en este aspecto se encuentra sobrepasando a los demás y en conjunto a la evolución del transporte, ambos factores produjeron que se esparciera mundialmente de forma rápida.




Fuente: https://www.statista.com/statistics/1103196/worldwide-infection-rate-of-major-virus-outbreaks/



Comenzando la pandemia, los contagios siguen una ley exponencial, luego hay una caída por inmunidad. Ésto se va a analizar con el k de cada país elegido, siendo el k la contagiosidad propia de la enfermedad, mayor éste número, mayor serán los casos confirmados en cada población.El k toma en cuenta el tiempo que contagia una persona a otra, nivel de infección del virus y cuántas personas se contagian por ver a una persona enferma por día.



K inicial

Como primer análisis se tomará en cuenta a Francia ya que fue uno de los primeros países en encontrarse con el COVID-19 además de Estados Unidos y China, pero éstos al ser países excepcionales por su tamaño, un análisis de un país más pequeño podría resultar más preciso.

Imagen en función del logaritmo de la cantidad de casos en un transcurso de ochenta días como período inicial de la pandemia.

Teniendo esto en cuenta, una vez elegido el tramo más estable de contagios, en este caso entre los 35 a los 65 días desde el primer contacto, se puede establecer la función del k.

Imagen en función del k calculado, siendo la línea punteada los datos reales y la naranja los simulados por el k.



K mundial

A partir de una cantidad de países se pudo determinar un promedio, pero éste no es preciso, se puede deber a distintos motivos.




1.Fecha del primer caso: 
 
Imagen de tasa de reproducción en el transcurso de un año entre países con estaciones alternadas.

Esto puede deberse a varios motivos, se puede tomar en consideración la baja humedad, vitamina D por el sol, baja temperatura, sobre esto pueden haber varias teorías, pero definitivamente es uno de los factores que se tienen que tener en cuenta al analizar cómo se propaga el virus.


2.Riqueza de población:

Imagen de gdp per cápita en función del país.

El factor de la riqueza se debe considerar por el hecho de que un país más rico puede tener una respuesta distinta debido a que pueden tener más recursos en el ámbito hospitalario o de higiene aunque a su vez también tienen su transporte más desarrollado, lo cual es el principal motivo de propagación: el uso de vuelos internacionales. Aquellos países más desarrollados tienen un uso más común de este medio de transporte.

3.Población:

Imagen de población en cientos de millones por país

Una mayor población puede llevar a un mayor grado de contagio, no sólo por la cantidad de personas, sino también por la dificultad de un control riguroso de medidas ya que tienen que ser a gran escala y por más recursos que se tenga, algunas políticas como el uso obligatorio de barbijo en un país grande como Estados Unidos, podría ser difícil de implementar ya que se necesitaría control en un terreno demasiado amplio y sólo se podría implementar en los lugares más concurridos.



3.Evaluando estrategias

Para este proyecto se eligieron a Estados Unidos, Reino Unido, Canadá y Francia como ejemplos de países que aplicaron barbijo obligatorio en el transcurso de Abril y Mayo de 2020, mientras que Suecia, Finlandia, Noruega y España no. Ambos grupos tuvieron buen desempeño por igual, esto puede deberse a los factores aclarados previamente y los culturales.
El clasificador realizado aprendió en conjunto a otra política que es la severidad de la cuarentena, ya que es otro factor importante que todos los países aplicaron simultáneamente. Teniendo en cuenta esto, el modelo nos permite saber qué es lo que más va a afectar el uso o no de barbijo obligatorio, en este caso las muertes por millón nos ayudan mejor a predecir si serviría o no ésta política. Aunque todos estos indicadores o el mismo clasificador, no serían válidos analizando si aplicaron o no esta política, si fuera el caso de un clasificador que tomaría en cuenta sólamente la severidad de las restricciones, podría predecir mejor el aumento o disminución de la propagación del virus.
