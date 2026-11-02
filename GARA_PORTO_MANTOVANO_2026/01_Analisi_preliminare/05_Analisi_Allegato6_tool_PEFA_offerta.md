# ALLEGATO 6 – TOOL ARERA "PEFA_Gara_Offerta" (det. 1/DTAC/2025): COME FUNZIONA E COME SI GIOCA

File originale: `00_Bando_e_atti_di_gara/Allegato_6_PEFA_Gara_Offerta.xlsx` (copia di lavoro in `05_Busta_C_Offerta_economica_PEF/`). Il disciplinare chiede la consegna in **.XLSM e .PDF**, firmati digitalmente e **asseverati** da commercialista o revisore legale: il file ricevuto è .xlsx, da chiarire con quesito se è accettato o va salvato come .xlsm.

## 1. Struttura del tool

| Foglio | Chi compila | Contenuto |
|---|---|---|
| IN_Anagrafica | ETC + Gestore (riga 11: denominazione, P.IVA, ID ARERA, date) | Bacino PORTO MANTOVANO, pop. 16.676, inizio 2027. Attività: raccolta SI, spazzamento SI, trattamento e recupero SI, **smaltimento NO**, gestione tariffe SI |
| IN_PAR | ETC (righe 1-85) + **Gestore (righe 90-98)** | Livello di partenza: RD 92,5%, R1 (a-2) 0,43 classe F con obiettivo 0,50 al 2029, R2 non valorizzato, γ = −0,15 nel 2027-28 poi 0, sharing b 0,7 (2027-28) poi 0,4, schema regolatorio II, CUeff 30 cent/kg vs benchmark 34,36. **Righe 91-92: Xcom e Kcom offerti per anno (H..O = 2027-2034). Righe 95-98: COnew TV, COI TV, COnew TF, COI TF offerti per anno.** Oggi vuote |
| PianoTariffarioGARA | ETC | Il PEFA di gara (identico al PDF "PEFA di GARA"), ∑Ta 2027 = 2.249.566 → 2034 = 2.397.416; somma 8 anni 18.544.596 + attività esterne 87.500 × 8 = **19.244.596** |
| PianoTariffarioOfferta | **Gestore** | Ogni voce di costo (CRT, CTR, CRD, CSL, CARC, CGG, CCD, COal, Amm, Acc, R...) è una formula che richiama il foglio GARA: **si sovrascrive con i propri valori**. Xcom, Kcom, COnew arrivano da IN_PAR righe 91-98. Il foglio calcola ρ, ∑Tmax e il delta tagliato |
| Conto_Economico, RendicontoFinanziario, StatoPatrimoniale | Gestore | Precompilati con i numeri del PEFA di gara (costi operativi 1.240.827, personale 827.500, ammortamenti 196.187, utile netto 107.121 nel 2027; apporto capitale 1.324.062). Vanno riscritti con i nostri valori; check SP attivo = passivo |
| Tab | — | Classi R1/R2/H, intervalli γ e Xreg, rpi 1,9% fino al 2029 e **0 dal 2030** (incoerente con il PEFA di gara che usa 1,9% su tutti gli anni: quesito) |

## 2. Meccanica del limite alla crescita (quello che decide i 20 punti economici)

ρ_a = rpi − (Xreg + **Xcom**) + **Kcom** + CRI, con rpi 1,9%, Xreg 0,1%, CRI 0.
∑Tmax_a = ∑T_(a−1) × (1 + ρ). Se ∑Ta offerto supera ∑Tmax, l'eccedenza viene tagliata (riga 64 "delta").
Per il 2027 il confronto è con il 2026 del gestore uscente: **2.689.045 €**. Il PEFA di gara parte da 2.249.566 € nel 2027 (−16%), quindi nel primo anno il tetto non morde; morde negli anni successivi se il percorso dei costi cresce più di ρ.

