# NIS2 Compliance Agent

En Claude Code agent som granskar kod och dokumentation mot EU:s NIS2-direktiv (Directive 2022/2555) för cybersäkerhet.

## Installation

Kopiera hela mappen till ditt projekt:

```bash
cp -r nis2-compliance-agent/.claude /ditt/projekt/
cp -r nis2-compliance-agent/markdown /ditt/projekt/
```

Eller klona direkt:

```bash
cd /ditt/projekt
git clone https://github.com/[USER]/nis2-compliance-agent.git temp
cp -r temp/.claude temp/markdown .
rm -rf temp
```

## Struktur

```
.claude/
├── agents/
│   └── nis2-compliance.md          # Agentdefinition
└── skills/
    └── nis2-compliance/
        ├── SKILL.md                 # Snabbreferens
        └── templates/
            ├── compliance-checklist.md
            └── incident-response-plan.md

markdown/
├── NIS2_BY_ARTICLE_COMPLETE.md     # Hela direktivet (64 KB)
├── ARTICLE4_GUIDELINES_COMPLETE.md  # Lex specialis/DORA
├── ARTICLE3_4_GUIDELINES_COMPLETE.md # Entitetsregistrering
└── nis2_by_article/                 # Artikelbaserade filer
    ├── art1_subject_matter.md
    ├── art20_21_22_risk_management.md
    ├── art23_incident_reporting.md
    └── ...
```

## Användning

Agenten aktiveras automatiskt vid säkerhetsrelaterade frågor, eller anropa explicit:

```
Granska detta projekt mot NIS2-kraven
```

```
Vilka krav ställer NIS2 på incidentrapportering?
```

```
Generera en compliance-checklista för vår organisation
```

## Vad agenten kan göra

| Kapacitet | Beskrivning |
|-----------|-------------|
| **Granska kod** | Analyserar mot Artikel 21:s 10 minimikrav |
| **Identifiera gaps** | Hittar compliance-brister med åtgärdsförslag |
| **Generera dokumentation** | Checklistor, incident response plans, policies |
| **Bedöma rutiner** | Verifierar incidentrapportering (24h/72h/1 månad) |

## NIS2 Artikel 21 - De 10 minimikraven

Agenten kontrollerar:

1. **(a)** Riskanalys och säkerhetspolicyer
2. **(b)** Incidenthantering
3. **(c)** Driftskontinuitet (backup, DR, BCP)
4. **(d)** Leverantörssäkerhet
5. **(e)** Säker utveckling (Secure SDLC)
6. **(f)** Effektivitetsbedömning (pentester, audits)
7. **(g)** Cyberhygien och utbildning
8. **(h)** Kryptografi
9. **(i)** HR och åtkomstkontroll
10. **(j)** MFA och säker kommunikation

## Rapportformat

Agenten levererar strukturerade rapporter:

```
## NIS2 Compliance Status

### Uppfyllda krav ✅
- [Krav] - [Hur det uppfylls]

### Gaps som måste åtgärdas ⚠️
- [Krav] - [Vad som saknas] - [Åtgärdsförslag]

### Kritiska brister 🚨
- [Krav] - [Risk] - [Omedelbar åtgärd]
```

## Medföljande templates

- **compliance-checklist.md** - Fullständig checklista för alla krav
- **incident-response-plan.md** - Mall för incidenthantering enligt Artikel 23

## Krav

- Claude Code CLI
- Projektet måste ha `.claude/`-mappen och `markdown/`-mappen

## Licens

MIT

## Bidrag

Pull requests välkomna! Särskilt:
- Uppdateringar när NIS2-implementeringsakter publiceras
- Fler templates
- Översättningar
