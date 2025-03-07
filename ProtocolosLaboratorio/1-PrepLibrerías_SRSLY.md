## Archivo escrito por Diana Carolina Thomas Rojas

PREPARACIÓN DE LIBRERÍAS NGS USANDO EL KIT SRSLY
Pasos generales:
Cuantificación de ADN en cada muestra y cálculos para correr la sonicación de ADN 
Fragmentación de ADN/Selección de objetivos 
Preparación de librerías usando SRSLY NGS KIT y purificación de ADN usando Beads
PCR e indexación de adaptadores (Incubación, Index y PCR)
Cuantificación final de ADN de la librería y control de calidad
Bioanalyzer

PRIMERA Y SEGUNDA PARTE:
PRIMERA PARTE 
Medición de la concentración de ADN y cálculos para correr la sonicación de ADN. 

Antes de comenzar:
Limpie el espacio a utilizar con EtOH 70% 
Aliste y/o uvee el material a utilizar por al menos 5 minutos (300 seg)


Guantes
Sharpies
Tubos PCR single connection (para sonicación)
Puntas 10 uL y 200 uL
Racks
QuBit tubos (para muestras y soluciones estándar)


Nota: Los tubos Qubit no se uvean porque cambian de color, y eso altera la lectura. 

Saque las muestras de ADN que desea utilizar y permita que estas se descongelen.
Saque de la nevera de 4°C el kit Qubit, el cual consta de 2 Standard Solution (SS1 and SS2) y 1 Working Solution (WS) (sensible a la luz) y permita que alcancen la temperatura ambiente antes de utilizarlos, ya que el WS frío puede causar problemas a la hora de llevar a cabo la lectura de la concentración.
Llene 2L de milli-Q H2O, si es posible mantener las botellas de agua en la nevera a 4°C, pero no es obligatorio (procedimiento a priori para el proceso de sonicación, para agilizar el proceso de enfriamiento en el sonicador).

Nota: Para tomar milli-Q H2O recordar que este a 18.2 mncm TC MQRest - debido al filtro. Si no, deje drenar un poco hasta que alcance este valor. También puede tomar agua destilada. 
 
Procedimiento:
Cuantificación de ADN en cada muestra

Aliste y marque de manera correspondiente el número de tubos Qubit por muestra y un par adicional para tubos con SS1 y SS2.
Agrege 199 uL de Qubit WS en cada uno de los tubos para las muestras.
Agrege 190 uL de WS en cada uno de los tubos para Standard Solution.
Haga spin de 5 seg a los tubos para homogeneizar. 

Nota: Recuerde mantener los tubos cubiertos con papel aluminio para evitar degradación o daño del reactivo por efecto de la luz mientras no los esté manipulando. 

Agrege 1 uL de la muestra de ADN correspondiente a cada tubo para las muestras e inmediatamente haga vórtex 5 seg a cada una de las muestras para homogeneizar. 
Agrege 10 uL de SS1 o SS2 en su correspondiente tubo y haga vórtex 5 seg
Spin 5 seg a todos los tubos
Cuantifique el ADN en el Qubit siguiendo las instrucciones en pantalla. 

Nota: Generalmente se usa muestra 1x dsDNA, coloca cada tubo en su interior y procede a hacer la correspondiente lectura. 

Tome nota de las concentraciones obtenidas (1 uL/ng es suficiente ADN para librerías). 

Nota: Si el Qbit dice que la muestra esta por encima del rango y dice que hay que diluirla. Llevar a cabo la dilución de tal manera que sea 9 uL de H2O miliQ por 1 uL de DNA, por ejemplo. Luego de esa dilución toma nuevamente 1 uL para la muestra que va a volver a medir en el Qbit, de tal manera que la concentración se encuentre dentro del rango adecuado para lectura.

Descarte los tubos Qubit una vez haya obtenido las lecturas. 

Lleve a cabo los cálculos para conocer los volúmenes de H2O y DNA necesario para la zonificación, de acuerdo con las concentraciones de ADN obtenidas. Ir al Google Sheet y correr las fórmulas. 