Parametri a base di gara: Xcom 0,1%, Kcom 5,0%, COnew TV 1.579 → 1.956 €/anno, COnew TF 63.469 → 75.527 €/anno. Punteggio: F.1 Xcom più ALTO vince (9 pt), F.2 Kcom più BASSO vince (3 pt), F.3/F.4 COnew più BASSI vincono (4 + 4 pt). Tutti relativi al migliore in gara, aggregati con i pesi Wt (il primo anno pesa 22%, l'ottavo 2,8%).

### Simulazione sul percorso di costi del PEFA di gara

| Xcom | Kcom | ρ | Ricavi 8 anni ammessi | Taglio |
|---|---|---|---|---|
| 0,1% | 5,0% | 6,70% | 18.544.596 | 0 |
| 3,0% | 5,0% | 3,80% | 18.541.012 | 3.584 |
| 0,1% | 0,0% | 1,70% | 18.417.997 | 126.599 |
| 1,0% | 0,0% | 0,80% | 18.145.522 | 399.075 |
| 2,0% | 0,0% | −0,20% | 17.675.270 | 869.326 |
| 3,0% | 0,0% | −1,20% | 17.220.446 | 1.324.151 |
| 5,0% | 0,0% | −3,20% | 16.104.887 | 2.439.709 |

Lettura: con il percorso di costi "a gradini" del PEFA di gara (+4% nel 2029), spingere Xcom e azzerare Kcom costa centinaia di migliaia di euro di ricavi. Ma il percorso lo scriviamo noi: **con un percorso piatto o decrescente in termini nominali** (efficienze che assorbono l'inflazione) il taglio è zero anche con Xcom 2% e Kcom 0.

### Il punto strategico decisivo (da chiarire con quesito, scadenza 19/11)

Il punteggio economico non premia un ∑Ta più basso. Il tetto del 2027 è 2.689.045 × (1+ρ): un concorrente potrebbe scrivere nel PEFA di offerta entrate 2027 **superiori** a quelle del PEFA di gara (fino a ~2,65 M€ con Xcom 3%) e poi farle scendere, incassando negli 8 anni fino a 20,4 M€ invece di 18,5 M€, prendendo comunque i 9 punti di Xcom. Serve chiedere alla CUC se il PEFA di offerta può prevedere ∑Ta superiori al PEFA di gara (nel rispetto del limite di crescita) o se il PEFA di gara è un tetto. La risposta cambia completamente l'impostazione dell'offerta economica, nostra e dei concorrenti.

Scenario massimo teorico (2027 al tetto, poi tetto ogni anno), Kcom 0:

| Xcom | ρ | ∑T 2027 | ∑T 2034 | Somma 8 anni |
|---|---|---|---|---|
| 0,1% | 1,70% | 2.734.759 | 3.077.271 | 23.225.031 |
| 2,0% | −0,20% | 2.683.667 | 2.646.321 | 21.319.653 |
| 3,0% | −1,20% | 2.656.777 | 2.441.483 | 20.382.644 |
| 5,0% | −3,20% | 2.602.996 | 2.073.008 | 18.635.129 |

## 3. Come impostare il nostro PEFA di offerta

1. Partire dal dimensionamento tecnico (FTE, mezzi, contenitori, impianti) e costruire il Conto Economico per anno; da lì derivare le componenti MTR-3 (CRT/CRD/CSL/CARC/CGG/CK) e sovrascrivere il foglio Offerta.
2. Decidere il percorso: nominale piatto o lievemente decrescente, così da poter offrire **Xcom alto (2-3%) e Kcom 0** senza tagli. Significa dichiarare recuperi di produttività reali: vanno giustificati nella relazione esplicativa (automezzi nuovi, RFID, riduzione secco, mini-isole).
3. COnew TV/TF: a zero vale 8 punti pieni se nessuno offre valori negativi (non ammessi). Verificare che azzerarli non tolga copertura a costi incentivanti che la relazione di gara destina a specifiche attività (sono i costi "incentivanti" ex art. 10 MTR-3: se li azzeriamo, quei servizi vanno coperti dentro gli altri costi).
4. Conto economico, rendiconto e stato patrimoniale: ricostruire con investimenti reali (mezzi acquistati vs noleggio), TFR, fondo crediti (FCDE 5% è nel PEFA di gara via accantonamenti 102-113 k€/anno), imposte IRES/IRAP, DSCR. Utile netto del PEFA di gara: 97-130 k€/anno (4,3-5,6% dei ricavi).
5. Asseverazione: individuare subito il commercialista/revisore e concordare il formato; prevedere 3-4 giorni per la sua revisione prima del 27/11.
