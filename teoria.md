# SICUREZZA DEI SISTEMI INFORMATICI

---

## COMPETENZE

Al termine del corso i partecipanti saranno in grado di:

- Sviluppare (o coordinare chi sviluppa) procedure software rispettando specifiche, tempi e costi, integrando controlli di sicurezza pratici.
- Valutare rischi e priorità, proporre interventi e piani di mitigazione.
- Identificare e applicare contromisure rapide per proteggere asset (sito, server, dispositivi connessi).
- Predisporre semplici procedure operative per la risposta a incidenti (first response).

---

## OBIETTIVI

- Proteggere asset aziendali (sito web, server, dispositivi, sistemi embedded) riducendo superficie di attacco.
- Limitare l’impatto operativo, economico e reputazionale in caso di compromissione.
- Consegnare strumenti concreti: checklist, modelli di valutazione rischio, mini-procedure operative.

---

## CONTENUTI (panoramica)

- Sicurezza fisica e logica
- Valutazione dei rischi e prioritizzazione
- Malware e virus: riconoscere e ridurre i rischi
- Strumenti di protezione: antivirus, EDR, firewall, backup
- Protezione rete: segmentazione, Wi-Fi sicuro, firewall di base
- Hardening sistemi operativi: checklist operative
- Crittografia (chiave pubblica), certificati SSL/TLS e gestione chiavi
- Deep Web & Dark Web: differenze e rischi per le organizzazioni

---

# Programma dettagliato

---

## Capitolo 1 — Introduzione alla sicurezza applicativa

**Descrizione:** panoramica non tecnica sul perché la sicurezza è fondamentale per progetti software e servizi digitali. Si spiega come la sicurezza influisce su costi, tempi, reputazione e continuità operativa.

**Argomenti trattati:**

- Cos’è la sicurezza applicativa (concetti in termini pratici).
- Il modello CIA (Confidenzialità, Integrità, Disponibilità) spiegato con esempi reali.
- Ruoli e responsabilità: sviluppatori, operations, security, management.
- Introduzione semplice a OWASP Top 10 come lista di controllo.

**Teoria:**

La **sicurezza applicativa** è l’insieme delle pratiche, dei controlli e delle tecnologie che proteggono un software dalle vulnerabilità e dagli attacchi.

Non è solo un tema tecnico: influisce direttamente su **reputazione, continuità operativa e costi aziendali**.

Il **modello CIA** (Confidenzialità, Integrità, Disponibilità) è il pilastro:

- **Confidenzialità:** solo chi è autorizzato può accedere ai dati.
- **Integrità:** i dati devono restare corretti e coerenti.
- **Disponibilità:** i sistemi devono essere sempre accessibili quando necessario.

Esempio pratico:

> Se un database clienti viene rubato (violata confidenzialità), alterato (integrità), o inaccessibile per un attacco ransomware (disponibilità), il danno è enorme su più fronti.
> 

**Ruoli nella sicurezza:**

- **Sviluppatori:** scrivere codice sicuro.
- **Operations:** mantenere infrastruttura e patch.
- **Security team:** monitorare e gestire vulnerabilità.
- **Management:** definire priorità e politiche.

**OWASP Top 10**: https://owasp.org/www-project-top-ten/ è l’elenco delle dieci vulnerabilità più critiche nelle applicazioni web. Strumento pratico per controllare la qualità del codice e la sicurezza dei rilasci.

## Esercizi

**Role play:**

Simula una riunione tra sviluppatore e project manager in cui emerge un problema di sicurezza (es. password in chiaro).

→ Obiettivo: discutere come gestirlo senza rallentare il progetto.

---

## Capitolo 2 — Sicurezza fisica e logica; valutazione dei rischi

**Descrizione:** esamina le protezioni fisiche (accesso a sedi, dispositivi) e logiche (accessi, permessi), e introduce un processo semplice di valutazione dei rischi per scegliere le priorità operative.

**Argomenti trattati:**

- Differenze tra sicurezza fisica e logica; esempi pratici.
- Valutazione del rischio in 5 fasi: identificare asset → minacce → probabilità → impatto → priorità.
- Strumenti semplici per mappare rischi (template mappa dei rischi).

### Teoria

La **sicurezza fisica** protegge gli asset materiali (server, dispositivi, archivi, badge).

