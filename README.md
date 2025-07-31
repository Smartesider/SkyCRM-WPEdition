# SkyCRM-WPEdition
CRM solution for Wordpress


# Komplett Funksjonsoversikt og Menystruktur for CRM + E-post + SMS WordPress-plugin

---

## 1. Meny- og modulstruktur (WP Admin)

* **CRM**

  * Kontakter
  * Bedrifter
  * Oppgaver
  * Kalender
  * Notater
* **E-post**

  * Innboks (trådvisning, søk)
  * Send e-post (utkast, signatur, maler)
  * Arkiv
  * Maler
  * Innstillinger
* **SMS**

  * Send SMS
  * Mottatte SMS
  * SMS-logg/status
  * SMS-maler
  * Innstillinger
* **Prosjektstyring**

  * Kanban-tavler
  * Milepæler
  * Tidsregistrering
  * Rapporter
* **Admin-innstillinger**

  * OAuth2 Google API
  * SMTP og e-postinnstillinger
  * SMS Gateway (SMStools)
  * Brukerroller og tilgangskontroll
  * Logging og varslinger
  * Backup og restore
  * Språk og tema
* **Dashboard**

  * Oversikt (aktiviteter, e-post/SMS status, kommende møter, oppgaver)
  * Widgets (konfigurerbare)

---

## 2. Funksjoner i detalj

### CRM-funksjoner

1. **Kontaktregister**

   * Opprett, rediger, slett kontakter
   * Import/eksport CSV, Google Kontakter-synk
   * Tilpassede felter
2. **Bedriftsregister**

   * Samle kontakter under bedrifter
   * Vis relasjoner og tilknytninger
3. **Oppgaveliste**

   * Opprett, tildel, følg opp oppgaver
   * Koble oppgaver til kontakter/bedrifter
   * Automatiske påminnelser
4. **Kalenderintegrasjon**

   * Vis og opprett møter synkronisert med Google Kalender
   * Fargekoding, påminnelser
5. **Notater per kontakt/bedrift**

   * Rike tekstnotater, koblet til aktivitet
6. **Favoritter og tagging**

   * Rask tilgang via favorittmarkering
   * Organisering med tags/kategorier
7. **Aktivitetssporing**

   * Logg over e-post, SMS, oppgaver og møter per kontakt
8. **Automatisk kobling av kommunikasjon**

   * E-post/SMS linkes automatisk til riktig kontakt basert på adresse/nummer
9. **Søk og filtrering**

   * Avanserte søk i kontakter, oppgaver, notater
10. **Mobiltilpasset visning**

    * Ryddig UI for mobilbruk

---

### E-post-funksjoner

11. **Innboks med trådvisning**

    * Vis e-post tråder med lesestatus og filtre
12. **Send e-post**

    * Rikt teksteditor med maler, signaturer, vedlegg
    * Planlegg sending
13. **E-postmaler**

    * Lagre og administrer maler for rask sending
14. **Automatisk tagging og prioritering**

    * Basert på AI-analyse eller regler
15. **Spamfilter og sortering**

    * Blokker søppelpost, sorter i mapper
16. **Varslinger**

    * Popup og e-postvarsler for nye meldinger
17. **Massehandlinger**

    * Marker som lest, slett, flytt flere e-poster samtidig
18. **Integrasjon med Gmail API og SMTP**

    * For sending og mottak, med fallback til lokal SMTP
19. **Offline modus**

    * Les og skriv e-post uten nettilgang, synkroniser ved tilkobling
20. **Søk i e-post med naturlig språk**

    * AI-basert søk for enklere funn
21. **Utkast auto-lagring**

    * Sikrer at man ikke mister arbeid
22. **Flerspråklig GUI for e-post**

    * Språkstøtte og tilpasning

---

### SMS-funksjoner

23. **Send SMS via SMStools**

    * Med kø, rate limit og sender-ID
24. **Motta SMS**

    * Polling av innkommende meldinger, vis i admin
25. **Statusoppdatering for SMS**

    * Leveringsstatus, feilvarsling
26. **SMS-maler**

    * Lagre vanlige tekster for rask sending
27. **Svar på SMS i admin**

    * To-veis SMS kommunikasjon
28. **SMS-historikk og logg**

    * Full sporbarhet med tidsstempel og status
29. **Varslinger ved feilsending**

    * Notifikasjoner til admin eller ansvarlig
30. **SMS-innstillinger**

    * Konfigurer SMStools path, rate limit, sender-ID

---

### Prosjektstyring

31. **Kanban-tavler for oppgaver**
32. **Milepælsplanlegging**
33. **Tidsregistrering på oppgaver/prosjekter**
34. **Automatiske rapporter og KPI-dashboards**
35. **Integrasjon med kalender og oppgaver**

---

### AI-funksjoner

36. **Automatisk e-postutkastgenerator**
37. **Prioritering og routing av meldinger**
38. **Sentimentanalyse**
39. **Automatisk tagging/kategorisering**
40. **Automatiske svarforslag**
41. **Språkkorrektur og oversettelse**
42. **Intelligent søk**
43. **Generering av møtereferater og oppsummeringer**
44. **Analyse av kryss-salgsmuligheter**
45. **AI-basert spamdeteksjon**

---

### Admin-innstillinger

46. **Google OAuth2 konfigurasjon**
47. **SMTP og e-postinnstillinger**
48. **SMS Gateway konfigurasjon (SMStools)**
49. **Brukerroller og tilgangskontroll**
50. **Logging, varslinger og backup**
51. **Temainnstillinger og språkvalg**

---

### Dashboard

52. **Dynamiske widgeter for aktivitet, e-post, SMS, oppgaver**
53. **Visning av kommende møter og viktige oppgaver**
54. **Statusindikatorer for API-tilkoblinger**
55. **Varsler for ubehandlede meldinger eller oppgaver**

---

## 3. Kort teknisk struktur for Copilot-koding

* **Database**: Egendefinerte tabeller for kontakter, bedrifter, e-post, SMS, oppgaver, prosjekter, logger.
* **REST API**: Endepunkter for CRUD-operasjoner på alle data, OAuth-tokenhåndtering, e-post/sms-sending, AI-forespørsler.
* **Frontend**: React/Vue SPA i WP-admin med komponenter for hver modul, rik UI med dynamiske widgeter og responsiv design.
* **Autentisering & Autorisasjon**: WP nonces, kapabiliteter, tilgangskontroll på API og UI.
* **Bakgrunnsjobber**: Cron/job queue for polling, synk, køstyring og asynkrone prosesser.
* **AI-integrasjon**: Kall til OpenAI API via backend, cache og presentasjon i UI.
* **SMS-integrasjon**: CLI/API-kall mot SMStools, håndtering av kø og status.

---

