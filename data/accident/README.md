## Accidents/Accidentes/accidents
|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|The details of this dataset complement the Accidents managed by the Urban Guard in the city of Barcelona|Les dades d’aquest dataset complementen les d'Accidents gestionats per la Guàrdia Urbana a la ciutat de Barcelona|El detalle de este conjunto de datos complementa los Accidentes gestionados por la Guardia Urbana en la ciudad de Barcelona.|
|The value '-1' in a cell indicates that it does not have that data. |El valor '-1' en una cel·la indica que no es té aquesta dada.|El valor '-1' en una celda indica que no se tiene ese dato.|

|Pos|Field/camp|Field description /Camp	Descripció|
|:--|:---------|:----------------------------------------------------------|
|01|Numero_expedient|Número d'expedient|
|02|Codi_districte|Codi del districte|
|03|Nom_districte|Nom del districte|
|04|Codi_barri|Nom del barri|
|05|Nom_barri|Nom del barri|
|06|Codi_carrer|Codi del carrer|
|07|Nom_carrer|Nom carrer|
|08|Num_postal|Número postal|
|09|Descripcio_dia_setmana|Nom del dia de la setmana|
|10|NK_Any|Any|
|11|Mes_any|Mes de l'any|
|12|Nom_mes|Nom del mes|
|13|Dia_mes|Dia del mes|
|14|Hora_dia|Hora del dia|
|15|Descripcio_causa_mediata|Descripció causa mediata|
|16|Descripcio_torn|Descripció del torn|
|17|Coordenada_UTM_X_ED50|Coordenada X en format UTM (ED50)|
|18|Coordenada_UTM_Y_ED50|Coordenada Y en format UTM (ED50)|
|19|Longitud_WGS84|Longitud|
|20|Latitud_WGS84|Latitud|


|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|After concatenating the seven years of accident records, although all the files have 20 columns, we can observe these anomalies:i|Després de Concatenar els set anys de registres d'accidents, tot i que tots els fitxers tenen 20 columnes, podem observar aquestes anomalies: |Tras Concatenar los siete años de registros de accidentes, aunque todos los ficheros tienen 20 columnas, podemos obeservar estas anomalías:|
|1. The field for the cause of the accident has two names: "Descripcio_causa_conductor" [2016 .. 2020] and "Descripcion_causa_mediata" [2021 .. 2022].|1. El camp per a la causa de l'accident té dos noms: "Descripcio_causa_conductor" [2016.. 2020] i "Descripcio_causa_mediata" [2021.. 2022].|1. El campo para la causa del accidente tiene dos nombres: "Descripcio_causa_conductor" [2016 .. 2020] y "Descripcion_causa_mediata"  [2021 .. 2022].|
|2. Exchange of the content of two fields. "Descripcio_torn" has values of "Descripcion_causa_Conductor" [2016..2020].|2. Intercanvi del contingut de dos camps. "Descripcio_torn" té valors de "Descripcio_causa_Conductor" [2016..2020].|2. Intercambio del contenido de dos campos. "Descripcio_torn" tiene valores de "Descripcion_causa_Conductor" [2016..2020].|


| |2016|2017|2018|2019|2020|2021|2022|
|--------------- |---:|---:|---:|---:|---:|---:|---:|
|Numero_expedient|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Codi_districte|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Nom_districte|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Codi_barri|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Nom_barri|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Codi_carrer|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Nom_carrer|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9319.0|
|Num_postal|10510.0|11089.0|10835.0|11018.0|7589.0|8979.0|9319.0|
|Descripcio_dia_setmana|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|NK_Any|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Mes_any|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Nom_mes|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Dia_mes|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Hora_dia|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Descripcio_torn|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Descripcio_causa_conductor|10510.0|11091.0|10835.0|11025.0|7595.0|NaN|NaN|
|Coordenada_UTM_X_ED50|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Coordenada_UTM_Y_ED50|10510.0|11091.0|10835.0|11025.0|7595.0|8979.0|9320.0|
|Longitud|10510.0|11091.0|10835.0|11025.0|7595.0|8949.0|9320.0|
|Latitud|10510.0|11091.0|10835.0|11025.0|7595.0|8949.0|9320.0|
|Descripcio_causa_mediata|NaN|NaN|NaN|NaN|NaN|8979.0|9320.0|