La **sicurezza logica** protegge l’accesso digitale (password, ruoli, VPN, cifratura).

Entrambe sono essenziali: un server protetto digitalmente ma accessibile fisicamente da chiunque resta vulnerabile.

**Valutazione dei rischi in 5 fasi:**

1. Identificare gli asset (hardware, software, dati).
2. Individuare le minacce (furto, malware, errore umano).
3. Stimare la probabilità.
4. Valutare l’impatto.
5. Assegnare priorità alle contromisure.

**Mappa dei rischi:** uno strumento visuale per capire dove agire prima.

### Esercizi

**Test pratico:**

- Identifica tre asset della tua azienda e assegna a ciascuno una minaccia, una probabilità e un impatto.
- Costruisci una mini mappa dei rischi (anche su foglio).

---

## Capitolo 3 — Malware e virus: cosa sono e come difendersi

**Descrizione:** spiegazione delle classi principali di malware e delle misure di protezione che qualsiasi organizzazione può applicare immediatamente.

**Argomenti trattati:**

- Tipologie: virus, worm, trojan, ransomware, spyware, rootkit (spiegati con esempi).
- Vettori principali: email/phishing, download malevoli, vulnerabilità non patchate, supply-chain.
- Misure difensive pratiche: aggiornamenti, antivirus/EDR, backup e policy di accesso.

## Teoria

**Malware** = “software malevolo”, qualsiasi programma che danneggia o ruba informazioni.

Tipi principali:

- **Virus:** si replica infettando altri file.
- **Worm:** si propaga automaticamente in rete.
- **Trojan:** finge di essere utile ma esegue codice dannoso.
- **Ransomware:** cripta dati e chiede riscatto.
- **Spyware:** raccoglie informazioni.
- **Rootkit:** ottiene controllo nascosto del sistema.

**Principali vettori di infezione:**

- Email con allegati sospetti.
- Link di phishing.
- Software non aggiornato.
- Dispositivi USB non controllati.

**Difesa:**

- Aggiornamenti regolari.
- Antivirus/EDR attivi e monitorati.
- Backup periodici offline.
- Policy di accesso con privilegi minimi.

### Esercizi

**Role play:**

Simulazione “Sospetto malware su PC aziendale”.

→ Il gruppo deve elencare le prime 5 azioni da fare (es. isolare, segnalare, non spegnere, contattare IT).

---

## Capitolo 4 — Protezione di endpoint, rete e hardening dei sistemi

**Descrizione:** misure pratiche, semplici da mettere in opera, per consolidare server, workstation e reti in modo economico ed efficace.

**Argomenti trattati:**

- Scelta e controllo di un antivirus/EDR(Endpoint Detection and Response); cosa aspettarsi dalle soluzioni di mercato.
- Concetti pratici di protezione di rete: segmentazione, firewall (policy di base), Wi-Fi sicuro.
- Hardening OS: checklist operativa (disabilitare servizi non necessari, aggiornamenti, utenti con privilegi).

### Teoria

Un **endpoint** è qualsiasi dispositivo connesso alla rete aziendale (PC, laptop, smartphone).

La protezione deve includere:

- **Antivirus/EDR:** strumenti che rilevano e isolano comportamenti anomali.
- **Firewall:** filtra il traffico in entrata/uscita.
- **Segmentazione di rete:** separare zone interne per ridurre l’impatto di un’infezione.
- **Wi-Fi sicuro:** WPA3, password complesse, rete ospiti separata.

**Hardening** = rendere più “duro” il sistema:

- Disabilitare servizi inutili.
- Aggiornare regolarmente OS e applicazioni.
- Limitare utenti amministratori.
- Attivare log e monitoraggio.

### Esercizi

**Check operativo:**

Crea una mini checklist di 5 punti per migliorare la sicurezza del tuo PC.

---

## Capitolo 5 — Crittografia pratica: chiavi pubbliche, SSL/TLS e gestione dei certificati

**Descrizione:** nozioni essenziali sulla crittografia applicata: cosa serve sapere per usare correttamente SSL/TLS e gestire certificati e chiavi in azienda senza addentrarsi nella matematica.

**Argomenti trattati:**

- Concetto semplice di crittografia simmetrica vs asimmetrica.
- Perché usare certificati SSL/TLS e come verificare che siano corretti (chain, scadenza, corretto issuer).
- Best practice operative: backup delle chiavi, rotazione e protezione delle credenziali.

