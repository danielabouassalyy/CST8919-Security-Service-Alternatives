

## 1. Azure Active Directory (SSO, IAM)

### Overview
- **Azure Active Directory (AAD)** – Microsoft’s cloud-based identity and access management service for SSO, MFA, role-based access control, and directory management.  
- **AWS IAM / AWS SSO** – IAM manages AWS user identities, access policies, and roles; AWS SSO provides single sign-on across AWS accounts and applications.  
- **Google Cloud Identity / IAM** – Cloud Identity handles identity management, MFA, and SSO; IAM controls access to GCP resources with fine-grained permissions.

### Comparison Table
| Feature | Azure Active Directory | AWS IAM / AWS SSO | Google Cloud Identity / IAM |
|---------|-----------------------|-------------------|-----------------------------|
| Core Features | SSO, MFA, RBAC, conditional access, directory sync | IAM for access control, SSO for centralized login | SSO, MFA, RBAC, directory services |
| Security & Compliance | ISO 27001, SOC, FedRAMP, GDPR, HIPAA | ISO 27001, SOC, FedRAMP, HIPAA | ISO 27001, SOC, FedRAMP, HIPAA |
| Pricing Model | Free tier + Premium P1/P2 per user | No cost for IAM; SSO pricing based on AWS usage | Free tier, premium features per user |
| Integration for DevSecOps | Works with Azure DevOps, GitHub, pipelines | Works with AWS CodePipeline, CodeBuild | Works with Cloud Build, CI/CD via APIs |

**Narrative Analysis:**  
AAD is powerful for centralized identity in Azure, with strong SSO and conditional access. AWS splits IAM for permissions and SSO for login, which works well but feels less unified. GCP’s solution is straightforward and ties tightly to Google services. If your stack is Azure-heavy, AAD is the most seamless; AWS’s approach is solid but split; GCP’s is simple and integrates naturally in Google environments.

---

## 2. Azure Monitor & Log Analytics

### Overview
- **Azure Monitor & Log Analytics** – Monitors infrastructure, apps, and network with centralized logging and advanced queries via Kusto Query Language (KQL).  
- **AWS CloudWatch / CloudTrail** – CloudWatch provides metrics, logs, and alerts; CloudTrail logs API calls and account activity for auditing.  
- **Google Cloud Monitoring / Logging** – Collects metrics, events, and logs from GCP services, with alerting and dashboards.

### Comparison Table
| Feature | Azure Monitor & Log Analytics | AWS CloudWatch / CloudTrail | GCP Monitoring / Logging |
|---------|------------------------------|-----------------------------|--------------------------|
| Core Features | Metrics, logs, alerts, KQL queries | Metrics, logs, alarms, API call logging | Metrics, logs, alerts |
| Security & Compliance | ISO 27001, SOC, FedRAMP, GDPR | ISO 27001, SOC, FedRAMP, GDPR | ISO 27001, SOC, FedRAMP, GDPR |
| Pricing Model | Pay for data ingestion, retention, and queries | Pay for metrics, logs storage, and retrieval | Pay for storage, retention, and queries |
| Integration for DevSecOps | Ties into Azure DevOps, pipelines, alerts | Works with AWS CI/CD, automation, alarms | Works with Cloud Build, automation, alert policies |

**Narrative Analysis:**  
Azure Monitor & Log Analytics shine when you need deep queries and strong integration with Azure services. AWS CloudWatch and CloudTrail together cover monitoring and auditing well but are separate services. GCP’s Monitoring and Logging keep it simple and unified. For Azure-based pipelines, Monitor fits perfectly; AWS’s combo is flexible; GCP’s tools are easy to adopt in their ecosystem.

---

## 3. Azure Policy

### Overview
- **Azure Policy** – Enforces rules and compliance across Azure resources, with auditing and automatic remediation options.  
- **AWS Config** – Tracks AWS resource configurations, evaluates compliance, and can remediate changes.  
- **GCP Organization Policy Service** – Sets and enforces rules for GCP resources at the org, folder, or project level.

### Comparison Table
| Feature | Azure Policy | AWS Config | GCP Org Policy Service |
|---------|--------------|------------|------------------------|
| Core Features | Policy enforcement, compliance reporting, remediation | Config tracking, compliance rules, remediation | Constraint-based policy enforcement |
| Security & Compliance | ISO 27001, SOC, FedRAMP | ISO 27001, SOC, FedRAMP | ISO 27001, SOC, FedRAMP |
| Pricing Model | Free for basic; pay for remediation triggers | Pay per config item and evaluation | No cost |
| Integration for DevSecOps | Works with Azure DevOps, ARM templates, pipelines | Works with CloudFormation, CodePipeline | Works with Deployment Manager, Cloud Build |

**Narrative Analysis:**  
Azure Policy is great for enforcing compliance with built-in templates and remediation. AWS Config offers similar control with strong integration into AWS infra tools. GCP’s service is simpler and constraint-based. If you want rich templates and automation, Azure Policy is strong; AWS Config is solid for AWS-native governance; GCP’s option is minimal but effective.

---

## 4. Defender for Cloud

### Overview
- **Defender for Cloud** – Monitors workloads for threats, vulnerabilities, and compliance, with security recommendations and integrations.  
- **AWS Security Hub** – Aggregates findings from AWS security services, checks compliance, and provides recommendations.  
- **GCP Security Command Center (SCC)** – Provides asset inventory, vulnerability scans, and threat detection across GCP.

