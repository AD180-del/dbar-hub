# DBAR Organisational Hierarchy

This diagram visualizes the structural relationship between the Chinese Academy of Sciences (CAS), the regional International Centres of Excellence (ICoEs), and the thematic Working Groups (WGs) that form the 'Scientific Silk Road'.

```mermaid
graph TD
    subgraph Top_Level ["Top Level (Governance)"]
        CAS["Chinese Academy of Sciences (CAS)"]
    end

    subgraph Executive_Level ["Executive Level (Secretariat)"]
        CBAS["CBAS (Secretariat / Headquarters)"]
    end

    subgraph Thematic_Level ["Thematic Level (Working Groups)"]
        DATA["DBAR-DATA"]
        HiMAC["DBAR-HiMAC"]
        HERITAGE["DBAR-HERITAGE"]
        COAST["DBAR-COAST"]
        AGRI["DBAR-AGRI"]
        DISASTER["DBAR-DISASTER"]
        URBAN["DBAR-URBAN"]
        WATER["DBAR-WATER"]
        ENVI["DBAR-ENVI"]
    end

    subgraph Regional_Level ["Regional Level (ICoEs)"]
        ICoE_Helsinki["ICoE-Helsinki<br/>(Uni Helsinki / INAR, Finland)"]
        ICoE_Potenza["ICoE-Potenza<br/>(CNR, Italy)"]
        ICoE_Bangkok["ICoE-Bangkok<br/>(GISTDA, Thailand)"]
        ICoE_Peshawar["ICoE-Peshawar<br/>(Uni Peshawar, Pakistan)"]
        ICoE_Moscow["ICoE-Moscow<br/>(RAS, Russia)"]
        ICoE_ElJadida["ICoE-El Jadida<br/>(Chouaib Doukkali Uni, Morocco)"]
        ICoE_Lusaka["ICoE-Lusaka<br/>(Uni Zambia, Zambia)"]
        ICoE_Columbia["ICoE-Columbia / Sri Lanka<br/>(Uni Colombo, Sri Lanka)"]
    end

    %% Vertical Hierarchical Connections
    CAS --> CBAS
    CBAS --- DATA
    CBAS --- HiMAC
    CBAS --- HERITAGE
    CBAS --- COAST
    CBAS --- AGRI
    CBAS --- DISASTER
    CBAS --- URBAN
    CBAS --- WATER
    CBAS --- ENVI

    %% Mapping ICoEs to Primary Thematic Groups (Based on data/nodes.yaml)
    HiMAC -.-> ICoE_Helsinki
    HERITAGE -.-> ICoE_Potenza
    AGRI -.-> ICoE_Bangkok
    DISASTER -.-> ICoE_Peshawar
    ENVI -.-> ICoE_Moscow
    WATER -.-> ICoE_ElJadida
    AGRI -.-> ICoE_Lusaka
    COAST -.-> ICoE_Columbia
    WATER -.-> ICoE_Columbia

    %% Style styling
    style CAS fill:#f9f,stroke:#333,stroke-width:4px
    style CBAS fill:#bbf,stroke:#333,stroke-width:2px
```

---

## Technical Appendix: Organisational Mapping

| Level | Entity | Role / Description |
| :--- | :--- | :--- |
| **Top Level** | CAS | Strategic oversight and primary funding body. |
| **Executive** | CBAS | Administrative headquarters and data infrastructure provider. |
| **Thematic** | Working Groups | Define research agendas and data standards for specific domains. |
| **Regional** | ICoEs | Physical interfaces for localised implementation and data collection. |
