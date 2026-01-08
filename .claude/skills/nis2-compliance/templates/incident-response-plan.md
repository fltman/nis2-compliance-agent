# Incident Response Plan (NIS2-kompatibel)

**Organisation**: [NAMN]
**Version**: 1.0
**Godkänd av**: [NAMN/ROLL]
**Datum**: [DATUM]
**Nästa review**: [DATUM]

---

## 1. Syfte och omfattning

Denna plan beskriver hur [ORGANISATION] hanterar cybersäkerhetsincidenter i enlighet med NIS2-direktivets artikel 23.

### Omfattning
- Alla IT-system och nätverk
- Alla anställda och konsulter
- Tredjepartsleverantörer med systemåtkomst

---

## 2. Definitioner

### Incident
En händelse som faktiskt komprometterar tillgänglighet, autenticitet, integritet eller konfidentialitet för data eller tjänster.

### Signifikant incident (NIS2 Art. 23(3))
En incident är signifikant om den:
- **(a)** Har orsakat eller kan orsaka allvarlig driftsstörning eller ekonomisk förlust
- **(b)** Har påverkat eller kan påverka andra genom betydande materiell eller immateriell skada

### Near miss
En händelse som kunde ha komprometterat säkerheten men förhindrades eller inte materialiserades.

---

## 3. Roller och ansvar

| Roll | Ansvar | Kontakt |
|------|--------|---------|
| **Incident Manager** | Leder incidenthantering, fattar beslut | |
| **Security Team** | Teknisk analys och åtgärder | |
| **IT Operations** | Systemåterställning | |
| **Kommunikation** | Intern/extern kommunikation | |
| **Legal/Compliance** | Regulatorisk rapportering | |
| **Ledning** | Eskalerade beslut, resurser | |

### Kontaktlista

| Funktion | Namn | Telefon | E-post |
|----------|------|---------|--------|
| Incident Manager | | | |
| Security Lead | | | |
| IT Chef | | | |
| CISO | | | |
| VD | | | |
| **Extern CSIRT** | | | |

---

## 4. Incidentklassificering

### Severity-nivåer

| Nivå | Beskrivning | Responstid | Eskalering |
|------|-------------|------------|------------|
| **Kritisk** | Omfattande påverkan på verksamhet, dataläckage, ransomware | Omedelbart | VD, styrelse |
| **Hög** | Signifikant påverkan, potentiell compliance-brist | < 1 timme | CISO, IT Chef |
| **Medium** | Begränsad påverkan, enskilda system | < 4 timmar | Security Team |
| **Låg** | Minimal påverkan, misstänkt aktivitet | < 24 timmar | IT Operations |

### Incidenttyper

- Malware/Ransomware
- Dataintrång
- DDoS-attack
- Phishing
- Insider threat
- Leverantörsrelaterad incident
- Konfigurationsfel
- Systemfel med säkerhetspåverkan

---

## 5. Incidenthanteringsprocess

### Fas 1: Detektion och initial bedömning (0-1 timme)

1. **Identifiera** incidenten via:
   - Säkerhetsverktyg (SIEM, IDS/IPS)
   - Användarrapporter
   - Extern information

2. **Dokumentera** initial information:
   - Vad hände?
   - När upptäcktes det?
   - Vilka system påverkas?
   - Vem upptäckte det?

3. **Klassificera** severity-nivå

4. **Aktivera** Incident Response Team vid severity Hög eller Kritisk

### Fas 2: Containment (1-4 timmar)

1. **Isolera** påverkade system
2. **Säkra** bevis (loggar, minne, disk)
3. **Förhindra** spridning
4. **Dokumentera** alla åtgärder

### Fas 3: Eradication och Recovery

1. **Identifiera** root cause
2. **Ta bort** hot (malware, obehörig åtkomst)
3. **Återställ** system från backup vid behov
4. **Verifiera** att hotet är eliminerat
5. **Återställ** normal drift

### Fas 4: Post-incident

1. **Lessons learned** möte inom 1 vecka
2. **Uppdatera** rutiner och säkerhetsåtgärder
3. **Dokumentera** fullständig incident timeline
4. **Rapportera** till ledning och relevanta parter

---

## 6. NIS2-rapportering (Artikel 23)

### Rapporteringskrav

| Fas | Deadline | Mottagare | Innehåll |
|-----|----------|-----------|----------|
| **Early Warning** | 24 timmar | CSIRT | Misstänkt attack? Cross-border? |
| **Incident Notification** | 72 timmar | CSIRT | Initial bedömning, severity, IoCs |
| **Intermediate Report** | Vid begäran | CSIRT | Statusuppdatering |
| **Final Report** | 1 månad | CSIRT | Root cause, åtgärder |

### CSIRT-kontakt

| Land | CSIRT | Kontakt |
|------|-------|---------|
| Sverige | CERT-SE | cert@cert.se, 010-240 40 40 |

### Early Warning (24h) - Mall

```
EARLY WARNING - [Incident ID]
Datum/tid upptäckt: [DATUM TID]
Organisation: [NAMN]
Kontaktperson: [NAMN, TELEFON, E-POST]

1. Incidenttyp: [Typ]
2. Misstänkt olaglig/illvillig handling: [Ja/Nej/Okänt]
3. Potentiell cross-border påverkan: [Ja/Nej]
4. Kort beskrivning: [Max 200 ord]
```

### Incident Notification (72h) - Mall

```
INCIDENT NOTIFICATION - [Incident ID]
Refererar till Early Warning: [ID]

1. Uppdaterad beskrivning
2. Initial bedömning av severity: [Kritisk/Hög/Medium]
3. Påverkade tjänster/system
4. Antal påverkade användare (uppskattning)
5. Indikatorer på kompromiss (IoCs)
6. Vidtagna åtgärder
```

### Final Report (1 månad) - Mall

```
FINAL REPORT - [Incident ID]

1. SAMMANFATTNING
   - Incidenttyp
   - Tidslinje
   - Total påverkan

2. DETALJERAD BESKRIVNING
   - Kronologisk händelsebeskrivning
   - Teknisk analys

3. ROOT CAUSE
   - Underliggande orsak
   - Bidragande faktorer

4. ÅTGÄRDER
   - Vidtagna åtgärder
   - Pågående åtgärder
   - Planerade åtgärder

5. CROSS-BORDER PÅVERKAN
   - Påverkade länder
   - Koordinering med andra CSIRTs

6. LESSONS LEARNED
   - Vad fungerade bra
   - Förbättringsområden
   - Rekommendationer
```

---

## 7. Kommunikation

### Intern kommunikation
- Incident-kanal i [VERKTYG]
- E-postlista: incident@[DOMÄN]
- Telefonbrygga: [NUMMER]

### Extern kommunikation
- All extern kommunikation via Kommunikationsansvarig
- Ingen information till media utan godkännande från VD
- Kundkommunikation enligt mall

---

## 8. Testning och övning

| Aktivitet | Frekvens | Ansvarig |
|-----------|----------|----------|
| Tabletop exercise | Kvartalsvis | CISO |
| Teknisk övning | Halvårsvis | Security Team |
| Full-scale exercise | Årligen | Incident Manager |
| Plan review | Årligen | Compliance |

---

## 9. Dokumenthistorik

| Version | Datum | Ändring | Godkänd av |
|---------|-------|---------|------------|
| 1.0 | [DATUM] | Initial version | |
