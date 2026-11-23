# CLF-C02 High-Yield Cheatsheet & Look-Alike Comparisons (2026 Edition)

> Use this reference during review blocks, mock error analysis, and Days 10–11 cram sessions. Every item is aligned with **CLF-C02 Exam Guide v1.3 (Oct 29, 2026)**.

---

## 1. Domain 1 Frameworks (5–10 Guaranteed Exam Questions)

### 6 Advantages of Cloud Computing
1. **Trade fixed expense (CapEx) for variable expense (OpEx)** — pay only as you consume.
2. **Benefit from massive economies of scale** — AWS aggregates global demand to lower prices.
3. **Stop guessing capacity** — scale up/down automatically instead of over-provisioning for peak.
4. **Increase speed and agility** — launch resources in minutes instead of weeks.
5. **Stop spending money running and maintaining data centers** — focus on customers, not racking/stacking.
6. **Go global in minutes** — deploy across worldwide AWS Regions with low latency.

### AWS Well-Architected Framework — 6 Pillars
*(Mnemonic: **O-S-R-P-C-S** — "**O**ur **S**ystems **R**un **P**erfectly, **C**ost **S**mart")*

| Pillar | Core Goal | Signature Exam Keywords / Design Principles |
| --- | --- | --- |
| **Operational Excellence** | Run & monitor systems; continuously improve processes | Operations as code (IaC), small reversible changes, refine procedures frequently, anticipate failure, learn from operational failures, managed services |
| **Security** | Protect data, systems, and assets | Strong identity foundation, least privilege, traceability (CloudTrail/Config), security at all layers, automate security best practices, protect data in transit & at rest, keep people away from data |
| **Reliability** | Recover from failures; meet demand consistently | Automatically recover from failure, test recovery procedures, scale horizontally, stop guessing capacity, manage change via automation |
| **Performance Efficiency** | Use computing resources efficiently as requirements evolve | Democratize advanced technologies (managed ML/DB), go global in minutes, use **serverless** architectures, experiment more often, mechanical sympathy (right tool for the job) |
| **Cost Optimization** | Deliver business value at lowest price point | Cloud Financial Management (CFM), adopt consumption model, measure overall efficiency, stop spending on undifferentiated heavy lifting, analyze & attribute expenditure (tags) |
| **Sustainability** | Minimize environmental impact of running cloud workloads | Understand impact, maximize utilization (rightsizing), adopt efficient hardware/managed services (e.g., Graviton), reduce downstream impact (less data moved/stored) |

### AWS Cloud Adoption Framework (AWS CAF) — 6 Perspectives
*(Mnemonic: **"Big Projects Go Pretty Smoothly Overall"**)*

| Group | Perspective | Core Focus (Exam Trigger) |
| --- | --- | --- |
| **Business Capabilities** | **Business** | IT aligns with business needs; strategy, product management, portfolio, business value |
| **Business Capabilities** | **People** | Culture, organizational change, workforce transformation, **training & cloud fluency** |
| **Business Capabilities** | **Governance** | Cloud financial management, program/project management, **risk management, data governance, benefits management** |
| **Technical Capabilities** | **Platform** | Enterprise-grade scalable hybrid cloud architecture, data/app architecture, CI/CD modernization |
| **Technical Capabilities** | **Security** | Confidentiality, integrity, availability; IAM, detection, infrastructure & data protection, incident response |
| **Technical Capabilities** | **Operations** | Day-to-day cloud service delivery at agreed SLAs: observability, AIOps, incident/problem/change management, **business continuity/DR** |

> **4 CAF Transformation Domains:** *Technology, Process, Organization, Product*.  
> **4 Business Value Outcomes:** *Reduced business risk, Improved ESG performance, Increased revenue, Increased operational efficiency*.

### 7 Rs of Cloud Migration
1. **Rehost** (*Lift and Shift*) — move apps as-is (fastest; e.g., AWS Application Migration Service / MGN).
2. **Relocate** (*Hypervisor-level lift and shift*) — move VMware workloads without buying hardware or rewriting apps.
3. **Replatform** (*Lift, tinker, and shift*) — small cloud optimizations without changing core architecture (e.g., self-managed DB → Amazon RDS).
4. **Repurchase** (*Drop and shop*) — switch to a different product, typically SaaS (e.g., CRM → Salesforce or AWS Marketplace SaaS).
5. **Refactor / Re-architect** — redesign app using cloud-native features (e.g., monolith → serverless Lambda + DynamoDB) — highest effort, highest agility.
6. **Retire** — decommission unneeded apps.
7. **Retain** (*Revisit*) — keep on-premises for now (compliance, latency, or not ready).

