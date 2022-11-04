# PI02_machine_learning
# Proyecto individual 2

​
## Información relevante
​
Este proyecto es una instancia de evaluación, por lo cual es INDIVIDUAL y OBLIGATORIO para los alumnos de Data Science de Henry. Se disponibilizará un Google Form y pueden cargarse los resultados las veces que quieran. Es obligatorio que todos disponibilicen el código utilizado, para validar los modelos construidos.
​
## Mercado inmobiliario
​
Dentro de la sociedad globalizada e industrializada, es sabido que los precios de los inmuebles han presentado un constante cambio, por lo que quienes deseen invertir o vender una propiedad se enfrentan al fenómeno especulativo existente en la valorización de éstos. Esto, debido a la constante tendencia de las ciudades a crecer demográfica y comercialmente, llegando a un punto en donde no se tiene certeza de la valorización real dentro del sector en donde se desee invertir. 
​
Pese a que el precio depende, en cierta medida, de las tendencias que esté teniendo el mercado inmobiliario en un determinado tiempo, poder estimar adecuadamente el valor de una propiedad es una referencia clave para entender si es una buena oportunidad, ya sea de compra o de venta.
​
## Descripción del problema
​
Usted ha sido contactado de una importante empresa inversora dentro del rubro de la inmobiliaria en Colombia, con el fin de que implemente un modelo de clasificación que permita clasificar el precio de las propiedades en venta, utilizando los datos que se han puesto a su disposición correspondientes al año 2020.
​
Para esto, específicamente, debe predecir la **categorización** de las propiedades entre baratas o caras, considerando como criterio el valor promedio de los precios (la media). 
​
## Métrica a utilizar
​
Como método de evaluación del desempeño del modelo, se utilizará la métrica de Exhaustividad (Recall) para las propiedades caras, a partir de la matriz de confusión (Confusion Matrix). 
​
$$ Recall=\frac{TP}{TP+FN}$$
​
Donde $TP$ son los verdaderos positivos y $FN$ los falsos negativos.

Adicionalmente, se incluye la Accuracy como métrica de control.
​
## Archivos provistos
​
Se proveen los archivos dentro del archivo comprimido 'properties_colombia.zip':
 - 'properties_colombia_train.csv': Contiene 197549 registros y 26 dimensiones, el cual incluye la información **numérica** del precio.
 - 'propiedades_colombia_test.csv': Contiene 65850 registros y 25 dimensiones, el cual no incluye la información del precio. 
​
## Descripción de las dimensiones
- id - Identificador del aviso. No es único: si el aviso es actualizado por la inmobiliaria (nueva versión del aviso) se crea un nuevo registro con la misma id pero distintas fechas: de alta y de baja.
- ad_type - Tipo de aviso (Propiedad, Desarrollo/Proyecto).
- start_date - Fecha de alta del aviso.
- end_date - Fecha de baja del aviso.
- created_on - Fecha de alta de la primera versión del aviso.
- lat - Latitud.
- lon - Longitud.
- l1 - Nivel administrativo 1: país.
- l2 - Nivel administrativo 2: usualmente provincia.
- l3 - Nivel administrativo 3: usualmente ciudad.
- l4 - Nivel administrativo 4: usualmente barrio.
- l5 - Nivel administrativo 5.
- l6 - Nivel administrativo 6.
- rooms - Cantidad de ambientes.
- bedrooms - Cantidad de dormitorios (útil en el resto de los países).
- bathrooms - Cantidad de baños.
- surface_total - Superficie total en m².
- surface_covered - Superficie cubierta en m².
- price - Precio publicado en el anuncio.
- currency - Moneda del precio publicado.
- price_period - Periodo del precio (Diario, Semanal, Mensual)
- title - Título del anuncio.
- description - Descripción del anuncio.
- property_type - Tipo de propiedad (Casa, Departamento, PH).
- operation_type - Tipo de operación (Venta).
- geometry - Puntos geométricos formados por las coordenadas latitud y longitud. 
​
## Observaciones:
​
Luego de realizada la exploración se observó la ubicación de las propiedades. Sacando dos outliers se obtuvo:
![01Mapa](https://user-images.githubusercontent.com/104787036/200039439-6ec5492b-2b8d-4edf-b2a5-a93b2c8681b4.JPG)
