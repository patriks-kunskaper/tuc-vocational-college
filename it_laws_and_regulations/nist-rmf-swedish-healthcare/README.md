# NIST RMF Implementation for Swedish Healthcare
**Risk Analysis and Security Governance Framework**

![Status](https://img.shields.io/badge/status-portfolio%20project-blue)
![Framework](https://img.shields.io/badge/framework-NIST%20RMF-green)
![Jurisdiction](https://img.shields.io/badge/jurisdiction-Sweden-yellow)
![Language](https://img.shields.io/badge/language-Swedish-red)

## 📋 Overview

This project demonstrates a **practical adaptation of NIST Risk Management Framework (RMF)** to Swedish healthcare cybersecurity requirements, integrating Swedish legislation (Cybersäkerhetslagen, GDPR, Patientdatalagen) with international best practices.

**Key Achievement**: Successfully bridged US federal cybersecurity framework with Swedish legal requirements, creating a legally compliant and technically sound security governance model for healthcare providers.

---

## 🎯 Project Scope

**Fictional Organization**: Stockholm Läkarhus AB  
**Sector**: Primary Healthcare (Private Provider)  
**Size**: Medium enterprise (125 employees, 60,000 patients, 75M SEK revenue)  
**Classification**: Important Entity (*Viktig enhet*) under Swedish Cybersecurity Act

**Critical System**: Electronic Health Record (EHR/Journalsystem)  
**Information Classification**: K3-R3-T3 (Confidentiality-Integrity-Availability)

---

## 🏗️ Framework Structure

The implementation follows NIST RMF's 7-step methodology:

1. **PREPARE** - Risk management strategy and organizational context
2. **CATEGORIZE** - Information and system classification (K-R-T model)
3. **SELECT** - Security controls based on legal requirements and risk
4. **IMPLEMENT** - Technical and organizational security measures
5. **ASSESS** - Threat analysis and vulnerability identification
6. **AUTHORIZE** - Executive risk acceptance and authorization decision
7. **MONITOR** - Continuous monitoring and incident response

---

## ⚖️ Legal Framework Integration

### Swedish Legislation Applied

| Law | Key Requirements | Application |
|-----|-----------------|-------------|
| **Cybersäkerhetslagen (SFS 2025:1506)** | Risk analysis, incident reporting, security measures | System categorization, incident response timelines |
| **GDPR (EU 2016/679)** | Technical safeguards (Art. 32), breach notification (Art. 33) | Encryption, access controls, 72h reporting to IMY |
| **Patientdatalagen (SFS 2008:355)** | Access restrictions (4 kap. 2§), audit logging (4 kap. 3§) | RBAC implementation, log monitoring |
| **Patientsäkerhetslagen (SFS 2010:659)** | Patient safety requirements (6 kap. 1§) | Data integrity controls |

### Regulatory Authorities

- **MCF (Myndigheten för civilt försvar)** - CSIRT incident reporting
- **IMY (Integritetsskyddsmyndigheten)** - GDPR compliance supervision
- **IVO (Inspektionen för vård och omsorg)** - Healthcare oversight

---

## 🔐 Security Controls Implemented

### Technical Controls
- **Authentication**: Multi-Factor Authentication (BankID + password)
- **Encryption**: AES-256 database encryption, TLS 1.3 transport security
- **Access Control**: Role-Based Access Control (RBAC) with least privilege
- **Logging**: Comprehensive audit trail with monthly reviews
- **Backup**: Daily incremental + weekly full backup with quarterly testing

### Organizational Controls
- Security awareness training (phishing, password hygiene)
- Quarterly access reviews and management reporting
- Annual incident response exercises
- Documented incident response procedures

---

## 📊 Risk Assessment Methodology

**Risk Formula**: `RISK = LIKELIHOOD × CONSEQUENCE`

**Consequence Levels** (MCF Methodology):
- **Nivå 3 (Allvarlig)**: Death, life-threatening situations, critical operational impact
- **Nivå 2 (Betydande)**: Serious harm, significant operational disruption
- **Nivå 1 (Måttlig)**: Noticeable harm, moderate consequences
- **Nivå 0 (Försumbar)**: Minimal impact

**Identified Critical Risks**:
- Ransomware attacks → K3-R3-T3 impact
- Insider threats → K2 impact with high likelihood
- Phishing campaigns → K3-R3-T3 impact pathway

---

## 📈 Key Deliverables

### 1. **System Categorization**
- Information classification using K-R-T (Konfidentialitet-Riktighet-Tillgänglighet) model
- Impact analysis aligned with Swedish MCF methodology
- Legal justification for each classification level

### 2. **Security Control Baseline**
- 15+ security controls mapped to Swedish legal requirements
- Gap analysis identifying implementation priorities
- Compliance matrix (Cybersäkerhetslagen × GDPR × Patientdatalagen)

### 3. **Incident Response Plan**
- Parallel reporting to MCF (CSIRT) and IMY with correct timelines:
  - **24 hours**: Initial notification (*upplysning*) to MCF
  - **72 hours**: Formal incident report (*incidentanmälan*) to MCF
  - **72 hours**: GDPR breach notification to IMY
  - **30 days**: Final incident report (*slutrapport*) to MCF

### 4. **Authorization Package**
- Executive risk acceptance decision
- Conditional authorization with remediation timeline
- 12-month authorization period with continuous monitoring requirements

---

## 🎓 Skills Demonstrated

### Cybersecurity Competencies
- ✅ Risk management framework implementation (NIST RMF)
- ✅ Information classification and impact analysis
- ✅ Security control selection and justification
- ✅ Threat modeling and vulnerability assessment
- ✅ Incident response planning

### Legal & Compliance
- ✅ Swedish cybersecurity law interpretation (Cybersäkerhetslagen)
- ✅ GDPR compliance for healthcare (Art. 9, 32, 33)
- ✅ Healthcare-specific data protection (Patientdatalagen)
- ✅ Multi-jurisdictional compliance mapping

### Technical Expertise
- ✅ Healthcare IT systems architecture
- ✅ Cryptographic controls (AES-256, TLS 1.3)
- ✅ Identity and Access Management (MFA, RBAC)
- ✅ Security monitoring and logging
- ✅ Business continuity planning

---

## 📁 Repository Contents
```
nist-rmf-swedish-healthcare/
├── README.md                          # This file
└── riskanalys-stockholms-lakarhus.pdf # Complete RMF implementation document
```

---

## 🌍 Context & Rationale

### Why NIST RMF for Swedish Healthcare?

**Challenge**: Swedish healthcare providers need structured cybersecurity frameworks, but US-centric NIST RMF requires significant adaptation for Swedish legal compliance.

**Solution**: This project demonstrates how to:
1. Preserve NIST RMF's structured methodology
2. Replace US regulations (FISMA, HIPAA) with Swedish equivalents
3. Adapt classification systems (FIPS 199 → MCF K-R-T)
4. Integrate EU/Swedish incident reporting timelines
5. Apply Swedish-specific technical requirements (BankID, IMY/MCF reporting)

**Value**: Creates a reusable template for Swedish healthcare organizations implementing international cybersecurity frameworks while maintaining legal compliance.

---

## 🔍 Technical Highlights

### Legal Citation Accuracy
Every legal reference has been verified against:
- Cybersäkerhetslagen (SFS 2025:1506) - Sweden's NIS2 implementation
- Cybersäkerhetsförordningen (SFS 2025:1507) - MCF/CSIRT structure
- GDPR (EU 2016/679) - with Swedish data protection supplements
- Patientdatalagen (SFS 2008:355) - healthcare-specific data protection

### Realistic Scenario Design
- Organization size triggers "viktig enhet" classification (125 employees, 75M SEK)
- System boundary excludes national infrastructure (NPÖ, e-recept) realistically
- Risk scenarios based on actual Swedish healthcare cyber incidents
- Implementation timeline reflects realistic organizational constraints

---

## 💼 Professional Application

This methodology is directly applicable to:
- Healthcare providers implementing cybersecurity frameworks
- IT security consultants advising Swedish healthcare organizations
- Compliance officers mapping international standards to Swedish law
- Risk managers conducting healthcare system assessments
- Auditors reviewing healthcare cybersecurity compliance

---

## 📚 Academic Foundation

**Program**: IT-säkerhetsspecialist (IT Security Specialist)  
**Institution**: TUC Yrkeshögskola, Stockholm  
**Focus Areas**: Cybersecurity law, compliance, risk management

**Relevant Coursework**:
- Swedish cybersecurity legislation (Cybersäkerhetslagen, NIS2)
- GDPR and data protection law
- Healthcare sector compliance (Patientdatalagen)
- NIST frameworks (RMF, Cybersecurity Framework)
- Risk analysis methodologies

---

## 📄 License & Disclaimer

**Educational Purpose**: This is a portfolio project demonstrating cybersecurity and legal compliance competencies. Stockholm Läkarhus AB is a fictional organization created for educational purposes.

**Legal Accuracy**: All legal references were verified as of January 2026. Swedish cybersecurity legislation is subject to change; consult current regulations for real implementations.

**Not Legal Advice**: This document demonstrates technical implementation and does not constitute legal advice. Organizations should consult qualified legal counsel for compliance matters.

---

## 🙏 Acknowledgments

- **NIST** for the Risk Management Framework methodology
- **MCF (Myndigheten för civilt försvar)** for Swedish cybersecurity guidance
- **IMY** for GDPR healthcare guidance
- **TUC Yrkeshögskola** for academic supervision

---

**Last Updated**: January 2026  
**Document Version**: 1.0  
**Framework Version**: NIST SP 800-37 Rev. 2