---

## 2. Domain 2: Shared Responsibility Model (Watch the Edge Cases!)

| Owner | Core Rule | Concrete Examples |
| --- | --- | --- |
| **AWS ("Security OF the Cloud")** | Global infrastructure, hardware, facilities, managed platform layer | Physical data center security, hardware disposal, virtualization/hypervisor layer, physical network, Region/AZ/Edge facilities, OS patching for **RDS / Lambda / DynamoDB / S3** |
| **Customer ("Security IN the Cloud")** | Customer data, IAM, client/server encryption choices, network/firewall configs, guest OS on IaaS | Customer data & classification, IAM users/roles/MFA, S3 bucket policies, **Security Group & NACL rules**, **EC2 Guest OS patching**, application code, deciding to enable encryption in transit/at rest |
| **Shared Controls** | *Processes* applied by both AWS (infrastructure layer) and Customer (OS/app/staff layer) | **Patch Management**, **Configuration Management**, **Awareness & Training** |

> **Service Shift Rule:** Moving from **EC2 (IaaS)** → **RDS (Managed)** → **S3 / DynamoDB / Lambda (Abstract/Serverless)** shifts **more** operational/OS/patching security responsibility onto **AWS**, while **Customer Data & IAM Access** ALWAYS remain the customer's responsibility.

---

## 3. Domain 4: 2026 AWS Support Plans (Verified Nov 2026)

| Plan | Min Cost | Technical Support Access | Fastest Response SLA | Key Differentiators (Exam Triggers) |
| --- | :---: | --- | --- | --- |
| **Basic** | **Free** | Account/billing & service quotas only (**no technical support**) | N/A | 24x7 account/billing support, forums, docs/whitepapers, AWS Health Dashboard, core Trusted Advisor checks |
| **AWS Business Support+** *(replaces legacy Developer & Business)* | **$29/mo** min per account | **GenAI real-time contextual support** + **24x7 phone, web, chat** to Cloud Support Engineers | **< 30 min** human engagement for business-critical system down | **500+ Trusted Advisor checks**, **AWS Support API** (automation), third-party software support, unlimited support cases |
| **AWS Enterprise Support** *(replaces legacy Enterprise On-Ramp too)* | **$5,000/mo** min *(reduced from $15k)* | All Business Support+ benefits + proactive guidance | **≤ 15 min** production-critical response | **Designated TAM (Technical Account Manager)**, **AWS Security Incident Response** included, strategic business reviews, **AWS Countdown** event management |
| **AWS Unified Operations** | Custom / Enterprise tier | Highest-touch consultative & operational engineering | Mission-critical / specialized | **Designated TAM + Domain Specialist Engineer (DSE)**, **Application Architecture Guidance**, **Infrastructure Event Management (IEM)**, **AWS Countdown Premium**, personalized runbooks & critical workload reviews |

> **Legacy Note (for free GitHub mocks only):** Legacy *Developer, Business, and Enterprise On-Ramp* are discontinued Jan 1, 2027 (remaining in GovCloud US only). If a legacy practice question asks *"lowest plan with TAM / 15-min SLA"*, the answer is **AWS Enterprise Support**. If it asks *"lowest plan with 24x7 phone/chat + Support API + full Trusted Advisor"*, the answer is **AWS Business Support+** (legacy: *Business*).

---

## 4. High-Yield Look-Alike Comparison Tables

