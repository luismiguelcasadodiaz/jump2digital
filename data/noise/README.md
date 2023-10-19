## Noise/Ruido/soroll
|  |General description/Descripción general/Descripció Geral|
|--|-------------------------------------------------------------------------------------------------------------------------|
|CA| Les xifres de població provenen de la lectura del padró de l'any corresponent. Els percentatges que es mostren són respecte a la població del barri, districte o ciutat, segons el recurs corresponent. Per l'avaluació del soroll hi ha tres períodes horaris definits per normativa. El període dia és de 7.00 a 21.00 hores; el vespre, de 21.00 a 23.00 hores; i la nit, de 23.00 a 7.00 hores. D'aquests tres períodes s'obtenen els índexs acústics Ld, Le i Ln. A més, hi ha un quart índex acústic, el ponderat dia-vespre-nit (Lden), que correspon a una mitjana ponderada dels índexs Ld, Le i Ln, penalitzant els períodes vespre i nit.|
|ES| Las cifras de población provienen de la lectura del padrón del año correspondiente. Los porcentajes que se muestran son respecto a la población del barrio, distrito o ciudad, según el recurso correspondiente. Para la evaluación del ruido hay tres períodos horarios definidos por normativa. El período día es de 7.00 a 21.00 horas; la tarde, de 21.00 a 23.00 horas; y la noche, de 23.00 a 7.00 horas. De estos tres períodos se obtienen los índices acústicos Ld, Le y Ln. Además, hay un cuarto índice acústico, el ponderado día-tarde-noche (Lden), que corresponde a una media ponderada de los índices Ld, Le y Ln, penalizando los períodos tarde y noche.|
|EN| Population data comes from the reading of the municipal register the corresponding year. The percentages shown are with respect the population of the neighbourhood, district or city, according to the corresponding resource. For noise evaluation there are three time periods defined by regulation. The day period is from 7 am to 9 pm, evening from 9 pm to 11 pm, and night from 11 pm to 7 am. From these three periods, the noise indicators Ld, Le and Ln are obtained. In addition, there is a fourth indicator, the weighted day-evening-night (Lden), which corresponds to a weighted average of the Ld, Le and Ln indicators, penalizing the evening and night periods.|


###  Estructura en format LONG (Vertical)

|Pos|Field/camp|Field description /Camp	Descripció|
|:--|:---------|:----------------------------------------------------------|
|01|Codi_Districte|Codi del districte / Código del distrito / District code|
|02|Nom_Districte|Nom del districte / Nombre del distrito / District name|
|03|Codi_Barri|Codi del barri / Código del barrio / Neighbourhood code|
|04|Nom_Barri|Nom del barri / Nombre del barrio / Neighbourhood name|
|05|Rang_soroll|Rang de soroll / Rango de ruido / Noise range|
|06|Concepte|Concepte/Concepto/Concept|
|07|Valor|Valor/Valor/Value|
  
  
### Estructura en format WIDE (Horizontal)

|Pos|Field/camp|Field description /Camp	Descripció|
|:--|:---------|:----------------------------------------------------------|
|01|Codi_Districte|Codi del districte / Código del distrito / District code|
|02|Nom_Districte|Nom del districte / Nombre del distrito / District name|
|03|Codi_Barri|Codi del barri / Código del barrio / Neighbourhood code|
|04|Nom_Barri|Nom del barri / Nombre del barrio / Neighbourhood name|
|05|Rang_soroll|Rang de soroll / Rango de ruido / Noise range|
|06|TOTAL_D|Soroll total en període dia / Ruido total en período día / Total noise in day period|
|07|TOTAL_E|Soroll total en període vespre / Ruido total en período tarde / Total noise in evening period|
|08|TOTAL_N|Soroll total en període nit / Ruido total en período noche / Total noise in night period|
|09|TOTAL_DEN|Soroll total en període Lden / Ruido total en período Lden / Total noise in Lden period|
|10|TRANSIT_D|Soroll de trànsit viari en període dia / Ruido de tráfico viario en período día / Road traffic noise in day period|
|11|TRANSIT_E|Soroll de trànsit viari en període vespre / Ruido de tráfico viario en período tarde / Road traffic noise in evening period|
|12|TRANSIT_N|Soroll de trànsit viari en període nit / Ruido de tráfico viario en período noche / Road traffic noise in night period|
|13|TRANSIT_DEN|Soroll de trànsit viari en període Lden / Ruido de tráfico viario en período Lden / Road traffic noise in Lden period|
|14|GI_TR_D|Soroll de grans infraestructures viàries en període dia / Ruido de grandes infraestructuras viarias en período día / Major road traffic noise in day period|
|15|GI_TR_E|Soroll de grans infraestructures viàries en període vespre / Ruido de grandes infraestructuras viarias en período tarde / Major road traffic noise in evening period|
|16|GI_TR_N|Soroll de grans infraestructures viàries en període nit / Ruido de grandes infraestructuras viarias en período noche / Major road traffic noise in night period|
|17|GI_TR_DEN|Soroll de grans infraestructures viàries en període Lden / Ruido de grandes infraestructuras viarias en período Lden / Major road traffic noise in Lden period|
|18|FFCC_D|Soroll d’eixos ferroviaris i tramvia en període dia / Ruido de ejes ferroviarios y tranvía en período día / Railway noise in day period|
|19|FFCC_E|Soroll d’eixos ferroviaris i tramvia en període vespre / Ruido de ejes ferroviarios y tranvía en período tarde / Railway noise in evening period|
|20|FFCC_N|Soroll d’eixos ferroviaris i tramvia en període nit / Ruido de ejes ferroviarios y tranvía en período noche / Railway noise in night period|
|21|FFCC_DEN|Soroll d’eixos ferroviaris i tramvia en període Lden / Ruido de ejes ferroviarios y tranvía en período Lden / Railway noise in Lden period|
|22|INDUST_D|Soroll d’indústria en període dia / Ruido de industria en período día / Industrial noise in day period|
|23|INDUST_E|Soroll d’indústria en període vespre / Ruido de industria en período tarde / Industrial noise in evening period|
|24|INDUST_N|Soroll d’indústria en període nit / Ruido de industria en período noche / Industrial noise in night period|
|25|INDUST_DEN|Soroll d’indústria en període Lden / Ruido de industria en período Lden / Industrial noise in Lden period|
|26|VIANANTS_D|Soroll en carrers de vianants en període dia / Ruido en calles peatonales en período día / Noise in pedestrian streets in day period|
|27|VIANANTS_E|Soroll en carrers de vianants en període vespre / Ruido en calles peatonales en período tarde / Noise in pedestrian streets in evening period|
|28|OCI_N|Soroll d’oci i aglomeració de persones en període nit / Ruido de ocio y aglomeración de personas en período noche / Recreational noise in night period|
|29|PATIS_D|Soroll en patis interiors d’illa en període dia / Ruido en patios interiores en período día / Noise in inner courtyards in day period|
|30|PATIS_E|Soroll en patis interiors d’illa en període vespre / Ruido en patios interiores en período tarde / Noise in inner courtyards in evening period|
|31|PARCS_D|Soroll en parcs en període dia / Ruido en parques en período día / Noise in parks in day period|

