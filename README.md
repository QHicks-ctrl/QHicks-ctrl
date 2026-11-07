# Corporate Sales & Finance Data Pipeline Architecture

## 📋 Project Overview
Designed and deployed a local relational database architecture to simulate an enterprise-grade corporate data warehouse. This end-to-end business intelligence pipeline transforms raw transactional rows into an interactive executive dashboard, pairing granular consumer sales volumes with wholesale manufacturing costs and overhead side-by-side to deliver real-time margin visibility.

> 🔒 **Security Notice:** All underlying production SQL source code, relational data schemas, and flat-file assets are maintained securely within a private, restricted enterprise repository to preserve data integrity and infrastructure privacy.

---

## 🏛️ Engineered Architecture Lifecycle

## 🛡️ Infrastructure Stress Test & GRC Compensating Controls
During deployment, the local business intelligence integration was blocked by a hard-stop authentication loop caused by strict native SSL encryption policies and unverified cryptographic root certificates on the local server.

To restore operational velocity without compromising data integrity, I independently troubleshooted the system over a **rigorous 7-hour infrastructure sprint**:
* **Protocol Re-Routing:** Bypassed default unencrypted Windows Named Pipes protocol constraints by forcing a direct TCP/IP network route through the root port configuration (`localhost\SQLEXPRESS`).
* **Cryptographic Exception Management:** Executed an authorized GRC change management override by enabling a **'Trust Server Certificate'** policy bypass. Because data traffic was completely confined within the local loopback network adapter boundary, this compensating control stabilized the connection pipeline while keeping all data traffic encrypted.

---
## 🧹 Data Transformation & Relational Modeling (ETL)
* **Metadata Remediation:** Extracted SQL data grids via flat CSV files. Upon importing into Power BI Desktop, launched **Power Query Editor** to scrub corrupted system-generated transformation histories and re-mapped compressed metadata columns to strongly typed schema categories (`product_name`, `quantity_sold`, `cost_of_goods_sold`).
* **Star-Schema Architecture:** Navigated to **Model View** to establish a relational **Many-to-One (`*:1`) relationship** using the `product_name` column as a universal data bridge.
* **Executive Visualization:** Deployed an interactive **Clustered Column Chart** on the canvas, dynamically pairing transactional volume against wholesale production costs to empower stakeholders with immediate variance visibility.

---
## 🛠️ Technical Skillset Demonstrated
* **Database Management:** Microsoft SQL Server, SQL Server Management Studio (SSMS), Relational Schema Design.
* **Data Pipelines:** ETL (Extract, Transform, Load), Flat File Extractions, Power Query Editor.
* **Business Intelligence:** Power BI Desktop, Star-Schema Modeling, Data Visualization (Clustered Column Charts).