### Security, Threat Detection & Governance
| Service | One-Line Exam Trigger | Don't Confuse With |
| --- | --- | --- |
| **Amazon GuardDuty** | **Intelligent threat detection** (ML) analyzing CloudTrail, VPC Flow Logs, DNS logs for malicious/unauthorized activity | *Inspector* (vulnerabilities), *Macie* (S3 PII) |
| **Amazon Inspector** | **Automated vulnerability management** scanning EC2, ECR container images, and Lambda for software CVEs & unintended network exposure | *GuardDuty* (active threat detection) |
| **Amazon Macie** | **ML-powered S3 sensitive data discovery** (finds PII, credit cards, credentials inside **Amazon S3** buckets) | *GuardDuty*, *Comprehend* |
| **AWS Shield** | **Managed DDoS protection** (Standard = free/automatic L3/L4; Advanced = paid + 24x7 SRT + DDoS cost protection) | *WAF* (L7 HTTP rules) |
| **AWS WAF** | **Layer 7 Web Application Firewall** blocking SQL injection, XSS, bad IPs/geo rules on CloudFront, ALB, API Gateway | *Shield* (DDoS), *Security Groups* (instance stateful firewall) |
| **AWS Firewall Manager** | **Centrally manage** WAF, Shield Advanced, Security Groups & Network Firewall rules **across AWS Organizations accounts** | *WAF* (single-account rules) |
| **AWS Security Hub** | **Central dashboard** aggregating security findings from GuardDuty, Inspector, Macie, Firewall Manager + automated compliance checks | *Detective* (root-cause investigation) |
| **Amazon Detective** | **Root-cause investigation** — visualizes graphs of security findings to figure out *how* an incident happened | *Security Hub* (aggregation) |
| **AWS Artifact** | **Self-service compliance reports** (SOC 1/2/3, ISO, PCI-DSS) & BAA/agreements download portal | *Trusted Advisor* (best-practice checks) |
| **AWS KMS vs. CloudHSM** | **KMS** = multi-tenant AWS-managed encryption keys; **CloudHSM** = **single-tenant dedicated** FIPS 140-2/3 Level 3 hardware security module (customer controls keys) | *Secrets Manager* (rotates DB passwords/API keys), *ACM* (SSL/TLS certs) |
| **IAM Identity Center vs. Cognito** | **IAM Identity Center** = **workforce SSO** (employees across multiple AWS accounts & business apps); **Cognito** = **customer/app user** sign-up/sign-in (mobile/web, Google/Apple/Facebook) | *IAM Users* (avoid for workforce SSO; use temporary creds/roles) |

### Monitoring, Auditing & Compliance
| Service | Exam Question It Answers |
| --- | --- |
| **Amazon CloudWatch** | *"What is happening to performance right now?"* — Metrics (CPU, memory), logs, dashboards, alarms, auto-scaling triggers |
| **AWS CloudTrail** | *"Who called which API, from what IP, and when?"* — Governance, compliance, and **API activity auditing** |
| **AWS Config** | *"How did a resource's configuration change over time, and is it compliant with rules?"* — Resource configuration history & compliance auditing |
| **AWS Trusted Advisor** | *"Am I following AWS best practices?"* — Checks across **Cost, Performance, Security, Fault Tolerance, Service Limits, Operational Excellence** |
| **AWS Health Dashboard** | *"Is AWS experiencing an outage, or is my specific EC2 instance scheduled for maintenance?"* — Public service status + personalized account health events |
| **AWS X-Ray** | *"Where is the latency bottleneck across my microservices?"* — Distributed request tracing |

### Networking & Global Delivery
| Pair | Service A | Service B |
| --- | --- | --- |
| **Security Group vs. NACL** | **Security Group:** Instance-level, **stateful** (return traffic auto-allowed), **Allow rules only** | **NACL:** Subnet-level, **stateless** (must allow inbound & outbound), **Allow & Deny rules** (evaluated by rule number) |
| **CloudFront vs. Global Accelerator** | **CloudFront:** **Caches** static/dynamic HTTP/HTTPS content at Edge Locations (CDN) | **Global Accelerator:** Improves **non-HTTP / TCP & UDP** performance via **2 static Anycast IPs** routing over AWS global backbone (no caching) |
| **Site-to-Site VPN vs. Direct Connect** | **VPN:** Encrypted tunnel over **public internet**, fast to set up, low cost, variable bandwidth | **Direct Connect:** **Dedicated private physical fiber** link, consistent high bandwidth/low latency, takes weeks/months, not encrypted by default |
| **VPC Peering vs. Transit Gateway** | **VPC Peering:** 1-to-1 private connection (non-transitive) | **Transit Gateway:** Central **hub-and-spoke** router connecting many VPCs + on-premises networks |
| **PrivateLink vs. NAT Gateway** | **PrivateLink:** Privately access AWS/partner services without traversing public internet | **NAT Gateway:** Lets **private subnet** instances make **outbound** internet calls while blocking inbound internet traffic |

