# Climate-data-analysis-using-machine-learning

## Cel projektu
Celem projektu jest analiza długookresowych zmian średniej rocznej temperatury oraz identyfikacja punktu zmiany strukturalnej w szeregu czasowym.

Po wykryciu zmiany seria została podzielona na dwa segmenty:
- okres przed punktem zmiany,
- okres po punkcie zmiany.

Dla obu segmentów zbudowano niezależne modele prognozujące temperaturę do roku 2033 z wykorzystaniem architektury N-BEATS. Następnie porównano jakość prognoz w obu okresach.


## Dane
Dane temperaturowe pochodzą z **Copernicus Climate Data Store**.
Wykorzystany został zbiór *E-OBS daily gridded meteorological data for Europe from 1950 to present, oparty na obserwacjach in-situ*.

W analizie wykorzystano zmienną:
- *tg* - średnia temperatura dzienna

Źródło:
(https://cds.climate.copernicus.eu/datasets/insitu-gridded-observations-europe?tab=overview)  

  
W celu ograniczenia analizy do obszaru Europy wykorzystano dane przestrzenne z bazy **Natural Earth Data**. Dane te posłużyły do przycięcia zbioru do granic Europy.  


Źródło:
(https://www.naturalearthdata.com/downloads/50m-cultural-vectors/)    



## Etapy przetwarzania i modelowania
1. Przygotowanie danych 

2. Wykrywanie punktu zmiany przy użyciu algorytmu PELT.

3. Podział danych - rozdzielenie szeregu na dwa segmenty: przed i po punkcie zmiany.

4. Przygotowanie do modelowania 

5. Modelowanie – budowa dwóch niezależnych modeli N-BEATS.

6. Ewaluacja – ocena jakości prognoz przy użyciu miar MAE, RMSE i MAPE.

7. Prognozowanie – ekstrapolacja temperatury do roku 2033.

## Podsumowanie
W analizie zidentyfikowano zmianę strukturalną w szeregu czasowym temperatury. Zastosowanie osobnych modeli dla wyodrębnionych segmentów pozwoliło lepiej uchwycić dynamikę zmian. Prognozy wskazują na utrzymujący się trend wzrostowy temperatury, a różnice w jakości dopasowania pomiędzy segmentami sugerują zmianę charakteru badanego procesu w czasie.
