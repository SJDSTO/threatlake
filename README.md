# threatlake

Threat-Intelligence-Datenplattform: sammelt Schwachstellen- und Bedrohungsdaten aus öffentlichen Quellen (NVD, CISA KEV, EPSS, abuse.ch ThreatFox), speichert sie geprüft und ohne Duplikate in PostgreSQL und einem Data Lake auf Apache Iceberg und macht sie per API und Suche abfragbar.

> Status: im Aufbau. Fortschritt siehe [Issues](https://github.com/SJDSTO/threatlake/issues).

## Architektur

- Überblick und Datenfluss: [docs/architecture.md](docs/architecture.md)
- Architekturentscheidungen (ADRs): [docs/adr/](docs/adr/)

## Schnellstart

Folgt mit Phase 1 (`make up && make ingest`).

## Datenquellen und Nutzungsbedingungen

| Quelle | Inhalt | Nutzungsbedingungen |
|---|---|---|
| NVD | CVE-Schwachstellen | folgt |
| CISA KEV | aktiv ausgenutzte Schwachstellen | folgt |
| EPSS | Ausnutzungswahrscheinlichkeit je CVE | folgt |
| abuse.ch ThreatFox | Indicators of Compromise (IOCs) | folgt |

## Roadmap

Phasen und Aufgaben stehen als Issues mit den Labels `phase-0` bis `phase-7` im Repo.

## Lizenz

Apache-2.0, siehe [LICENSE](LICENSE).