Google Sheet: https://docs.google.com/spreadsheets/d/1ZTH6LL4ubLh1Np5cHxSSZh0R0uqNqRRxn6KZXiYAJcA/edit#gid=12225278 

[ ] DNA obtenida por Qubit 
Target = Colocar el valor de acuerdo con la tabla de rangos presente en el google sheet y teniendo en cuenta la [ ] de ADN.


SEGUNDA PARTE
Sonicación de ADN

Procedimiento:
Conociendo los valores necesarios para hacer la sonicación de ADN se colocan esos volúmenes en los tubos de PCR. 
Agregar volumen de H2O
Agregar volumen de ADN
Hacer spin y vórtex suave de 5 seg para homogeneizar 
Separar los tubos para que queden individuales 

Nota: El sonicador trabaja con 18 muestras por lo que siempre debe completar este “número de muestras”. Si lo requiere, llenar tubos adicionales con H2O, estos tubos llenarlos con la mitad del volumen total de los tubos de las muestras, como punto de referencia.

En la QSonica ingresar 1L de milli-Q H2O, conectar el par de mangueras a la máquina según corresponda y configure el sistema para que disminuya la temperatura a 4°C.  
Una vez la temperatura disminuya proceda a agregar ½ L mili-Q H20 (dado que el nivel del agua seguramente descendió tras encender la máquina). 
Inicie el proceso de desgasificación del agua (DGas option) para eliminar el gas y que luego esto no interrumpa el proceso. Tiempo = ~10 min.

Nota: Si por alguna razón el montaje ya se encuentra realizado y usted desea usar el mismo, solo debe comenzar desde la desgasificación. 

En el sonicador organice las muestras en el rotador ubicado en el centro de la máquina. No es necesario que se encuentre balanceado, pero si que se encuentren bien colocadas las muestras para que a la hora de taparlos la tapa quede bien. 
Se coloca el rotador con las muestras en el sonicador sobre/dentro del agua que ha sido desgasificada. 

Nota: Recuerde revisar el nivel del agua respecto a las muestras de tal manera que esté igual o al menos un poco por debajo del nivel de las muestras. Si está por encima del nivel de las muestras es mejor drenar un poco el sistema para disminuir el nivel del agua lo suficiente. Si hace falta agua, agregue el agua suficiente, idealmente se espera que sea muy poca para evitar tener que desgasificar nuevamente. 

Comenzar el proceso con temperatura en 4°C
Configuración del sistema: tiempo =  7:00 min ; pulse = 30 / 30 ; Amplitud = 25°

Nota: Encontramos que para perritos llaneros el tiempo estandarizado con el cual habían hecho las librerías antes era de 12 minutos en total. Así que modificamos el ciclo a t = 6 min (recuerde que son 2 ciclos). El tiempo de sonicación depende de si ya se encuentra estandarizado para las muestras a procesar o no, si ya lo está genial, si no, se debe hacer un procedimiento de testeo con solo 5 min por ciclo para ir viendo como son los resultados obtenidos.  

Una vez el primer ciclo del sonicador termina se sacan las muestras, se revisan, se seca un poco el exceso de agua en el rotador y se le hace un spin corto a las muestras. Posteriormente, se colocan nuevamente en el rotador en diferente posición a la inicial, solo para evadir la posibilidad de que alguna de las muestras haya recibido más o menos energía al igual que nivel de temperatura. 

Las muestras se pasan en el sonicador por unos nuevos 7 minutos o el tiempo establecido de acuerdo con las muestras usadas.

Una vez terminado el proceso de sonicación. Retira las muestras del rotador, hace spin 5 seg y las almacena a 4°C para su próximo uso. 

Nota: Recuerde desconectar las mangueras y drenar el sistema tal como lo encontró.  





TERCERA PARTE
SRSLY NGS Library Preparation Kit and Beads Purification (PCR Desnaturalización e Incubación)

Antes de comenzar:
SRSLY Kit se encuentra en el REVCO -20°C: 
1 Single Standard “Tapa roja”
Adaptador A “Tapa Amarilla” y Adaptador B “Tapa Naranja”
Master Mix “Tapa verde”