### Comparison Table
| Feature | Defender for Cloud | AWS Security Hub | GCP SCC |
|---------|--------------------|------------------|---------|
| Core Features | Threat detection, vulnerability scans, compliance checks | Centralized security findings, compliance checks | Asset discovery, scans, threat detection |
| Security & Compliance | ISO 27001, SOC, FedRAMP, GDPR, HIPAA | ISO 27001, SOC, FedRAMP, HIPAA | ISO 27001, SOC, FedRAMP, HIPAA |
| Pricing Model | Free tier + pay per resource protected | Pay per finding ingested | Free tier + pay for premium threat intel |
| Integration for DevSecOps | Hooks into Azure pipelines, Defender APIs | Works with AWS CI/CD and security tools | Works with Cloud Build and API-based alerts |

**Narrative Analysis:**  
Defender for Cloud is strong for unified threat detection and compliance in Azure. AWS Security Hub centralizes findings but depends on other AWS tools for scans. GCP SCC is feature-rich for Google workloads. For Azure-heavy security, Defender is best; AWS Security Hub is flexible but modular; SCC is excellent for Google-native protection.

---

## 5. Azure Sentinel (SIEM/SOAR)

### Overview
- **Azure Sentinel** – Cloud-native SIEM and SOAR for collecting logs, detecting threats, and automating responses.  
- **AWS Security Lake / GuardDuty** – Security Lake centralizes security data; GuardDuty detects threats in AWS environments.  
- **Google Chronicle Security Operations** – SIEM/SOAR platform for threat detection, investigation, and response.

### Comparison Table
| Feature | Azure Sentinel | AWS Security Lake / GuardDuty | Google Chronicle Security Ops |
|---------|----------------|--------------------------------|--------------------------------|
| Core Features | SIEM, SOAR, log collection, playbooks | Security data lake + threat detection | SIEM, SOAR, investigation tools |
| Security & Compliance | ISO 27001, SOC, FedRAMP, GDPR | ISO 27001, SOC, FedRAMP | ISO 27001, SOC, FedRAMP |
| Pricing Model | Pay per GB ingested | Pay per GB stored and scanned | Pay per data usage |
| Integration for DevSecOps | Works with Azure Logic Apps, Sentinel API | Works with AWS analytics and SIEM partners | Works with Google APIs and automation |

**Narrative Analysis:**  
Sentinel is great for full SIEM/SOAR in the cloud, with automation through Logic Apps. AWS uses Security Lake for storage and GuardDuty for detection, making it more modular. Google Chronicle offers a strong investigative toolkit. If you want one tool for everything, Sentinel fits; AWS’s split approach is flexible; Chronicle is powerful for threat hunting.

---

## 6. Azure Firewall

### Overview
- **Azure Firewall** – Managed cloud firewall with stateful inspection, application rules, and threat intelligence integration.  
- **AWS Network Firewall** – Managed firewall for VPCs with stateful inspection and custom rules.  
- **GCP Cloud Firewall** – Network firewall for filtering traffic in GCP, with rule-based configurations.

### Comparison Table
| Feature | Azure Firewall | AWS Network Firewall | GCP Cloud Firewall |
|---------|----------------|----------------------|--------------------|
| Core Features | Stateful inspection, app rules, threat intel | Stateful inspection, rules, intrusion prevention | Layer 3/4/7 filtering |
| Security & Compliance | ISO 27001, SOC, FedRAMP | ISO 27001, SOC, FedRAMP | ISO 27001, SOC, FedRAMP |
| Pricing Model | Pay for deployment + data processed | Pay for endpoint hours + data processed | No extra cost for basic rules; premium features billed |
| Integration for DevSecOps | Works with Azure policies, pipelines | Works with AWS configs, automation | Works with GCP deployment tools |

**Narrative Analysis:**  
Azure Firewall is robust with built-in threat intel feeds. AWS Network Firewall offers similar features with tight VPC integration. GCP’s Cloud Firewall is simpler and often used with other GCP security tools. For enterprise-grade Azure networking, the Azure Firewall fits best; AWS Network Firewall is highly customizable; GCP’s option is lightweight and cost-efficient.

---

## 7. Azure DDoS Protection

### Overview
- **Azure DDoS Protection** – Protects Azure resources from volumetric and protocol-based DDoS attacks with real-time monitoring and mitigation.  
- **AWS Shield** – AWS’s managed DDoS protection service with two tiers: Standard and Advanced.  
- **GCP Cloud Armor** – Protects applications from DDoS and web attacks, with rules and IP allow/deny lists.

### Comparison Table
| Feature | Azure DDoS Protection | AWS Shield | GCP Cloud Armor |
|---------|----------------------|------------|-----------------|
| Core Features | DDoS mitigation, traffic monitoring, adaptive tuning | DDoS mitigation, network edge protection | DDoS protection, WAF, IP-based rules |
| Security & Compliance | ISO 27001, SOC, FedRAMP | ISO 27001, SOC, FedRAMP | ISO 27001, SOC, FedRAMP |
| Pricing Model | Basic included, Standard tier billed per protected resource | Standard free, Advanced billed monthly | Pay for rules and bandwidth |
| Integration for DevSecOps | Works with Azure Monitor, automation alerts | Works with AWS logging, automation | Works with GCP logging, Cloud Functions for automation |

**Narrative Analysis:**  
Azure DDoS Protection offers seamless coverage for Azure workloads with strong monitoring integration. AWS Shield provides layered defense with its Advanced tier adding more features. GCP Cloud Armor combines DDoS protection with a WAF for application-layer defense. For Azure-native defense, DDoS Protection fits perfectly; AWS Shield Advanced is strong for AWS-heavy apps; Cloud Armor is great for apps needing both DDoS and web attack protection.
