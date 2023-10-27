## Accidents/Accidentes/accidents
Les dades d’aquest dataset complementen les d'Accidents gestionats per la Guàrdia Urbana a la ciutat de Barcelona
El valor '-1' en una cel·la indica que no es disposa de la dada.

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


Tras Concatenar los siete años de registros de accidentes, aunque todos los ficheros tienen 20 columnas, podemos obeservar estas anomalías:

	-El campo para la causa del accidente tiene dos nombres:
		-"Descripcio_causa_conductor" [2016 .. 2020].
		-"Descripcion_causa_mediata"  [2021 .. 2022].
	-Intercambio del contenido de dos campos.
		- "Descripcio_torn" tiene valores de "Descripcion_causa_Conductor" [2016..2020].

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

Tras la correción la vision global de los datos es está.


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

Es un set de datos de 69 355 fial spor 20 clumnas