|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|After the correction, the global view of the data is this:|Després de la correcció, la visió global de les dades és aquesta:|Tras la correción, la visión global de los datos es esta:|


||2016|2017|2018|2019|2020|2021|2022|
|-----------|----|----|----|----|----|----|----|
|Numero_expedient|10510|11091|10835|11025|7595|8979|9320|
|Codi_districte|10510|11091|10835|11025|7595|8979|9320|
|Nom_districte|10510|11091|10835|11025|7595|8979|9320|
|Codi_barri|10510|11091|10835|11025|7595|8979|9320|
|Nom_barri|10510|11091|10835|11025|7595|8979|9320|
|Codi_carrer|10510|11091|10835|11025|7595|8979|9320|
|Nom_carrer|10510|11091|10835|11025|7595|8979|9319|
|Num_postal|10510|11089|10835|11018|7589|8979|9319|
|Descripcio_dia_setmana|10510|11091|10835|11025|7595|8979|9320|
|NK_Any|10510|11091|10835|11025|7595|8979|9320|
|Mes_any|10510|11091|10835|11025|7595|8979|9320|
|Nom_mes|10510|11091|10835|11025|7595|8979|9320|
|Dia_mes|10510|11091|10835|11025|7595|8979|9320|
|Hora_dia|10510|11091|10835|11025|7595|8979|9320|
|Causa|10510|11091|10835|11025|7595|8979|9320|
|Torn|10510|11091|10835|11025|7595|8979|9320|
|Coordenada_UTM_X_ED50|10510|11091|10835|11025|7595|8979|9320|
|Coordenada_UTM_Y_ED50|10510|11091|10835|11025|7595|8979|9320|
|Longitud|10510|11091|10835|11025|7595|8949|9320|
|Latitud|10510|11091|10835|11025|7595|8949|9320|

|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|It is a data set of 69,355 rows by 20 columns. It has 30 records with NaN in Longitude and Latitude and with unknown UTM coordinates (-1). We delete those 30 records from the dataset.|És un set de dades de 69 355 files por 20 columnes.Té 30 registres amb NaN a Logitud ia Latitud i amb les coordenades UTM desconegudes (-1). Esborrem del dataset aquests 30 registres.|Es un set de datos de 69 355 filas por 20 columnas.Tiene 30 registros con NaN en Logitud y en Latitud y con las coordenadas UTM desconocidas (-1). Borramos del dataset esos 30 registros.|


|Nom_barri|Nom_carrer|Coordenada_UTM_X_ED50|Coordenada_UTM_Y_ED50|Longitud|Latitud|
|---------|----------|---------------------|---------------------|--------|-------|
|52129|Desconegut|Desconegut|-1.0|-1.0|NaN|NaN|
|52130|Desconegut|Desconegut|-1.0|-1.0|NaN|NaN|
|52131|Desconegut|Desconegut|-1.0|-1.0|NaN|NaN|
|52132|Desconegut|Desconegut|-1.0|-1.0|NaN|NaN|
|52133|Desconegut|Desconegut|-1.0|-1.0|NaN|NaN|
|||||||
|58948|Desconegut|Desconegut|-1.0|-1.0|NaN|NaN|
|58949|Desconegut|Desconegut|-1.0|-1.0|NaN|NaN|


|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|There are still 471 accidents whose neighborhood is unknown, but they have the coordinates of the accident site. Let's try to find out in which neighborhood it happened.|Encara queden 471 accidents el barri dels quals és desconegut, però tenen les coordenades del lloc de l'accident. Intentarem esbrinar en quin barri han passat.|Aún quedan 471 accidentes cuyo barrio es desconocido, pero que tienen las coordenadas del lugar del accidente. Vamos a intentar averiguar en que barrio han sucedido.|