Nota: El Single Standard y los Adaptadores se deben conservar fuera de la nevera en racks fríos hasta su uso, mientras que el MM luego de sacarlo de la nevera se mantiene a temperatura ambiente hasta su uso. 

Nota: Tenga en cuenta que es necesario que los Adaptadores y el SS se descongelen, por lo que los puede dejar descongelar unos minutos antes de utilizarlos. Luego, una vez descongelados los vuelve a colocar en el rack frío para mantenerlos a la temperatura correcta. Sin embargo, procure que no se vuelvan a congelar antes de usarlos para no tener que volver a pasar por el proceso de descongelarlos, etc, evitando dañar los reactivos. 

Limpiar el espacio a utilizar con EtOH 70% 
Marcar y uvear material a utilizar t = 300 seg = 5 min


Guantes
Sharpies
Tubos PCR triple connection (tupos pre-pre-PCR)
Puntas 10 uL y 200 uL
Racks



Encender 2 termocicladores. Deje los termo precalentando, uno en el protocolo SRSLY desnaturalización a T = 98°C y V = 10 uL y el otro en el protocolo SRSLY Incubación a T = 37°C V = 25uL. 

Nota: Si solo cuenta con un termociclador, debe contar con que luego del proceso de desnaturalización debe esperar al menos ~30 min a qué la temperatura disminuya y alcance los 37°C para seguir con el siguiente paso.

Nota: Modifique los protocolos al volumen correspondiente (si es necesario). Ej. 10 uL. o de acuerdo a la cantidad que se tenga, pero 10 uL es el estándar. Luego del beep el termociclador esta listo para usar.

Procedimiento:
Desnaturalización de la hebra de ADN

Haga “flick” a los tubos del sonicador y un spin corto antes de comenzar 
Marque los nuevos tubos PCR a utilizar (tubos pre-pre-PCR) 
Tome 9 uL de ADN sonicado y agreguelos en cada uno de los tubos pre-pre-PCR correspondientes. 

Nota: Haga un negativo al cual se le incluyen solo 9 uL de mili-Q H2O en vez de DNA (opcional).

Haga vórtex full y spin por 5 seg al tubo Single Standard (tapa roja) antes de usarlo. Repita el proceso con las muestras (3 veces - vórtex de 5 pulsos cortos).

Saque un rack frio del congelador y coloque allí los tubos pre-pre-PCR para continuar los siguientes pasos en frío. 

Nota: Procuré hacer el proceso lo más rápido posible para no congelar las muestras en el rack. 

Agrege 1 uL de Single Standard (tapa roja) en cada tubo, recuerde cambiar de punta en cada proceso. 

Nota: Procuré absorver el líquido de manera perpendicular sin inclinar el tubo dado su viscosidad. 

Haga vórtex de 5 pulsos a los tubos y spin para homogenizar (3 veces).
Lleve las muestras al termociclador a 98°C y comience el proceso donde las muestras se mantienen por 3 minutos a 98°C para el choque térmico.

Nota: Recuerde estar atento del tiempo, finalizados los 3 minutos inmediatamente coloque los tubos en un rack recién sacado del REVCO -20°C que se encuentre completamente frío para llevar a cabo el choque térmico.  

Una vez terminado el ciclo de 3 minutos en el termociclador se colocan las muestras en un nuevo rack bien frío, ejerciendo presión sobre los tubos para evitar que salgan volando. Deje las muestras en reposo en el rack por 2 minutos. 

Incubación Master Mix

Nota: Los siguientes pasos los hace en el mismo rack frío donde dejo las muestras tras el choque térmico. 

Haga vórtex y spin a los tubos de los Adaptadores por 5 seg (3 veces) antes de utilizarlo 
Agrege 1 uL de Adaptador A en cada tubo de muestra
Agrege 1 uL de Adaptador B en cada tubo de muestra

