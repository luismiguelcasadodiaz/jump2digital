## Prices/Precio/Preu

|Pos|Field/Campo|Description/Descripció|
|:--|:----------|:---------------------|
|01|Any|Any de les dades|
|02|Trimestre|Trimestre de les dades|
|03|Codi_Districte|Codi del districte|
|04|Nom_Districte|Nom del districte|
|05|Codi_Barri|Codi del barri|
|06|Nom_Barri|Nom del barri|
|07|Lloguer_mitja|Lloguer mitjà mensual i lloguer mitjà per superfície|
|08|Preu|Preu lloguer|



|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|In the first 8 years there are 584 prices per year.|Els 8 primers anys hi ha 584 preus per any.|En los 8 primeros años hay 584 precios por año.|
|In each year we have one data per quarter (4 quarters).|A cada any tenim una dada per trimestre (4 trimestres).|En cada año tenemos un dato por trimestre (4 trimestres).|
|The quarterly data has two values: (2 prices) "Average monthly rent of an apartment" and "Average monthly rent of a m2"|La dada trimestral té dos valors: (2 preus) "Lloguer de mitjana mensual d'un pis" i "Lloguer de mitjana mensual d'un m2"|El dato trimestral tiene dos valores: (2 precios) "Alquiler promedio mensual de un piso" y "Alquiler promedio mensual de un m2"|
|Each of the 73 neighborhoods of Barcelona has records to contain this data.|Cadascun dels 73 barris de Barcelona té registres per contenir aquestes dades.|Cada uno de los 73 barrios de Barcelona tiene registros para contener esos datos.|
|In total 73 neighborhoods x 2 prices x 4 quarters = 584 registrations per year.|En total 73 barris x 2 preus x 4 trimestres = 584 registres cada any.|En total 73 barrios x 2 precios x 4 trimestres = 584 registros al año.|
|In 2022, the fourth quarter prices are missing. In 2023, the prices for the third and fourth quarters are missing.|L'any 2022 manquen els preus de quart trimestre. L'any 2023 manquen els preus del tercer i del quart quadrimestre.|En el año 2022 faltan los precios de cuarto trimestre. En el año 2023 faltan los precios del tercero y del cuarto cuatrimestre.|
|The price data has 5402 rows by 8 columns.|Les dades de preus tenen 5402 files per 8 columnes.|Los datos de precios tienen 5402 filas por 8 columnas|

 
|Camp/field/Campo|2014|2015|2016|2017|2018|2019|2020|2021|2022|2023|
|---|---|---|---|---|---|---|---|---|---|---|
|Any|584|584|584|584|584|584|584|584|438|292|
|Trimestre|584|584|584|584|584|584|584|584|438|292|
|Codi_Districte|584|584|584|584|584|584|584|584|438|292|
|Nom_Districte|584|584|584|584|584|584|584|584|438|292|
|Codi_Barri|584|584|584|584|584|584|584|584|438|292|
|Nom_Barri|584|584|584|584|584|584|584|584|438|292|
|Lloguer_mitja|584|584|584|584|584|584|584|584|438|292|
|Preu|546|552|553|546|540|538|538|584|406|273|

|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|What about missing data?|Què passa amb les dades faltants?|¿que pasa con los datos faltantes?|


|Camp/field/Campo|2014|2015|2016|2017|2018|2019|2020|2021|2022|2023|Total|
|--|----|----|----|----|----|----|----|----|----|----|-----|
|Preu = NaN0|38|32|31|38|44|46|46|44|32|19|=326

|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|In the Preu field, 326 records of the 5402 have no value. This is 6.03% of the data.|Al camp Preu, 326 registres dels 5402, no tenen valor. Això és un 6,03% de les dades.|En el campo Preu, 326 registros de los 5402, no tiene valor.Esto es un 6,03 % de los datos.|


|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|The first preprocessing treatment will be to unite the two existing price types into a single quarterly record, creating two new columns "Eur" and "Eur_m2" for this purpose. To do this, we first create a key that allows us to join the data later. This key has the neighborhood code, the year and the quarter. We divide the prices into two subsets: a subset with the records that contain the price of the type "Average monthly rent of an apartment" and another subset with the records that contain the price of the type "Average monthly rent of a m2." In each subset we appropriately rename the price column and merge the two subsets by the created key.|El primer tractament del preprocessat serà unir en un únic registre trimestral els dos tipus de preu existents, creat per a això dues noves columnes "Eur" i "Eur_m2". Per això es creem primer una clau que ens permeti unir les dades posteriorment. Aquesta clau té el codi de barri l'any i el trimestre. Dividim els preus en dos subconjunts: un subconjunt amb els registres que contenen el preu de tipus "Lloguer de mitjana mensual d'un pis" i un altre subconjunt amb els registres que conté el preu del tipus "Lloguer de mitjana mensual d'un m2". A cada subconjunt canviem adequadament el nom de la columna preu i fusionem els dos subconjunt per la clau creada.|El primer tratamiento del preprocesado será unir en  un único registro trimestrasl los dos tipos de precio existentes, creado para ello dos nueva columnas "Eur" y "Eur_m2". Para ellos creamos primero una clave que nos permita unir los datos posteriormente. Esta clave tiene el codigo de barrio el año y el trimestre. Dividimos los precios en dos subconjuntos: un subconjunto con los registros que contienen el precio de tipo "Alquiler promedio mensual de un piso" y otro subconjunto con los registros que contiene el precio del tipo "Alquiler promedio mensual de un m2". En cada subconjunto cambiamos adecuadamente el nombre de la columna precio y fusionamos los dos subconjunto por la clave creada.|
|The result of the transformation is 2701 rows of 7 columns:|El resultat de la transformació son 2701 files de 7 columnes:|El resultado de la transformación son 2701 filas de 7 columnas:|

