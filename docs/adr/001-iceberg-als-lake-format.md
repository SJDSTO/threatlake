# ADR-001: Apache Iceberg als Tabellenformat für den Data Lake

Status: angenommen
Datum: 2026-11-05

## Kontext
Rohdaten aus vier Quellen sollen vollständig und versioniert aufbewahrt
und mit SQL ausgewertet werden. PostgreSQL bleibt für schnelle API-Abfragen.

## Entscheidung
Rohdaten und bereinigte Tabellen liegen als Iceberg-Tabellen auf
S3-kompatiblem Speicher; Abfragen laufen über Trino.

## Betrachtete Alternativen
- Alles in PostgreSQL: einfach, aber keine günstige Historie, kein Time Travel.
- Reine Parquet-Dateien: billig, aber ohne Transaktionen und Schema-Evolution.
- Delta Lake: ähnlich mächtig, aber engere Bindung an das Spark-Ökosystem.

## Konsequenzen
+ Time Travel, Schema-Evolution, mehrere Engines auf denselben Daten
- Zusätzliche Dienste (Katalog, Objektspeicher, Trino) und mehr RAM