Haga “flick”, vórtex y spin al Master Mix por 30 seg antes de usar (3-5 veces), en este caso es mejor sobre-vortear que no, ya que el reactivo es muy viscoso. 
Agrege 13 uL de MM para obtener un total de 25 uL de volumen total en cada tubo, mezcle el líquido con la punta (opcional) y recuerde pipetear el MM suavemente dado la viscosidad.
Haga  vórtex (5 pulsos ~20seg) y spin corto de 5 seg 

Nota: Tenga cuidado de no sobre-homogeneizar las muestras.

En el termociclador a 37°C llevar las muestras para el siguiente paso de incubación. 
t = ~1h

Nota: Recuerde retornar el kit SRLSY a su lugar para mantener su temperatura. 

Limpieza de las muestras usando Beads de purificación 

Antes de comenzar:
Aliste y/o uvee el material a utilizar por al menos 5 minutos (300 seg)


Guantes
Sharpies
Tubos PCR single connection (final pre-PCR tubes)
Puntas 10 uL y 200 uL
Racks
Milli-Q H2O con tapa abierta
3 Canaletas blancas de plástico (Beads, milli-Q H2O, EtOH 80% fresco)



Nota: Los beads se encuentran alicuotados en la nevera. Además hay más un tubo de colecta de 50 mL cubierto con aluminio, si llega a necesitar.

Nota: Las canaletas blancas de plásticos las va a necesitar para verter allí el miliQ-H2O, los beads y el EtOH 80% para luego hacer uso de las multipipetas. Recuerde que cada canaleta esta marcada con el reactivo correspondiente.

Haga vórtex a la Solución de Beads antes de utilizar, de tal manera que observe como el tubo tiene un tono homogéneo y dejela a T° ambiente
Preparar EtOH 80% en un tubo de colecta de 50 mL para que esté fresco. Puede usar uno ya preparado de al menos 1 semana. (40 mL EtOH 80% y 10 mL miliQ-H2O) 

Procedimiento:

Nota: Para el proceso de limpieza alistar racks metálicos. El volumen de Beads agregados para llevar a cabo la limpieza depende del volumen de líquido en los tubos donde se encuentran las muestras. 
>Beads <Volumen = >fragmentos largos.

Nota: Para ahorrar tiempo en este proceso puede hacer uso de la multipipeta y las canaletas.

Retire los tubos pre-pre-PCR del termociclador.
Agrege 37.5 uL milli-Q H2O a cada uno de los tubos pre-pre-PCR que saco del termociclador y posteriormente, haga “flick” y un spin corto para homogeneizar.

Agrege 29.25 uL de Beads en cada tubo pre-pre-PCR. Homogenice haciendo flick a los tubos de tal manera que los vea de un solo tono y haga un spin corto.
Deje los tubos en reposo por 10 min en un rack de plástico.
Pase los tubos al rack de anillos metálico por 5 min, más o menos dependiendo de cómo se vean las muestras limpias. 

Pasados los 5 min, trabajando sobre el mismo rack metálico. Retire el sobrenadante (~100 uL) y descarte. 

Nota: Para retirar permita que la punta toque el fondo del tubo y absorba. Intente recuperar la mayor cantidad posible del sobrenadante y que el nivel en las puntas sea el mismo.   

Agregar 190 uL de EtOH 80%  y espere 30 seg.
Rápidamente retire el sobrenadante (~200 uL) y descarte. Para evitar que el etanol dañe el ADN.
Agregar 190 uL de EtOH 80%  y espere 30 seg.
Rápidamente retire el sobrenadante (~200 uL) y descarte. Para evitar que el etanol dañe el ADN.
Deje secar los tubos con las tapas abiertas por 5-10 min. En el mismo rack magnético.

Nota: Faltando 3 min sacar ~10 uL de sobrenadante para asegurar el secado de las muestras y que esta limpio de EtOH 80%, pero sin sobresecar las muestras. 

Coloque los tubos en el rack de plástico y agregue 15 uL de milli-Q H2O a cada tubo. Haga “flick” a los tubos, de tal manera que mezcle todo muy bien y luego hace spin rápido y dejar en reposo por 2 min en un rack plástico.
 