### Compute & Deployment
| Service | Exam Trigger |
| --- | --- |
| **Amazon EC2** | Full OS control IaaS virtual servers |
| **AWS Lambda** | Event-driven **serverless functions** (pay per invocation/duration, zero server management, max 15m) |
| **AWS Fargate** | **Serverless compute engine for containers** (runs ECS/EKS containers without managing EC2 nodes) |
| **ECS vs. EKS vs. ECR** | **ECS** = AWS-native container orchestration; **EKS** = managed Kubernetes; **ECR** = container image registry |
| **AWS Batch** | Dynamically provisions compute to run large-scale **batch computing jobs** |
| **AWS Elastic Beanstalk** | **PaaS** — upload your web app code; AWS handles provisioning, LB, scaling, health monitoring (you still retain OS access if needed) |
| **Amazon Lightsail** | **Simple, predictable fixed monthly price** VPS/bundles for small websites, blogs, simple apps (lowest setup friction) |
| **AWS CloudFormation** | **Infrastructure as Code (IaC)** — repeatable JSON/YAML templates to provision entire AWS environments identically |
| **AWS Outposts** | **AWS-managed hardware racks installed in your on-premises data center** for ultra-low latency / local data residency |

### Storage & Databases
| Service | Category & Exam Trigger |
| --- | --- |
| **Amazon S3** | Unlimited **object storage** (11 9s durability), static website hosting, regional, pay per GB/requests/transfer |
| **S3 Storage Classes** | **Standard** (frequent) · **Intelligent-Tiering** (unknown/changing access patterns, auto-moves, small monitoring fee) · **Standard-IA / One Zone-IA** (infrequent, rapid retrieval, min 30d; One Zone = 1 AZ, cheaper, re-creatable data) · **Glacier Instant** (ms retrieval, archive) · **Glacier Flexible** (min–hours) · **Glacier Deep Archive** (lowest cost, 12–48h, 180d min) |
| **Amazon EBS vs. Instance Store** | **EBS:** Persistent network **block storage** attached to 1 EC2 in same AZ (survives stop/start); **Instance Store:** Ephemeral high-speed local NVMe (**lost on stop/terminate**) |
| **Amazon EFS vs. Amazon FSx** | **EFS:** Serverless, elastic **Linux NFS** shared file system across **multiple AZs**; **FSx:** Managed **Windows File Server (SMB)**, Lustre (HPC), NetApp ONTAP, OpenZFS |
| **AWS Storage Gateway** | **Hybrid** bridge connecting on-premises apps to AWS cloud storage (File, Volume, Tape gateways) |
| **RDS vs. Aurora vs. DynamoDB** | **RDS:** Managed SQL (MySQL, Postgres, Oracle, SQL Server, MariaDB — Multi-AZ = HA failover, Read Replicas = read scaling); **Aurora:** AWS cloud-native MySQL/Postgres (up to 5x/3x faster, auto-scales to 128TB, 6 copies across 3 AZs); **DynamoDB:** Serverless **NoSQL key-value/document**, single-digit ms latency at any scale |
| **Redshift vs. Athena vs. EMR** | **Redshift:** Petabyte **data warehouse (OLAP)**; **Athena:** **Serverless SQL queries directly on S3** (pay per TB scanned); **EMR:** Managed **Hadoop / Spark** big data clusters |
| **ElastiCache / Neptune / DocumentDB** | **ElastiCache:** In-memory sub-ms caching (Redis/Valkey/Memcached); **Neptune:** Managed **Graph DB** (social networks, fraud); **DocumentDB:** MongoDB-compatible JSON document DB |

### Billing, Pricing & Cost Management
| Tool / Option | Exam Trigger |
| --- | --- |
| **AWS Pricing Calculator** | **Estimate costs BEFORE** launching a new workload |
| **AWS Budgets** | **Set custom cost/usage thresholds & alerts** (email/SNS) for actual or forecasted spend |
| **AWS Cost Explorer** | **Visualize & analyze past spend + forecast up to 12 months** ahead |
| **AWS Cost & Usage Report (CUR)** | **Most granular, comprehensive** line-item billing CSV/Parquet files delivered to S3 |
| **AWS Compute Optimizer** | **ML-driven rightsizing recommendations** for EC2, EBS, Lambda, ECS Fargate |
| **AWS Organizations** | Multi-account **consolidated billing** (volume discount pooling + RI/Savings Plan sharing across accounts) + **SCPs** (guardrails) |
| **EC2 Pricing Models** | **On-Demand:** Short-term/unpredictable, no commitment · **Savings Plans:** Commit to **$/hour** for 1 or 3 yrs (Compute SP = flexible across EC2 family/Region/Fargate/Lambda; up to 66–72% off) · **Reserved Instances (RI):** Commit to instance attributes 1 or 3 yrs (Standard = max discount; Convertible = change family/OS) · **Spot:** Interruptible/fault-tolerant, up to 90% off, 2-min notice · **Dedicated Hosts:** Physical server dedicated to you (**BYOL per-socket/per-core compliance**) · **Dedicated Instances:** Hardware isolation, no host visibility |
| **Data Transfer Rule** | Data **IN** from internet = **FREE**; Data **OUT** to internet or **across Regions** = **CHARGED** |

