## 🧠 Diagrama DER — AI Finance Incidents

Este diagrama representa a modelagem de dados para o registro e análise de incidentes relacionados ao uso de Inteligência Artificial no setor financeiro.

### 📌 Entidades

- **INCIDENTE**: representa um evento relacionado a falhas, riscos ou problemas envolvendo sistemas de IA.
- **ORGANIZACAO**: entidade que sofreu ou foi impactada por um incidente.
- **CLASSIFICACAO**: detalha a categorização técnica do incidente (tipo de falha, domínio de IA, origem dos dados).

### 🔗 Relacionamentos

- **ORGANIZACAO → INCIDENTE (1:N)**  
  Uma organização pode sofrer vários incidentes, mas cada incidente está associado a uma única organização.

- **INCIDENTE → CLASSIFICACAO (1:N)**  
  Um incidente pode possuir múltiplas classificações, permitindo análise mais granular.


### 💡 Objetivo

Esse modelo facilita:
- Análise de riscos em sistemas de IA
- Auditoria e rastreabilidade de incidentes
- Classificação estruturada para estudos e relatórios

---

```mermaid
%%{init: {
  "theme": "base",
  "themeVariables": {
    "primaryColor": "#0d1117",
    "primaryTextColor": "#ffffff",
    "primaryBorderColor": "#00b4d8",
    "lineColor": "#00b4d8",
    "background": "#0d1117"
  },
  "themeCSS": "
    .er.relationshipLine path { stroke: #00b4d8 !important; }
    .er.entityBox { stroke: #00b4d8 !important; fill: #0d1117 !important; }
    .er.attributeBoxOdd { fill: #0d1117 !important; }
    .er.attributeBoxEven { fill: #0d1117 !important; }
    .er.entityLabel { fill: #ffffff !important; }
  "
}}%%

erDiagram
    INCIDENTE {
        int incident_id PK
        date data_incidente
        string titulo
        string descricao
        string tipo_risco
        string severidade
    }

    ORGANIZACAO {
        int org_id PK
        string nome_org
        string pais
        string setor
    }

    CLASSIFICACAO {
        int class_id PK
        int incident_id FK
        string dominio_ai
        string tipo_falha
        string origem_dado
    }

    INCIDENTE ||--o{ CLASSIFICACAO : possui
    ORGANIZACAO ||--o{ INCIDENTE : sofre
```


