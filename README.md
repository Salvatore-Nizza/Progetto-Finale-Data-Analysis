# Progetto-Finale-Data-Analysis

Questo progetto si propone di esplorare un dataset relativo a viaggi organizzati da un'agenzia che progetta **esperienze immersive e sostenibili di turismo nel metaverso**. L'obiettivo principale è comprendere i comportamenti e le preferenze degli utenti, identificare i fattori chiave che contribuiscono al successo del prodotto e ottimizzare le future strategie per l'agenzia.

L'obiettivo finale è **definire distinte user personas** e sviluppare **strategie efficaci** per il prossimo anno, al fine di personalizzare le offerte e la comunicazione per massimizzare il successo dell'agenzia nel mercato dei viaggi nel metaverso.

Il progetto è stato strutturato in tre fasi principali:
1.  **Analisi dei Dati**.
2.  **Creazione delle Personas Utente**.
3.  **Proposta di Strategia**.

## Analisi Esplorativa dei Dati (EDA)

L'analisi è stata condotta sul **dataset "Travel\_data.csv"**, che inizialmente contiene 999 osservazioni e 11 variabili. Le colonne chiave includono `visit_date`, `user_uuid`, `category`, `country_id`, `language`, `pacchetto_id`, `country`, `subscription_date`, `platform`, `hotel_id`, e `stars`.

### Preparazione dei Dati
Prima dell'analisi, i dati sono stati puliti e strutturati:
*   **Conversione delle Date**: Le colonne `visit_date` e `subscription_date` sono state convertite nel formato `datetime`.
*   **Codifica Categorica**: Le variabili categoriche come `category`, `language`, `country` e `platform` sono state codificate utilizzando `LabelEncoder`, creando nuove colonne `_encoded` (es. `category_encoded`). Questo processo ha espanso il dataset a 15 colonne.
*   **Qualità dei Dati**: Non sono stati riscontrati dati mancanti o valori outlier, indicando un dataset pulito e affidabile per l'analisi. Il dataset contiene tipi di dati `int64`, `object` e `datetime64[ns]`.

### Risultati Chiave dall'EDA
L'analisi iniziale ha rivelato importanti intuizioni sulle preferenze e sui comportamenti degli utenti:
*   **Categoria di Vacanza Preferita**: La categoria **"Luxury & Relax"** è stata identificata come la più preferita.
*   **Stagionalità delle Visite**: Sono stati osservati picchi di visite a **gennaio, aprile e settembre**, con un notevole calo a febbraio e marzo.

## Creazione delle Personas Utente (Clustering)

Per definire le personas utente, gli utenti sono stati suddivisi in **tre cluster distinti**. Questa segmentazione fornisce una comprensione variegata e dettagliata della base utenti.

### Metodologia di Clustering
*   **Variabili Utilizzate**: Il clustering ha considerato tre parametri chiave per ciascun utente:
    *   **`num_trips`**: La frequenza delle loro visite.
    *   **`avg_stars`**: Le loro valutazioni medie degli hotel.
    *   **`num_categories`**: Il numero di categorie di viaggio uniche preferite.
*   **Algoritmo**: È stato applicato l'algoritmo **K-Means con 3 cluster**, dopo aver standardizzato le feature selezionate utilizzando `StandardScaler`.

### Personas Utente Identificate
Attraverso questa analisi, sono stati definiti tre profili di viaggiatori nel metaverso:
*   **Giramondo Virtuali**: Rappresentano **105 utenti**. Cercano di "esplorare ogni angolo del metaverso, senza limiti e con la migliore tecnologia". Questo gruppo mostra tipicamente un alto numero di viaggi e esplora molte categorie.
*   **Nomadi Digitali**: Comprendono **75 utenti**. Cercano "un'esperienza che mi permetta di essere produttivo ma anche di staccare e divertirmi in un ambiente stimolante". Questo gruppo mostra una frequenza di viaggi moderata, le valutazioni medie di stelle più alte e un numero moderato di categorie esplorate.
*   **Turisti Occasionali**: Con **59 utenti**. Affermano: "Non ho molto tempo, cerco una fuga veloce dalla realtà che sia economica e rilassante". Questo gruppo tende ad avere la frequenza di viaggi più bassa, le valutazioni medie di stelle più basse e la minore diversità di categorie.

## Strategie Proposte

Basandosi sulle personas utente identificate, sono state sviluppate **strategie mirate specifiche** per ottimizzare l'engagement futuro e il successo del prodotto:

*   **Per i Giramondo Virtuali**:
    *   **Obiettivo**: Mantenere l'engagement e migliorare le valutazioni.
    *   **Offerte**: Abbonamenti per accesso illimitato, eventi speciali e anteprime, e una community online per la condivisione delle esperienze.
    *   **Comunicazione**: Utilizzare forum e gruppi online, e condurre sondaggi regolari sulla qualità.
*   **Per i Nomadi Digitali**:
    *   **Obiettivo**: Fidelizzazione dei clienti.
    *   **Offerte**: Pacchetti "Work & Relax", bonus per recensioni dettagliate e un sistema di raccomandazione avanzato.
    *   **Comunicazione**: Engagement tramite Instagram e LinkedIn, e collaborazioni con influencer.
*   **Per i Turisti Occasionali**:
    *   **Obiettivo**: Aumentare la frequenza delle visite e stimolare l'esplorazione.
    *   **Offerte**: Pacchetti brevi ed economici, elementi di gamification (punti, badge) e promozioni "porta un amico".
    *   **Comunicazione**: Implementare campagne email personalizzate e brevi video tutorial.

## Conclusioni e Prossimi Passi

Comprendere e segmentare gli utenti in base alle loro preferenze è cruciale per creare esperienze di viaggio virtuali personalizzate e più interessanti. Questo progetto ha sfruttato con successo l'analisi dei dati per segmentare gli utenti e proporre **strategie mirate**.

I **prossimi passi** riguarderanno la sperimentazione di queste strategie proposte e il monitoraggio della loro efficacia. Considerazioni future includono l'integrazione dell'Intelligenza Artificiale (AI) per esperienze più personalizzate e l'utilizzo della Realtà Aumentata (AR) per migliorare il realismo e l'immersione nel viaggio nel metaverso.

## Risorse Esterne (come parte del progetto originale)

Durante il progetto originale, sono state create e utilizzate diverse risorse interattive:
*   **Tableau Dashboards**: Dashboards interattive, inclusa una 'Overview' e una 'Clusters', sono state sviluppate per un'ulteriore esplorazione e visualizzazione dei dati.
*   **Cartella Drive**: Una cartella Google Drive associata contiene il dataset raw `Travel_data.csv`, il notebook EDA e le linee guida per navigare nelle dashboard di Tableau.
