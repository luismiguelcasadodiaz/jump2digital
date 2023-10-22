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




Tenemos en cada año 584 registros.
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
|2014|10.0| 6.0|10.0|12.0|38.0|6.51%  |
|2015|12.0| 4.0| 8.0| 8.0|32.0|5.48%  |
|2016| 4.0|10.0| 9.0| 8.0|31.0|5.31%  |
|2017|10.0| 8.0|10.0|10.0|38.0|6.51%  |
|2018|12.0|10.0|12.0|10.0|44.0|7.53%  |
|2019|12.0|12.0|12.0|10.0|46.0|7.88%  |
|2020| 8.0|14.0|12.0|12.0|46.0|7.88%  |
|2022|12.0|10.0|10.0| nan|32.0|7,30%  |
|2023| 9.0|10.0| nan| nan|19.0|6,50%  |

En el año 2022 faltan los precios de cuarto trimestre
En el año 2021 faltan los precios del tercero y del cuarto cuatrimestre.

La falta de precios afecta a estos barrios:
Barris amb preus NaN ['Baró de viver' 'Can peguera' 'Canyelles' 'La clota'
 'La marina del prat vermell' 'Torre baró' 'Vallbona']

La cantidad de datos faltantes se ve en esta tabla

|loguer_mitja              |Lloguer mitjà mensual (Euros/mes) |Lloguer mitjà per superfície (Euros/m2 mes) |%datos faltantes|
|--------------------------|----------------------------------|--------------------------------------------|---|
|Baró de Viver             |                                25|                                          25|76%|
|Can Peguera               |                                28|                                          28|85%|
|Canyelles                 |                                 3|                                           3|09%|
|Torre Baró                |                                19|                                          20|61%|
|Vallbona                  |                                30|                                          30|91%|
|la Clota                  |                                32|                                          32|97%|
|la Marina del Prat Vermell|                                251                                          26|79%|

Considerando 7 años completos (2014..2020), 28 trimestres, mas tres trimestres del 2021, 31 trimestres, mas dos trimestres de 2023, 33 trimestres, son los que un  barrio con toda la información deberá tener. 

Estimaremos los 3 valores faltantes en el barrio de Canyelles, calculando la media movil de los valores previos

