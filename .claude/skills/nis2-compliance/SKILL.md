---
name: nis2-compliance
description: NIS2 directive compliance knowledge and checklists for cybersecurity requirements assessment
---

# NIS2 Compliance Skill

Denna skill ger tillgång till strukturerad kunskap om NIS2-direktivet för compliance-granskningar.

## Kunskapsfiler

Fullständig NIS2-dokumentation finns i:
- `markdown/NIS2_BY_ARTICLE_COMPLETE.md` - Komplett direktiv (64 KB)
- `markdown/ARTICLE4_GUIDELINES_COMPLETE.md` - Lex specialis/DORA (15 KB)
- `markdown/ARTICLE3_4_GUIDELINES_COMPLETE.md` - Entitetsregistrering (9 KB)

## Snabbreferens: Artikel 21 - De 10 kraven

### (a) Riskanalys och säkerhetspolicyer
**Krav**: Dokumenterade policies för informationssystemsäkerhet
**Kontrollera**:
- [ ] Informationssäkerhetspolicy finns
- [ ] Riskanalysprocess dokumenterad
- [ ] Risk register uppdaterat
- [ ] Policies godkända av ledningen

### (b) Incidenthantering
**Krav**: Rutiner för att hantera incidenter
**Kontrollera**:
- [ ] Incident Response Plan
- [ ] Incidentklassificering definierad
- [ ] Eskaleringsprocedurer
- [ ] Loggning och övervakning aktiverad
- [ ] Kontaktlista för CSIRT

### (c) Driftskontinuitet
**Krav**: Backup, disaster recovery, krishantering
**Kontrollera**:
- [ ] Backup-policy och scheman
- [ ] Backup-tester dokumenterade
- [ ] Disaster Recovery Plan
- [ ] Business Continuity Plan
- [ ] RTO/RPO definierade

### (d) Leverantörssäkerhet
**Krav**: Säkerhet i leverantörsrelationer
**Kontrollera**:
- [ ] Leverantörsbedömningsprocess
- [ ] Säkerhetskrav i avtal
- [ ] SLA med säkerhetsklausuler
- [ ] Tredjepartsriskbedömning

### (e) Säker utveckling
**Krav**: Säkerhet i anskaffning, utveckling och underhåll
**Kontrollera**:
- [ ] Secure SDLC dokumenterad
- [ ] Kodgranskning för säkerhet
- [ ] Sårbarhetsskanning (SAST/DAST)
- [ ] Dependency scanning
- [ ] Patch management

### (f) Effektivitetsbedömning
**Krav**: Bedöma om åtgärder fungerar
**Kontrollera**:
- [ ] Penetrationstester
- [ ] Säkerhetsrevisioner
- [ ] KPIer för säkerhet
- [ ] Regelbunden uppföljning

### (g) Cyberhygien och utbildning
**Krav**: Grundläggande praxis och utbildning
**Kontrollera**:
- [ ] Security awareness program
- [ ] Utbildningsregister
- [ ] Phishing-tester
- [ ] Dokumenterade rutiner för användare

### (h) Kryptografi
**Krav**: Policies för kryptering
**Kontrollera**:
- [ ] Krypteringspolicy
- [ ] Data-at-rest kryptering
- [ ] Data-in-transit kryptering (TLS)
- [ ] Nyckelhantering

### (i) HR och åtkomstkontroll
**Krav**: Personalsäkerhet och behörighetshantering
**Kontrollera**:
- [ ] IAM-system
- [ ] RBAC/ABAC implementerat
- [ ] Onboarding-säkerhetsprocedur
- [ ] Offboarding med behörighetsrevokering
- [ ] Privileged Access Management

### (j) MFA och säker kommunikation
**Krav**: Multifaktorautentisering, säkra kanaler
**Kontrollera**:
- [ ] MFA för alla användare
- [ ] MFA för admin/privilegierade konton
- [ ] Säkra kommunikationskanaler
- [ ] Nödkommunikation

---

## Snabbreferens: Artikel 23 - Incidentrapportering

### Tidslinje

| Fas | Deadline | Innehåll |
|-----|----------|----------|
| Early Warning | **24 timmar** | Misstänkt attack? Cross-border impact? |
| Incident Notification | **72 timmar** | Initial bedömning, severity, IoCs |
| Intermediate Report | Vid begäran | Statusuppdatering |
| Final Report | **1 månad** | Root cause, åtgärder, lessons learned |

### Vad är en "signifikant incident"?

En incident är signifikant om den:
- Orsakar eller kan orsaka **allvarlig driftsstörning** eller **ekonomisk förlust**
- Påverkar eller kan påverka andra genom **betydande materiell eller immateriell skada**

---

## Compliance-nivåer

### Essential Entity (Väsentlig)
- Proaktiv tillsyn
- Böter: €10M eller 2% av global omsättning
- Ledningsansvar explicit

### Important Entity (Viktig)
- Reaktiv tillsyn
- Böter: €7M eller 1.4% av global omsättning
- Ledningsansvar explicit

---

## Sektorer (Annex I - Högkritiska)

1. Energi (el, gas, olja, värme, vätgas)
2. Transport (flyg, järnväg, vatten, väg)
3. Bankverksamhet
4. Finansmarknadsinfrastruktur
5. Hälsa
6. Dricksvatten
7. Avloppsvatten
8. Digital infrastruktur
9. ICT-tjänstehantering (MSP/MSSP)
10. Offentlig förvaltning
11. Rymd

## Sektorer (Annex II - Övriga kritiska)

1. Post och kurir
2. Avfallshantering
3. Kemikalier
4. Livsmedel
5. Tillverkning (medicinteknisk, elektronik, fordon)
6. Digitala tjänster (marknadsplatser, sökmotorer, sociala nätverk)
7. Forskning