|Nom_barri|Nom_carrer|Coordenada_UTM_X_ED50|Coordenada_UTM_Y_ED50|Longitud|Latitud|
|---------|----------|---------------------|---------------------|--------|-------|
|1281|Desconegut|Desconegut|426830.03|4576250.78|2.124450|41.332574|
|1|Desconegut|ALMIRALL CERVERA / Sevilla ...|432316.21|4581276.81|2.154737|41.376367|
|2|Desconegut|NÚMERO 3 / E ...|427265.97|4576644.81|2.157427|41.381284|
|3|Desconegut|RDA DALT (BESÒS) ...|424991.14|4581760.18|2.157427|41.381284|
|0|Desconegut|NÚMERO 6 / A ...|427519.99|4575229.36|2.165891|41.375166|


|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|With the help of `geopandas` we import a Shapefile with the polygons of the Barcelona neighborhoods and do a `join within` to determine which polygons contain the coordinates of the accidents. This allows us to locate 434 accidents of the 471 we had with the unknown location. With this we get a data set of 69,288 rows and 20 columns.|Amb l'ajuda de `geopandes` importem un Shapefile amb els polígons dels barris de Barcelona i fem un `join within` per determinar quins polígons contenen les coordenades dels accidents. Això ens permet localitzar 434 accidents dels 471 que teníem amb la ubicació desconeguda. Amb això aconseguim un set de dades de 69 288 files i 20 columnes.|Con la ayuda de `geopandas` importamos un Shapefile con los polígonos de los barrios de Barcelona y hacemos un `join within` para determinar que polígonos contienen las coordenadas de los accidentes. Esto nos permite localizar 434 accidentes de los 471 que teníamos con la ubicación desconocida. Con esto conseguimos un set de datos de 69 288 filas y 20 columnas.|
|We summarize the accident data by neighborhood and by quarter to, in the transformation phase, add them to the price data. Apart from counting the accidents by quarter in the neighborhood, we break them down into those that have occurred in each of the time intervals (morning, afternoon and night) in absolute numbers and percentage. A view of the result is:|Resumim les dades d'accidents per barri i per trimestre per afegir, a la fase de transformació, les dades de preus. A part comptar els accidents per trimestre al barri, els desglossem en els que han passat en cadascun dels intervals horaris (matí tarda i nit) en números absoluts i en percentatge. Una vista del resultat és: |Resumimos los datos de accidentes por barrio y por trimestre para, en la fase de transformación, añadirlos a los datos de precios. A parte contar los accidentes por trimestre en el barrio, los desglosamos en los que han ocurrido en cada uno de los intervalos horarios (mañana tarde y noche) en números absolutos y en porcentaje. Una vista del resultado es:|


||Clau|Accidents|Mat|Tar|Nit|Mat_P|Tar_p|Nit_p|
|-|----|---------|---|---|---|-----|-----|-----|
|0|0320163|1|1.0|0.0|0.0|1.000000|0.000000|0.000000|
|1|0320192|1|0.0|1.0|0.0|0.000000|1.000000|0.000000|
|2|0420172|1|0.0|1.0|0.0|0.000000|1.000000|0.000000|
|3|0420182|1|0.0|1.0|0.0|0.000000|1.000000|0.000000|
|4|0420183|1|1.0|0.0|0.0|1.000000|0.000000|0.000000|
|...|...|...|...|...|...|...|...|...|
|1540|920212|104|37.0|57.0|10.0|0.355769|0.548077|0.096154|
|1541|920213|120|53.0|59.0|8.0|0.441667|0.491667|0.066667|
|1542|920221|105|33.0|57.0|15.0|0.314286|0.542857|0.142857|
|1543|920222|100|41.0|46.0|13.0|0.410000|0.460000|0.130000|
|1544|920223|117|51.0|51.0|15.0|0.435897|0.435897|0.128205|


|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|Remember here that the key is made up of the neighborhood code, the year and the quarter. The result is saved in a csv file "accidents_trimestrals_16_22.csv"|Recordeu aquí que la clau està formada pel codi del barri, l'any i el trimestre. El resultat es desa en un fitxer csv "accidents_trimestrals_16_22.csv"|Recordar aqui que la clave está formada por el código del barrio, el año y el trimestre. El resultado se guarda en un archivo csv "accidents_trimestrals_16_22.csv"|



