# 👕 Kloset

## 📌 Descrizione del Progetto
Kloset è un'applicazione che aiuta gli utenti a organizzare il proprio guardaroba e ricevere suggerimenti personalizzati per gli outfit, basati su preferenze e abbinamenti cromatici. L'app utilizza **React** per il frontend, **Spring Boot** per il backend, un database **PostgrSQL** per la gestione dei dati ed utilizzo di una AI (GEMMA-AI) per suggerimenti. 

---

## 🚀 Procedura di Sviluppo

### 1️⃣ Definizione dei Requisiti e Pianificazione
- Identificazione delle funzionalità chiave: caricamento immagini, generazione outfit, salvataggio preferiti.
- Scelta dell'architettura: **React (frontend), Spring Boot (backend), PostgreSQL (database)**.
- Definizione delle API per la comunicazione tra frontend e backend.
-Utilizzo di una AI per suggerimenti (Gemma-AI tramite Hugging Face)

### 2️⃣ Configurazione dell'Ambiente di Sviluppo
- Creazione del progetto **React** per il frontend.
- Configurazione di **Spring Boot** per il backend.
- Installazione e configurazione di **PostgreSQL** o **MySQL** per il database.
- Creazione della struttura delle tabelle: utenti, capi d'abbigliamento, outfit suggeriti.

### 3️⃣ Sviluppo del Backend
- Creazione delle API REST per gestire autenticazione, gestione utenti, capi d'abbigliamento e outfit.
- Implementazione dell'autenticazione con **JWT (JSON Web Token)**.
- Configurazione della sicurezza dell'API.

### 4️⃣ Sviluppo del Frontend
- Creazione dell'interfaccia utente con **React e Bootstrap CSS**.
- Implementazione della dashboard utente per il caricamento e la gestione dei capi.
- Comunicazione con il backend tramite **Fetch API**.

### 5️⃣ Integrazione dell'Intelligenza Artificiale
- Utilizzo di **Gemma-AI** tramite Hugging Face  per suggerire outfit basati sul guardaroba dell'utente.
- Configurazione delle API per ottenere suggerimenti personalizzati.

### 6️⃣ Ottimizzazione e Test
- Verifica del corretto funzionamento del sistema con test unitari e di integrazione.
- Ottimizzazione delle prestazioni per garantire un'app fluida.

### 7️⃣ Manutenzione e Aggiornamenti
- Monitoraggio dell'applicazione per individuare miglioramenti.
- Raccolta feedback dagli utenti per aggiungere nuove funzionalità.

---

## 🛠️ Configurazione del Progetto

### 📂 Clonare il Repository
```bash
git clone https://github.com/antgian96/provafinalekloset
cd kloset-app
```

### 📦 Installazione delle Dipendenze
#### 🔹 Backend (Spring Boot)
Assicurati di avere **Java 17+** e **Maven** installati, quindi esegui:
```bash
cd backend
mvn clean install
mvn spring-boot:run
```

#### 🔹 Frontend (React)
Assicurati di avere **Node.js 16+**, quindi esegui:
```bash
cd frontend
npm install
npm start
```

---

## 🔐 Configurazione del Token Hugging Face
Per utilizzare le API di Hugging Face per il suggerimento degli outfit, imposta il tuo **token API** come variabile d'ambiente:

### Su macOS/Linux:
```bash
export HF_TOKEN="il_tuo_token"
```

### Su Windows (PowerShell):
```powershell
[System.Environment]::SetEnvironmentVariable("HF_TOKEN", "il_tuo_token", "User")
```

### Usare un File `.env`
Se preferisci, crea un file `.env` nella root del progetto **frontend e backend** con il seguente contenuto:
```env
HF_TOKEN=il_tuo_token
```
📌 **Importante:** Assicurati di **aggiungere `.env` a `.gitignore`** per evitare che venga caricato su GitHub.

---

## 📌 API Endpoints Principali
| Metodo | Endpoint | Descrizione |
|--------|------------|-------------|
| POST | `/api/auth/register` | Registra un nuovo utente |
| POST | `/api/auth/login` | Effettua il login e restituisce il token JWT |
| POST | `/api/outfit/add` | Aggiunge un nuovo outfit salvato dall'utente |
| GET | `/api/outfit/user` | Ottiene la lista degli outfit salvati dall'utente |
| POST | `/api/outfit/suggest` | Richiede un suggerimento outfit basato sui capi salvati |

---

## 💡 Contribuire al Progetto
Se vuoi contribuire:
1. **Forka** il repository.
2. Crea un nuovo branch: `git checkout -b feature-nuova-funzionalita`.
3. Aggiungi le tue modifiche e fai commit: `git commit -m "Aggiunta nuova funzionalità"`.
4. Effettua un push: `git push origin feature-nuova-funzionalita`.
5. Apri una **Pull Request** su GitHub.

---

## 📜 Licenza
Questo progetto è rilasciato sotto la licenza **MIT**.

📌 Per eventuali domande, contattami su **[GitHub](https://github.com/antgian96)**. 🚀