Pase los tubos al rack metálico paralelo (optimizado para menos de 30 uL de volumen) y dejar allí en reposo por 2 min o hasta que se encuentren limpios los tubos. 

Nota: Para colocar los tubos en este rack lleve a cabo una pequeña presión de tal manera que los tubos quedan “bien adheridos” a las paredes del rack de forma paralela y que si usted intenta moverlos no sea sencillo. 

Tome 20 uL del sobrenadante y transfieralos a los nuevos tubos pre-PCR y se descarte los anteriores. 

Nota: Como esta trabajando sobre el rack con los tubos en paralelo asegúrese de que se encuentran fijos a las paredes y puede retirar el volumen sin mezclar nuevamente los beats con el líquido, pues los beats quedan pegados a fondo a la pared. 

Reservar tubos pre-PCR a 4°C para la PCR o a -20°C por más de un mes. 









































CUARTA PARTE
PCR

Antes de comenzar:
PCR Kit: 
Index PCR
Index PCR Master Mix

Los Index se encuentran en el REVCO -20°C en diferentes racks. Siempre los índex van por pares, forward con sus correspondientes reverse. 

Marcar y uvear material a utilizar


Guantes
Sharpies
Tubos PCR triple connection
Puntas
Racks
TE-Buffer con tapa abierta
3 Canaletas blancas de plástico (Beads, TE-Buffer, EtOH 80% fresco)



Nota: Para la PCR tener en cuenta tubos de PCR adicionales para correr la PCR en duplicado por muestra. 

Nota: La PCR Master Mix se encuentra dentro de la misma caja del SRSLY Kit y es aquel tubo de tapa transparente. Igual que los demás reactivos, se debe dejar descongelar, pero luego de descongelada se debe mantener en un rack frío. 

Nota: Los index se encuentran también a -20°C se deben dejar descongelar, pero mantener luego en un rack frío.

Nota: Antes de comenzar revise el Google Sheet para conocer los ciclos que debe llevar acabo la PCR de acuerdo con la información correspondiente de su muestra. Dado el caso que no todas sus muestras requieran el mismo número de ciclos, utilice más de un termociclador a la vez. 

Procedimiento:
PCR

Tome la PCR MM y haga vórtex y spin antes de usar
Agregar 12.5 uL PCR MM a los nuevos tubos de PCR vacíos haciendo uso de la pipetea electrónica
Tome los tubos con los índex hágales “flick” y un spin corto antes de usarlos. 
Mueva los tubos PCR del rack de plástico a un rack frío antes de añadir los index
Agregar 2.5 uL de cada uno de los índex y se agregan en cada tubo PCR con MM
Haga “flick” y spin a los tubos con las muestras de ADN para homogeneizar antes de utilizarlos (tubos librerías o pre-PCR) 
Agregar 7.5 uL de cada uno de los tubos librerías en los tubos PCR. Hacer “flick”, vórtex y un spin corto a los tubos PCR (3 veces). 

Nota: En este punto solo se han llenado 1 tubo por cada muestra, pero se hará la PCR por duplicado. En este caso los tubos tienen un volumen total de 25 uL.

Tomar 12.5 uL de la mezcla para PCR en cada uno de los tubos para duplicado. De tal manera que todos los tubos para PCR tendrán un volumen final igual. 
Hacer spin a cada uno de los tubos PCR 
Llevar los tubos PCR al termociclador. Usar el protocolo SRSLY-IndexPCR. Modifica el valor de volumen, si es necesario. Y modifica el número de repeticiones también en el step 5 si esto es necesario (de acuerdo a la info revisada en el google sheet). Tenga presente, si la muestra se hará por 8 ciclos entonces modifica a 7x = 8 repeticiones. Esto depende de la concentración de la muestra inicial.

Nota: El proceso en el termociclado toma ~20 min. 

Limpieza de productos PCR usando Beads de purificación

Antes de comenzar:
Uvear materiales (racks, guantes, nuevos tubos PCR triple connection, TE Buffer-con la tapa abierta-) 
Sacar de la nevera la solución de Beads y dejarla a T° ambiente antes de utilizarlo. 

