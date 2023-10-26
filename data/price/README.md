## Prices/Precio/Preu

|Pos|Field/Campo|Description/Descripció|
|:--|:----------|:---------------------|
|01|Any|<span style="color:#2d9bda">Any de les dades</span>|
|02|Trimestre|Trimestre de les dades|
|03|Codi_Districte|Codi del districte|
|04|Nom_Districte|Nom del districte|
|05|Codi_Barri|Codi del barri|
|06|Nom_Barri|Nom del barri|
|07|Lloguer_mitja|Lloguer mitjà mensual i lloguer mitjà per superfície|
|08|Preu|Preu lloguer|




Tenemos en cada año de los 8 primeros años 584 registros.
En cada año tenemos un dato por trimestre (4 trimestres)
El dato trimestral tiene dos valores: (2 precios)
	- Alquiler promedio mensual de un piso
	- Alquiler promedio mensual de un m2
Esos datos están para cada Barrio (73 Barrios)

73 barrios x 2 precios x 4 trimestres = 584 registros a año.

 
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

¿que pasa con los datos faltantes?

|Any = 0|
|Trimestre = 0| |Codi_Districte = 0| |Nom_Districte = 0| |Codi_Barri = 0| |Nom_Barri = 0| |Lloguer_mitja = 0| |Preu = 326|

En el campo Preu tenemos sin valor 326 registros de los 5402. un 6,03 % de los datos.

|Trimestre| 1|2|3|4|sum|
|----|----|----|----|----|----|
|2014|5.0|3.0|5.0|6.0|19.0|6.51%|
|2015|6.0|2.0|4.0|4.0|16.0|5.48%|
|2016|2.0|5.0|4.0|4.0|15.0|5.14%|
|2017|5.0|4.0|5.0|5.0|19.0|6.51%|
|2018|6.0|5.0|6.0|5.0|22.0|7.53%|
|2019|6.0|6.0|6.0|5.0|23.0|7.88%|
|2020|4.0|7.0|6.0|6.0|23.0|7.88%|
|2021|6.0|5.0|6.0|5.0|22.0|7.53%|
|2022|6.0|5.0|5.0|nan|16.0|7.30%|
|2023|4.0|5.0|nan|nan|09.0|6.16%|
||

En el año 2022 faltan los precios de cuarto trimestre
En el año 2021 faltan los precios del tercero y del cuarto cuatrimestre.

La falta de precios afecta a estos barrios:
Barris amb preus NaN ['Baró de viver' 'Can peguera' 'Canyelles' 'La clota'
 'La marina del prat vermell' 'Torre baró' 'Vallbona']

La cantidad de datos faltantes se ve en esta tabla

|Barri                     |Euros|Euros_m2|%datos faltantes|
|--------------------------|-----|--------|---|
|Baró de Viver             |   27|      27|73%|
|Can Peguera               |   32|      32|86%|
|Canyelles                 |    3|       3|08%|
|Torre Baró                |   23|      24|65%|
|Vallbona                  |   34|      34|92%|
|la Clota                  |   36|      36|97%|
|la Marina del Prat Vermell|   29|      30|81%|

Considerando 8 años completos (2014..2020), 32 trimestres, mas tres trimestres del 2021, 35 trimestres, mas dos trimestres de 2023, 37 trimestres, son los que un barrio con toda la información deberá tener.


Estimaremos los 3 valores faltantes en el barrio de Canyelles, calculando la media movil de los valores previos
 Los otros seis barrios con datos faltantes, debido al alto número de datos faltantes, los borraremos del conjunto de datos de precios. Seis barrios por 37 registros por barrio suponen la supresion de 222 registros.


