# Broadband-Usage-Statements
Connected Home Usage Statement Platform collects home gateway usage telemetry, ingests it through Azure Event Hubs into PostgreSQL, and turns it into monthly customer usage insights and email statements.
<img width="940" height="202" alt="image" src="https://github.com/user-attachments/assets/337af250-26ce-4b8a-84a2-fb366b166b4a" />

1. **Source And Stream:** Home gateway collects usage data from connected devices. Telemetry is sent to Azure Event Hubs for ingestion through the operators telemetry service. 

2. **Process:** Python worker validates, deduplicates, and stores the records in PostgreSQL.  

3. **Aggregate:** Daily and monthly usage is calculated and saved for reporting. 

4. **Serve:** Monthly data is sent to the customer through email and the Navigate app API.
