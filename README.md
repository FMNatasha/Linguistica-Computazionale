# Analisi del Sentiment e Riconoscimento Tematiche/Emozioni su Forum Online

**Corso:** Linguistica Computazionale – Modulo B  
**Università:** Università di Catania  
**Anno Accademico:** 2024/2025  

## Obiettivo del Progetto:
Questo progetto nasce come estensione del lavoro svolto nella mia tesi di laurea triennale e mira a replicare in forma automatizzata l’analisi manuale condotta su una selezione di commenti estratti dal *Forum dei Brutti*. L’analisi si concentra su tre assi: **sentiment**, **tematiche** e **emozioni**, con l'obiettivo di confrontare l'output dell'elaborazione automatica con l'annotazione manuale.

---

## Dettagli: 

- **Tipo di dati**: Commenti testuali in italiano estratti manualmente da un forum (formato Excel `.xlsx`)
- **Fonte**: Forum dei Brutti ([link al sito](https://ilforumdeibrutti.is/))
- **Problema affrontato**: Classificazione e clustering semantico (sentiment, topic, emozioni)
- **Modelli utilizzati**:
  - Word2Vec (preaddestrato e locale)
  - Sentence Transformer (`distiluse-base-multilingual-cased-v1`, `paraphrase-albert-small-v2`)
- **Librerie principali**:  
  `pandas`, `numpy`, `spacy`, `gensim`, `emoji`, `matplotlib`, `scikit-learn`, `sentence-transformers`

---

## Metodologia

### Preprocessing:
- Rimozione di punteggiatura, emoji, stopword
- Lemmatizzazione
- Estrazione solo di aggettivi, verbi, avverbi, sostantivi

### Fasi principali:
1. **Analisi del sentiment**:
   - Calcolo della similarità semantica con liste di parole positive/negative
   - Addestramento Word2Vec su corpus locale per affinità con il dominio
2. **Riconoscimento delle tematiche**:
   - Embedding delle frasi
   - Clustering semantico con KMeans e DBSCAN
3. **Analisi delle emozioni**:
   - Matching tra frasi e vettori emozionali predefiniti
   - Uso di modelli transformer per stima automatica

### Metriche:
- Similarità coseno
- Accuratezza rispetto all’annotazione manuale
- Confronto visuale tra output manuale e automatico

---

## Risultati

- Performance differenziate a seconda della task:
  - Il sentiment è stato rilevato in modo coerente per il 70–80% dei casi
  - Le tematiche hanno mostrato un buon livello di clustering nei casi fortemente marcati
  - Le emozioni risultano la dimensione più difficile da automatizzare


## Riferimenti
- Tesi triennale: "Mascolinità in crisi: l'influenza delle app di dating sul fenomeno Incel e le dinamiche di genere contemporanee"  
- Paper: *"Tinder is overrated": Neoliberal Affective Economies in an Italian Incel Forum* [CMC 2025 – Bayreuth](https://www.cmc2025.uni-bayreuth.de/en/index.html)

Developed by **Maria Natasha Fragalà** 
[LinkedIn](https://www.linkedin.com/in/marianatasha-fragalà)  
---
© 2025 Università degli studi di Catania — For educational purposes.
