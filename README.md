# 🎯 Customer Segmentation con Analisi RFM & K-Means Clustering

## 📌 Executive Summary
La spesa pubblicitaria e le promozioni indifferenziate riducono il ROI del marketing. Questo progetto implementa un modello di **Customer Segmentation non supervisionato** su dati transazionali reali di un e-commerce, aggregando il comportamento d'acquisto tramite la metodologia **RFM (Recency, Frequency, Monetary)** e segmentando i clienti con l'algoritmo **K-Means**.

## 🛠️ Architettura Tecnica & Pipeline
- **Dataset:** Transazioni reali e-commerce (*Online Retail Dataset*).
- **Data Preprocessing:** Pulizia record senza ID cliente, rimozione transazioni a quantità/prezzo negativo e calcolo metrica di fatturato per riga.
- **Feature Engineering (RFM):**
  - **Recency ($R$):** Giorni trascorsi dall'ultimo ordine rispetto a una snapshot date.
  - **Frequency ($F$):** Conteggio degli ordini unici per cliente.
  - **Monetary ($M$):** Fatturato totale generato dal cliente.
- **Data Transformation:** Correzione della marcata asimmetria (*right-skewness*) tramite trasformazione logaritmica (`np.log1p`) e standardizzazione delle feature (`StandardScaler`).
- **Machine Learning:** Algoritmo **K-Means** ottimizzato con valutazione del **Silhouette Score** e dell'**Elbow Method**.

---

## 👥 Segmenti Identificati & Strategie di Business

![RFM Clusters Visualization](rfm_clusters_chart.png)

| Segmento | Profilo Comportamentale | Quota Ricavi | Strategia di Marketing & CRM |
| :--- | :--- | :--- | :--- |
| **🏆 Champions (VIP)** | Bassa Recency, Altissima Frequenza e Spesa | **Top ~50-60%** | Accesso anticipato alle nuove collezioni, loyalty club esclusivo e assistenza prioritaria. |
| **⭐ Loyal Customers** | Recency recente/media, spesa costante | **~25%** | Strategie di Up-Selling, Bundle personalizzati e programmi referral con incentivi. |
| **⚠️ At Risk** | Hanno speso molto in passato ma non acquistano da mesi | **~10-15%** | Campagne di "Win-Back" con sconti personalizzati su categorie precedentemente acquistate. |
| **💤 Hibernating** | Bassa spesa, ordini rari e fermi da molto tempo | **< 5%** | Campagne automatizzate a basso costo via email; evitare budget ADV a pagamento. |

---

## 🚀 Come Eseguire il Progetto
Il codice completo è disponibile nel notebook interattivo. Puoi eseguirlo con un click:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]([INSERISCI_LINK_AL_TUO_NOTEBOOK_COLAB](https://colab.research.google.com/drive/1PfD9MlRjbiyO-5Dge-Mj5_Fkp_Po0Ow7))
