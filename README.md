# jump2digital
PROVA DATA SCIENCE HACKATÓ
## Project information

[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)


## Data sources / conjunts de dades.
[Rent prices / Llogers](https://opendata-ajuntament.barcelona.cat/data/es/dataset/est-mercat-immobiliari-lloguer-mitja-mensual/resource/0a71a12d-55fa-4a76-b816-4ee55f84d327)

[Noise / Soroll](https://opendata-ajuntament.barcelona.cat/data/es/dataset/poblacio-exposada-mapa-estrategic-soroll/resource/3846500e-72aa-4780-967f-f09aa184eaba)

[Accidents / Accidentes](https://opendata-ajuntament.barcelona.cat/data/ca/dataset/accidents_causa_conductor_gu_bcn/resource/1a05cdd4-4844-41a5-872d-a0824d11b517?inner_span=True)


## Mission / Missió.

|  |English     |Catala      |
|-|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------|
|1|Select two sets of data and unify them bearing in mind that our base set is that of rents|Seleccionar dos conjunts de dades i unificar-los tenint en conta que el nostre conjunt base és el dels lloguers.|
|2|Perform the necessary data pre-processing to ensure that the data is accurate.|Realitzar el preprocessament de dades necessari per garantir que les dades siguin precises.|
|3|Apply principal component analysis (PCA) to reduce the dimensions of the data set.|Aplicar una anàlisi de components principals per reduir les dimensions del conjunt de dades.| 


Un arxiu Jupyter Notebook amb totes les línies de codi executades i les interpretacions que
consideris necessàries.
- Un arxiu README amb la següent informació:
1. Introducció: Presentació del conjunt de dades i de les variables seleccionades.
2. Depuració de dades: Descripció detallada de les tècniques de preprocessat aplicades i els
criteris d’avaluació utilitzats.
3. Resultats: Presentació dels resultats obtinguts.
4. Conclusions: Principals inferències derivades dels resultats aconseguits. 

# Preus/Prices/Precios
          1         2         3         4         5          6         7         8         9         0          1         2         3         4         5
|12345678901234567890123456789012345678901234567890|12345678901234567890123456789012345678901234567890|12345678901234567890123456789012345678901234567890
|English     |Catala      |Español|
|__________________________________|___________________________________|____________________________________|
|----------------------------------|-----------------------------------|-----------------------------------|
|Prices for the years 2014 to 2023 come in annual files. They must be integrated into a single file. The prices for each neighborhood are quarterly. There are prices per square meter and monthly housing rental prices. In 2022 there is one quarter left and in 2023 there are two left. Six neighborhoods that have more NaN than data have been removed from the data set. IN a neighborhood that only had three quarters left, these three values have been estimated. For more [details](https://github.com/luismiguelcasadodiaz/jump2digital/blob/main/data/price/README.md)| Els preus del 2014 al 2023 vénen en arxius anuals. Cal integrar-los en un únic fitxer. Els preus de cada barri són trimestrals. Hi ha preus per metre quadrat i preus mensuals de lloguer d'habitatge. El 2022 en falta un trimestre i del 2023 en falten dos. S'han eliminat del conjunt de dades sis barris que tenen més NaN que dades. En un barri on només li faltaven tres trimestres s'han estimat aquests tres valors. Per tenir més [detalls](https://github.com/luismiguelcasadodiaz/jump2digital/blob/main/data/price/README.md)   |Los precios de los años 2014 al 2023 vienen en archivos anuales. Hay que integrarlos en un único archivo. Los precios de cada barrio son trimestrales.Hay precios por metro cuadrado y precios mensuales de alquiler de vivienda. En 2022 falta un trimestre y de 2023 faltan dos. Se han eliminado del conjunto de datos seis barrios que tiene mas NaN que datos. En un barrio al que solo le faltaban tres trimestres se han estimado estos tres valores. Para tener más [detalles](https://github.com/luismiguelcasadodiaz/jump2digital/blob/main/data/price/README.md)|


# Accidents/Accidents/Accidentes
|English     |Catala      |Español|
|__________________________________________________|__________________________________________________|__________________________________________________|
|--------------------------------------------------|--------------------------------------------------|--------------------------------------------------|
|The accident data from the years 2016 to 2022 are in annual files that must be integrated into one. Each of the 69,355 records corresponds to an accident file. There are 501 records for which the neighborhood of the accident is unknown. Of these, 30 do not even have the coordinates of the event. These 30 records are removed from the data set. For the remaining 471 records that have coordinates of the accident, we recover the neighborhood in 434 records. As part of the preprocessing of the accident data and with the intention of adding it to the price data, we summarize the number of accidents by neighborhood and quarter. More [details](https://github.com/luismiguelcasadodiaz/jump2digital/blob/main/data/accident/README.md)| Les dades dels accidents dels anys 2016 al 2022 estan en fitxers anuals que cal integrar en un. Cadascun dels 69.355 registres correspon a un expedient d'accident. Hi ha 501 registres per als quals no se sap el barri de l'accident. D'aquests, 30 no tenen ni tan sols les coordenades del succés. Aquests 30 registres s'eliminen del conjunt de dades. Pels 471 registres restants que tenen coordenades de l'accident, recuperem el barri a 434 registres. Com a part del preprocessament de les dades daccidents i amb la intenció dafegir-les a les dades de preus, fem un resum del nombre daccidents per barri i trimestre. Per tenir més [detalls](https://github.com/luismiguelcasadodiaz/jump2digital/blob/main/data/price/README.md)   |Los datos de los accidentes de los años 2016 a 2022 están en ficheros anuales que hay que integrare en uno. Cada uno de los 69 355 registros corresponde a un expediente de accidente. Hay 501 registros para los  que se desconoce el barrio del accidente. De estos 30 no tienen nisiquiera las coordenadas del suceso. Estos 30 registros se eliminan del conjunto de datos. Para los 471 registres restantes que tienen coordenadas del accidente, recuperamos el barrio en 434 registros. Como parte del preprocesamiento de los datos de accidentes y con la intención de agregarlos a los datos de precios, hacemos un resumen del número de accidentes por barrio y trimestre. [detalles](https://github.com/luismiguelcasadodiaz/jump2digital/blob/main/data/accident/README.md)|