Nota: En este proceso requerirá en total 3 tubos PCR-triple connection por muestra a analizar. Adicionalmente, recuerde que los Beats son sensibles a la luz. 

Finalizada la PCR se le hace spin a todos los tubos
Hacer vórtex al Bead Mix tube antes de ser utilizado
Tome los 12.5 uL de los tubos de PCR duplicado y pasarlos a los otros tubo de PCR “originales” o viceversa, da igual. Con el fin de combinarlos nuevamente, de tal manera que la limpieza se lleva a cabo sobre el volumen total de 25 uL. Descarta los tubos vacíos. Y hace “flick” y spin a los tubos para homogenizar. 

Agrege 20 uL de Bead Mix tube a cada uno de los tubos PCR y hacer “flick” y spin 
Dejar tubos en reposo por 10  min en el rack de plástico
Pasar los tubos al rack metálico de anillos por 5 min
Luego tome 45 uL de los tubos PCR y transferirlos a unos nuevos tubos cada uno. Descartando los tubos vacíos. 

Nota: En este proceso de limpieza, comparado con el anterior que se hace antes de la PCR, en este caso se hace el proceso 2 veces variando el volumen de Beads agregado (en el anterior se hizo para limpieza de reads largos y el siguiente es para limpieza de reads más cortos). De la siguiente manera: 

Hacer vórtex al Bead Mix tube antes de ser utilizado (si es necesario) 
Tomar 12.5 uL de Beads Solution y agregarlos a cada tubo. Hacer “flick” y spin para homogenizar. 
Dejar tubos en reposo por 10 min en el rack de plástico.
Pasar los tubos al rack metálico de anillos por 5 min.

Tomar 57.5 uL del sobrenadante y descartarlos

Agregar 190 uL de EtOH 80%  y espere 30 seg.
Rápidamente retire el sobrenadante (~200 uL) y descarte. Para evitar que el etanol dañe el ADN.
Agregar 190 uL de EtOH 80%  y espere 30 seg.
Rápidamente retire el sobrenadante (~200 uL) y descarte. Para evitar que el etanol dañe el ADN.
Deje secar los tubos con las tapas abiertas por 5-10 min. En el mismo rack magnético.

Nota: Faltando 3 min sacar ~10 uL de sobrenadante para asegurar el secado de las muestras y que esta limpio de EtOH 80%, pero sin sobresecar las muestras. 

Nota: Mientras los tubos están en reposo puede ir alistando las soluciones para el siguiente paso que es el Bioanalyzer. Solo sí, es el siguiente paso que va a hacer y será el mismo día, de lo contrario, no lo haga y prosiga con el protocolo y almacene las muestras hasta que las vaya a revisar en el Bioanalyzer. 

DNA Dye Concetrate → Trasladar toda la solución al tubo de tapa roja. Hacer Spin y pasar toda la solución a un Eppendorf con filtro (Gel Dye Matrix) 

Llevar el Gel Dye Matrix a la centrifuga (no olvide balancearla) por 15 min a 2240 g (rcf) y dejar a T° ambiente al menos 30 min antes de usar. 

Marcar los nuevos y finales tubos PCR (CT 001 PCR) tanto en la tapa como en el lateral del tubo. 

Retirar los tubos del rack magnético, colocolelos en un rack plástico y agregue 20 uL de TE Buffer a cada tubo. Haga “flick” y spin corto, y dejar en reposo por 2 min en rack de plástico. 
Mover los tubos al rack magnético paralelo por 2 min o hasta que los tubos se vean limpios 
Tomar 20-25 uL del sobrenadante y trasladarlo a los nuevos tubos PCR finales.
Haga spin corto a lo snuevos tubos

Cuantificación del ADN en la librería preparada, siguiendo el protocolo para QuBit nombrado anteriormente. 

Lleve a cabo la medición de la concentración de ADN

Nota: No olvide dejar los reactivos a temperatura ambiente antes de utilizarlos. 

