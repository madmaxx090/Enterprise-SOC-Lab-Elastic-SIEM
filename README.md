# Enterprise-SOC-Lab-Elastic-SIEM
Enterprise SOC Lab using Elastic SIEM, Sysmon, Fleet Server, Detection Engineering, Threat Hunting, and MITRE ATT&amp;CK Mapping.
```mermaid
graph LR
    %% Direction: Left to Right works beautifully for banners
    
    %% Nodes & Labels
    subgraph Attack_Simulation [Attack Phase]
        A[Kali Linux]
    end

    subgraph Defense_Ingestion [Telemetry & Ingestion]
        B(Windows Endpoint)
        C{Elastic Agent / Sysmon}
    end

    subgraph Centralized_SIEM [Analysis & Response]
        D[(Elasticsearch DB)]
        E[Kibana SIEM]
        F[SOC Analyst]
    end

    %% Flow/Connections
    A -->|RDP Brute Force / Malware| B
    B -->|Local Logs| C
    C -->|Secure Beats TLS| D
    D -->|Query & Visualization| E
    E -->|Alert Triage & Hunting| F

    %% Node Styles (Professional Cyber Theme)
    style A fill:#4A154B,stroke:#333,stroke-width:1.5px,color:#fff
    style B fill:#1F4E79,stroke:#333,stroke-width:1.5px,color:#fff
    style C fill:#005F73,stroke:#333,stroke-width:1.5px,color:#fff
    style D fill:#EE9B00,stroke:#333,stroke-width:1.5px,color:#fff
    style E fill:#0A9396,stroke:#333,stroke-width:1.5px,color:#fff
    style F fill:#9B2226,stroke:#333,stroke-width:2px,color:#fff

    %% Subgraph Styles (Subtle Backgrounds)
    classDef default font-family:sans-serif,font-weight:bold;
    style Attack_Simulation fill:none,stroke:#d9534f,stroke-dasharray: 5 5,color:#d9534f
    style Defense_Ingestion fill:none,stroke:#5bc0de,stroke-dasharray: 5 5,color:#5bc0de
    style Centralized_SIEM fill:none,stroke:#5cb85c,stroke-dasharray: 5 5,color:#5cb85c