### Teoria

La **crittografia** protegge i dati tramite trasformazioni matematiche.

Due grandi famiglie:

- **Simmetrica:** stessa chiave per cifrare e decifrare (es. AES).
- **Asimmetrica:** coppia di chiavi pubblica/privata (es. RSA).

**SSL/TLS:** protocolli che cifrano la comunicazione tra client e server.

→ Garantisce che il sito sia autentico e che i dati non vengano intercettati.

**Certificati digitali:** garantiscono l’identità del sito o del servizio.

Best practice:

- Verificare validità e catena di certificazione.
- Evitare certificati scaduti o autofirmati.
- Proteggere e ruotare le chiavi private.

### Esercizi

**Discussione di gruppo:**

Perché è rischioso usare un certificato scaduto? Cosa comunica all’utente?

---

## Capitolo 6 — Deep Web & Dark Web: cosa sono e rischi per le organizzazioni

**Descrizione:** spiegazione delle differenze tra surface web, deep web e dark web, con focus sui rischi pratici (esfiltrazione di dati, vendita di accessi, ricadute reputazionali).

**Argomenti trattati:**

- Differenze operative tra Surface, Deep e Dark Web.
- Come i dati esposti possono finire su marketplace o forum (con esempi illustrativi).
- Cosa monitorare, quando e come segnalare (CSIRT/forze dell’ordine).

### Teoria

- **Surface Web:** parte visibile indicizzata dai motori di ricerca.
- **Deep Web:** pagine non indicizzate ma legittime (es. intranet, archivi).
- **Dark Web:** parte nascosta del Deep Web accessibile tramite software specifici (es. Tor).

**Rischi principali:**

- Vendita di dati rubati (credenziali, database).
- Diffusione di malware o exploit.
- Danni reputazionali se appaiono dati aziendali.

**Prevenzione:**

- Monitoraggio delle fughe di dati (data leak alert).
- Educazione del personale all’uso responsabile delle informazioni.
- Collaborazione con CSIRT o forze dell’ordine in caso di violazione.

**Role play:**

Simula la gestione di un alert “dati aziendali trovati su forum Dark Web”.

→ Il gruppo decide chi informa chi, cosa fare nei primi 30 minuti e come comunicare internamente.

---

## Capitolo 7 — Laboratorio finale: simulazione d’incidente e piano operativo minimo

**Descrizione:** mettere insieme tutte le conoscenze acquisite per rispondere a un incidente e produrre deliverable concreti e immediatamente utilizzabili in azienda.

**Argomenti trattati:**

- Revisione e integrazione delle misure viste (hardening, antivirus, SSL, rete).
- Role-play: simulazione di un incidente (es. rilevamento file sospetto / possibile ransomware / credenziali compromesse).
- Creazione di una mini-procedura operativa per il primo intervento (1 pagina) e di una lista minima da consegnare al management.

### Teoria

Raccoglie le conoscenze dei capitoli precedenti per gestire un **incidente informatico**.

Obiettivo: reagire rapidamente, comunicare correttamente e minimizzare danni.

Fasi chiave:

1. Rilevamento e segnalazione.
2. Isolamento del sistema compromesso.
3. Notifica a referenti IT/Security.
4. Comunicazione interna controllata.
5. Ripristino da backup e verifica post-incidente.

### Esercizi

**Role play:**

Simulazione “Attacco ransomware in azienda”.

- Team 1: utenti che segnalano.
- Team 2: IT che risponde.
- Team 3: management che comunica esternamente.

**Compito finale:**

Scrivi la tua **mini-procedura di risposta agli incidenti** (max 1 pagina) includendo:

- Primo contatto
- Azioni immediate
- Notifiche interne
- Documentazione del caso

---

## Risorse utili e fonti consigliate (per approfondire)

- **OWASP — Top 10 & Cheat Sheets** — ottimo per liste di controllo e riferimenti pratici: https://owasp.org/
- **CLuSIT — Rapporto sulla sicurezza ICT in Italia** — trend e casi nazionali (rapporto annuale).
- **AgID / Linee guida** — documenti italiani su SDLC e sicurezza applicativa.
- **CSIRT Italia / ACN** — canale ufficiale per segnalazioni e allerta.
