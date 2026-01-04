```mermaid
flowchart TD

    A[1. Normal JOIN<br>Raw table + Raw table] --> B[2. Aggregated JOIN<br>Summary + Summary]

    B --> C[3. Normal + Summary JOIN<br>Detail + Summary]

    C --> D[4. Subquery Summary<br>JOIN (SELECT ... GROUP BY ...)]

    D --> E[5. CTE Summary<br>WITH cte AS (SELECT ... GROUP BY ...)]

    E --> F[6. JOIN + CTE<br>Detail + cte_continent]

    style A fill:#d9e8ff,stroke:#1a4fb3,stroke-width:2px
    style B fill:#d9ffe8,stroke:#1a8f4f,stroke-width:2px
    style C fill:#fff4d9,stroke:#b38f1a,stroke-width:2px
    style D fill:#ffe0e0,stroke:#b31a1a,stroke-width:2px
    style E fill:#f0d9ff,stroke:#6b1ab3,stroke-width:2px
    style F fill:#e8e8e8,stroke:#333,stroke-width:2px
```