Nota: En esta ocasión por encima de 2 ng/mL es una buena concentración de ADN. Si esta por debajo, el problema pudo haber sido en la PCR, por lo que probablemente se requiera 1 o 2 ciclos adicionales de PCR en esa muestra. De todas maneras en ese caso pues hay que repetir el ensayo. 

Reservar tubos a -20°C hasta llevar a Bioanalyzer 






QUINTA PARTE
BIOANALYZER 

Nota: A continuación hay un pequeño protocolo para llevar a cabo la corrida de las muestras en el bioanalyzer. Sin embargo, el protocolo de la máquina se encuentra en el kit sobre la nevera 4°C y también en el cajón donde se encuentre la máquina. 

Procedimiento:
Montando chip en el Bioanalyzer

Antes de empezar: 
Dejar descongelar los tubos finales obtenidos tras la PCR 
Alistar bioanalyzer kit que se encuentra dentro la nevera de 4°C y dejarlo a temperatura ambiente, con al menos 30 minutos de antelación, antes del análisis. Adicionalmente, deje listo el chip a usar y el rack de muestras que se descongele. 

Nota: Recuerde manipular el chip y demás con guantes (no deben estar esterilizados).

Nota: Los reactivos del Kit son sensibles a la luz, así que evite exponerlos por prolongados periodos a la luz. 

Agregar 350 uL de mili-Q H2O en cada esquina del chip tomado del mueble. Luego colocar en la máquina (bioanalyzer) para la limpieza por 30 seg, terminado el tiempo se saca y lo deja afuera. 

Hacer vórtex y spin al Gel Dye Mix antes de usar, brevemente.  
Colocar el chip nuevo en el chip priming station (plataforma negra con la jeringa) 
Agregar 9 uL de Gel Dye Mix en la G en todo el centro y reventar la burbuja si ésta se forma. 
Asegurese que el émbolo esté colocado en 1 ml y luego cierre el chip priming station. Generar una presión estable, no completamente rápida o lenta sobre el chip usando la jeringa hasta que suena el clip. Asegurese que Cuando toca el fondo toma 60 seg de temporizador, pasando este tiempo se devuelve “solo”, espera 5 seg y luego se le auda a la jeringa en el proceso. 

Abre la plataforma negra y agrega 9 uL de Gel Dye Mix en cada espacio de la misma fila donde esta la G. Recuerde ir cambiando la punta siempre. 

Tomar 5 uL del Marker (tapa verde) y agregar en cada uno de los espacios para las muestras y en el Well marked (donde esta la escalera). No dejar ningún espacio vacío. Recuerde ir cambiando la punta siempre.  

Agregue 1 uL de High Sensibility DNA ladder (tapa amarilla) en el marcador de escalera.

Agregar 1 uL de su muestra correspondiente en cada espacio de acuerdo a como lo quiere ordenar. 

Nota: Si va a dejar un pozo como negativo o no tiene suficientes muestras para la lectura del chip, sino que tal vez va a llevar a cabo el análisis con menos de 11 muestras. En vez de muestra usted añade 5 uL o 1 uL de marker del chip, idealmente para alcanzar un volumen por cada pozo de 6 uL. De esta manera el bioanalyzer no le enseñará un mensaje de error. Tenga en cuenta, que esto sería una adición al  negativo de las muestras que se hace como una muestra más, si es que usted contó con algún negativo en el proceso.  

Colocar el chip en el vórtex adaptado por 1 min a 2400 rpm. 
No deje pasar más de 5 minutos e introduzca el chip dentro de la máquina para correr el programa.

Revisión de la calidad de las librerías

Abrir en el PC el programa 2100 Expert Program
Colocar el chip en la máquina con el programa encendido 
Analyze → double (dsDNA) → high sensibility
Llenar sheet con información de las muestras - nombres → START
Tiempo de corrida: ~30 - 45 min en correr el chip completo
Lectura de gráficos (200 - 1000 pb) ; corte  DNA (250 - 1000 pb)  de acuerdo a los resultados obtenidos. 