### AI/ML, Analytics, Integration & End-User Computing (2026 In-Scope)
| Service | 5-Word Exam Trigger |
| --- | --- |
| **Amazon SageMaker AI** | Build, train, deploy custom ML models |
| **Amazon Q** | Generative AI assistant for business & devs |
| **Amazon Rekognition** | Image & video analysis (faces, labels, moderation) |
| **Amazon Comprehend** | NLP text sentiment & entity extraction |
| **Amazon Textract** | Extract text, tables, forms from scanned PDFs/docs |
| **Amazon Transcribe / Polly / Translate** | **Transcribe** = Speech→Text · **Polly** = Text→Lifelike Speech · **Translate** = Language translation |
| **Amazon Lex / Amazon Connect** | **Lex** = Conversational AI chatbots · **Connect** = Cloud contact/call center |
| **Amazon Quick** *(formerly QuickSight)* | Serverless BI dashboards & visualizations |
| **AWS Glue / Amazon Kinesis** | **Glue** = Serverless **ETL** data catalog/prep · **Kinesis** = **Real-time streaming** data ingestion |
| **SQS vs. SNS vs. EventBridge vs. Step Functions** | **SQS** = Decoupling message **queue** (pull) · **SNS** = **Pub/sub** fan-out notifications (push) · **EventBridge** = Serverless **event bus** routing SaaS/AWS events · **Step Functions** = Visual **workflow orchestration** |
| **WorkSpaces vs. AppStream 2.0 vs. WorkSpaces Secure Browser** | **WorkSpaces** = Full cloud virtual desktop (VDI) · **AppStream 2.0** = Stream **specific desktop apps** to browser · **WorkSpaces Secure Browser** = Managed **secure web browser** for internal web apps |
| **AWS DMS + AWS SCT** | **DMS** = Migrate databases with minimal downtime · **SCT** = Convert database schema between **different** engines (heterogeneous, e.g., Oracle → Aurora Postgres) |
| **AWS Amplify / AWS IoT Core / Amazon SES** | **Amplify** = Frontend web/mobile apps · **IoT Core** = Connect billions of IoT devices · **SES** = High-volume transactional/marketing email |

---

## 5. Exam-Day Keyword Decoder (Fast Elimination)

| Phrase in Question Stem | Immediately Look For |
| --- | --- |
| *"Least operational overhead"* / *"without managing servers"* | **Serverless / Managed** (Lambda, Fargate, DynamoDB, Aurora, S3, Athena) |
| *"Highest availability within a Region"* / *"no single point of failure"* | **Multi-AZ** + **ELB** + **Auto Scaling** |
| *"Global low latency for static files / video"* | **Amazon CloudFront** (Edge Locations) |
| *"Audit who deleted / modified a resource"* | **AWS CloudTrail** |
| *"Track configuration changes / resource compliance history"* | **AWS Config** |
| *"Compliance reports (SOC, ISO, PCI, BAA)"* | **AWS Artifact** |
| *"Unknown or changing S3 access patterns"* | **S3 Intelligent-Tiering** |
| *"Lowest cost archival, 12+ hour retrieval OK"* | **S3 Glacier Deep Archive** |
| *"BYOL per-core / per-socket licensing"* | **EC2 Dedicated Hosts** |
| *"Report suspected abuse / unauthorized penetration from AWS IP"* | **AWS Trust and Safety team** *(legacy: AWS Abuse team)* |
| *"24x7 phone/chat + Support API + 500+ Trusted Advisor checks (lowest cost)"* | **AWS Business Support+** |
| *"Designated TAM + ≤15-min SLA + Security Incident Response"* | **AWS Enterprise Support** |
| *"Third-party software / vendor firewall / SaaS trial"* | **AWS Marketplace** |
| *"Expert help migrating / hands-on consulting"* | **AWS Professional Services** or **AWS Partner Network (APN)** |