||Any|Trimestre Nom_Districte|Nom_Barri|Eur|Clau|Eur_m2|
|----|---|---------|-------------|---------|---|----|------|
|0|2014|1|Ciutat Vella|el Raval|589.55|120141|10.76|
|1|2014|1|Ciutat Vella|el Barri Gòtic|712.79|220141|10.58|
|2|2014|1|Ciutat Vella|la Barceloneta|540.71|320141|14.40|
|2698|2023|2|Sant Martí|Provençals del Poblenou|1204.20|7120232|16.70|
|2699|2023|2|Sant Martí|Sant Martí de Provençals|960.90|7220232|13.20|
|2700|2023|2|Sant Martí|la Verneda i la Pau|991.10|7320232|14.50|



|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|When we analyze the records with NAN in the "Eur" column, we see that they are distributed throughout the data set.|Quan analitzem els registres amb NAN a la columna "Eur", veiem que estan repartits per tot el conjunt de dades.|Cuando analizamos los registros con NAN en la columna "Eur", vemos que están repartidos por todo el conjunto de datos.| 


|Trimestre| 1|2|3|4|sum|%|
|----|---:|---:|---:|---:|---:|---:|
|2014|5|3|5|6|19|6.51%|
|2015|6|2|4|4|16|5.48%|
|2016|2|5|4|4|15|5.14%|
|2017|5|4|5|5|19|6.51%|
|2018|6|5|6|5|22|7.53%|
|2019|6|6|6|5|23|7.88%|
|2020|4|7|6|6|23|7.88%|
|2021|6|5|6|5|22|7.53%|
|2022|6|5|5|nan|16|7.30%|
|2023|4|5|nan|nan|09|6.16%|
|**Tot**|**50**|**47**|**47**|**40**|**184**|**6.81%**|


|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|When we analyze the records with NAN in the "Eur_m2"" column, we see that they are distributed throughout the data set.|Quan analitzem els registres amb NAN a la columna "Eur_m2"", veiem que estan repartits per tot el conjunt de dades.|Cuando analizamos los registros con NAN en la columna "Eur_m2"", vemos que están repartidos por todo el conjunto de datos.| 


|Trimestre| 1|2|3|4|sum|%|
|----|---:|---:|---:|---:|---:|---:|
|2014|5|3|5|6|19|6.51%|
|2015|6|2|4|4|16|5.48%|
|2016|2|5|5|4|16|5.48%|
|2017|5|4|5|5|19|6.51%|
|2018|6|5|6|5|22|7.53%|
|2019|6|6|6|5|23|7.88%|
|2020|4|7|6|6|23|7.88%|
|2021|6|5|6|5|22|7.53%|
|2022|6|5|5|nan|16|7.30%|
|2023|5|5|nan|nan|10|6.84%|
|**Tot**|**51**|**47**|**48**|**40**|**186**|**6.81%**|



|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|The lack of prices affects 7 neighborhoods. We calculate the percentage of missing data considering 8 complete years (2014..2020), 32 quarters, plus three quarters of 2021, 35 quarters, plus two quarters of 2023, 37 quarters. 37 quarters are what a "complete" neighborhood should have.|La manca de preus afecta 7 barris. Calculem el percentatge de dades mancants considerant 8 anys complets (2014..2020), 32 trimestres, més tres trimestres del 2021, 35 trimestres, més dos trimestres del 2023, 37 trimestres. 37 trimestres són els que un barri “complet” hauria de tenir.|La falta de precios afecta a 7 barrios. Calculamos el porcentaje de datos faltantes considerando 8 años completos (2014..2020), 32 trimestres, mas tres trimestres del 2021, 35 trimestres, mas dos trimestres de 2023, 37 trimestres, son los que un barrio con toda la información debería tener.|


|Barri                     |Euros|Euros_m2|%datos faltantes|
|--------------------------|-----|--------|---|
|Baró de Viver             |   27|      27|73%|
|Can Peguera               |   32|      32|86%|
|Canyelles                 |    3|       3|08%|
|Torre Baró                |   23|      24|65%|
|Vallbona                  |   34|      34|92%|
|la Clota                  |   36|      36|97%|
|la Marina del Prat Vermell|   29|      30|81%|



|_________________________|_________________________|_________________________|
|-------------------------|-------------------------|-------------------------|
|We will estimate the 3 missing values in the Canyelles neighborhood, calculating the moving average of the previous values. The other six neighborhoods with missing data, due to the high number of missing data, we will delete from the price data set. Six neighborhoods for 37 records per neighborhood mean the deletion of 222 records.|Estimarem els 3 valors faltants al barri de Canyelles, calculant la mitjana mòbil dels valors previs. Els altres sis barris amb dades faltants, a causa de l'alt nombre de dades faltants, els esborrarem del conjunt de dades de preus. Sis barris per 37 registres per barri suposen la supressió de 222 registres.|Estimaremos los 3 valores faltantes en el barrio de Canyelles, calculando la media movil de los valores previos. Los otros seis barrios con datos faltantes, debido al alto número de datos faltantes, los borraremos del conjunto de datos de precios. Seis barrios por 37 registros por barrio suponen la supresion de 222 registros.|
|The result is saved in a csv file "prices_14_23.csv"|El resultat es desa en un fitxer csv "prices_14_23.csv"|El resultado se guarda en un archivo csv "prices_14_23.csv"|



![a](http:///home/luis/Documentos/python/jump2digital/data/price/barris_rank.png)

