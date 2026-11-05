  ```mermaid
  flowchart LR
    NVD[NVD] --> C[Collectors]
    AB[abuse.ch] --> C
    C --> L[(Iceberg auf S3)]
    L --> T[Trino]
    C --> P[(PostgreSQL)] --> A[API]
    C --> O[(OpenSearch)]
  ```
