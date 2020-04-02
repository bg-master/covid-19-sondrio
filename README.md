# COVID-19 Monitoraggio dati provincia di Sondrio - aggiornamento quotidiano 

[![GitHub license](https://img.shields.io/badge/License-Creative%20Commons%20Attribution%204.0%20International-blue)](LICENSE)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md) 

Questo repository raccoglie i dati comunicati quotidianamente dalla **Agenzia
di Tutela della Salute della Montagna** sulla diffusione dell'infezione da
Coronavirus (COVID-19) nei comuni della provincia di Sondrio.<br>
Il repository verrà aggiornato quotidianamente fino a quando **ATS Montagna**
continuerà a comunicare i dati.  

## Dataset
- dati-comuni (csv)
- dati-provincia (csv)

## Formato dei dati

### Dati per Comune - file giornaliero

**Directory:**  dati-comuni<br>
**Nome file:** covid19-ita-sondrio-comuni-yyyymmdd.csv (covid19-ita-sondrio-comuni-20200316.csv)<br>
**Nome ultimo file:** covid19-ita-sondrio-comuni-latest.csv<br>

| Nome campo                  | Descrizione                                  | Formato                             | Esempio                  |
| --- | --- | --- | --- |
| **data**                    | Data dell’informazione                       | YYYY-MM-DDTHH:MM:SS+HHMM (ISO 8601) | 2020-03-16T19:00:00+0100 |
| **stato**                   | Stato di riferimento                         | XYZ (ISO 3166-1 alpha-3)            | ITA                      |
| **codice_regione**          | Codice della Regione (ISTAT 2019)            | Testo (2)                           | 03                       |
| **denominazione_regione**   | Denominazione della Regione                  | Testo                               | Lombardia                |
| **codice_provincia**        | Codice della Provincia (ISTAT 2019)          | Testo (3)                           | 014                      |
| **denominazione_provincia** | Denominazione della Provincia                | Testo                               | Sondrio                  |
| **sigla_provincia**         | Sigla della Provincia                        | Testo (2)                           | SO                       |
| **codice_comune**           | Codice del Comune (ISTAT 2019)               | Testo (6)                           | 014001                   |
| **denominazione_comune**    | Denominazione del Comune                     | Testo                               | Sondrio                  |
| **abitanti**                | Numero di abitanti (Popolazione legale 2011) | Numero (int >= 0)                   | 1000                     |
| **totale_casi**             | Totale casi positivi                         | Numero (int >= 0)                   | 5                        |

**Esempio**
```
data,stato,codice_regione,denominazione_regione,codice_provincia,denominazione_provincia,sigla_provincia,codice_comune,denominazione_comune,abitanti,totale_casi
2020-03-16T19:00:00+0100,ITA,03,Lombardia,014,Sondrio,SO,014001,Albaredo per San Marco,349,0
```

### Dati per Comune - file complessivo

**Directory:**  dati-comuni<br>
**Nome file:** covid19-ita-sondrio-comuni.csv<br>

| Nome campo                  | Descrizione                                                                       | Formato                             | Esempio                  |
| --- | --- | --- | --- |
| **data**                    | Data dell’informazione                                                            | YYYY-MM-DDTHH:MM:SS+HHMM (ISO 8601) | 2020-03-16T19:00:00+0100 |
| **stato**                   | Stato di riferimento                                                              | XYZ (ISO 3166-1 alpha-3)            | ITA                      |
| **codice_regione**          | Codice della Regione (ISTAT 2019)                                                 | Testo (2)                           | 03                       |
| **denominazione_regione**   | Denominazione della Regione                                                       | Testo                               | Lombardia                |
| **codice_provincia**        | Codice della Provincia (ISTAT 2019)                                               | Testo (3)                           | 014                      |
| **denominazione_provincia** | Denominazione della Provincia                                                     | Testo                               | Sondrio                  |
| **sigla_provincia**         | Sigla della Provincia                                                             | Testo (2)                           | SO                       |
| **codice_comune**           | Codice del Comune (ISTAT 2019)                                                    | Testo (6)                           | 014001                   |
| **denominazione_comune**    | Denominazione del Comune                                                          | Testo                               | Sondrio                  |
| **abitanti**                | Numero di abitanti (Popolazione legale 2011)                                      | Numero (int >= 0)                   | 1000                     |
| **nuovi_casi**              | Nuovi casi positivi (totale_casi giorno corrente - totale_casi giorno precedente) | Numero (int >= 0)                   | 5                        |
| **totale_casi**             | Totale casi positivi                                                              | Numero (int >= 0)                   | 5                        |

**Esempio**
```
data,stato,codice_regione,denominazione_regione,codice_provincia,denominazione_provincia,sigla_provincia,codice_comune,denominazione_comune,abitanti,nuovi_casi,totale_casi
2020-03-16T19:00:00+0100,ITA,03,Lombardia,014,Sondrio,SO,014001,Albaredo per San Marco,349,0,0
```

### Dati per Provincia - file complessivo

**Directory:**  dati-provincia<br>
**Nome file:** covid19-ita-sondrio.csv<br>

| Nome campo                  | Descrizione                                                                                  | Formato                             | Esempio                  |
| --- | --- | --- | --- |
| **data**                    | Data dell’informazione                                                                       | YYYY-MM-DDTHH:MM:SS+HHMM (ISO 8601) | 2020-03-16T19:00:00+0100 |
| **stato**                   | Stato di riferimento                                                                         | XYZ (ISO 3166-1 alpha-3)            | ITA                      |
| **codice_regione**          | Codice della Regione (ISTAT 2019)                                                            | Testo (2)                           | 03                       |
| **denominazione_regione**   | Denominazione della Regione                                                                  | Testo                               | Lombardia                |
| **codice_provincia**        | Codice della Provincia (ISTAT 2019)                                                          | Testo (3)                           | 014                      |
| **denominazione_provincia** | Denominazione della Provincia                                                                | Testo                               | Sondrio                  |
| **sigla_provincia**         | Sigla della Provincia                                                                        | Testo (2)                           | SO                       |
| **nuovi_deceduti**          | Nuove persone decedute (totale_deceduti giorno corrente - totale_deceduti giorno precedente) | Numero (int >= 0)                   | 10                       |
| **totale_deceduti**         | Totale delle persone decedute                                                                | Numero (int >= 0)                   | 10                       |
| **nuovi_casi**              | Nuovi casi positivi (totale_casi giorno corrente - totale_casi giorno precedente)            | Numero (int >= 0)                   | 5                        |
| **totale_casi**             | Totale casi positivi                                                                         | Numero (int >= 0)                   | 5                        |

**Esempio**
```
data,stato,codice_regione,denominazione_regione,codice_provincia,denominazione_provincia,sigla_provincia,nuovi_deceduti,totale_deceduti,nuovi_casi,totale_casi
2020-03-16T19:00:00+0100,ITA,03,Lombardia,014,Sondrio,SO,0,2,54,104
```

## Fonte
- [ATS Montagna](https://www.ats-montagna.it)