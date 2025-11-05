# <img src="https://www.altered.gg/apple-touch-icon.png" width="32" alt="Altered.gg Logo"/> Altered TCG Card Database

## 🎯 Goal
This project aims to provide a **community-driven repository** of all **Common and Rare** (non-unique) cards from the **Altered TCG**, available in all supported languages.

The purpose is to reduce unnecessary load on the official Altered API servers.  
Since repeated API calls may trigger throttling or overload, we recommend using this local JSON database first before sending new HTTP requests to the official API.

---

## 📂 Folder Structure

Files are stored using the following path pattern :
```bash
./
├── CARDS/                           # All cards grouped here
│ ├── EN/                            # Cards language folder
│ │ ├── CORE/                        # Set folder (set code as name)
│ │ │ ├── AX/                        # Faction folder (faction code as name)
│ │ │ │ ├── ALT_CORE_A_AX_22_C.json  # JSON file per card
│ │ │ │ └── ...
│ │ │ └── ...
│ │ └── ...
│ └── ...
│
├── SETS/                            # All sets grouped here
│ ├── CORE/                          # Set folder (set code as name)
│ │ ├── CORE_EN.json                 # JSON file per language
│ │ └── ...
│ └── ...
│
├── META/                            # Metadata about cards & filters
│ ├── card_sets_en.json
│ ├── filter_data_en.json
│ └── ...
│
├── HISTORY/                         # English-only history of card changes
│ ├── cards_history_CORE.json
│ └── ...
└── ...
```

- **CARDS** → Contains all individual card files, grouped by language, then by set code, then by faction code.
- **SETS** → Contains all card data grouped by set code, each set has its own folder, and inside, one file per language.  
- **META** → Contains only metadata (types, sets, factions, rarities, etc.).  
- **HISTORY** → Contains versioned history of card changes (English only, per set).

---

## 🌍 Supported Languages
- English (`EN`)
- French (`FR`)
- Spanish (`ES`)
- Italian (`IT`)
- German (`DE`)

---

## 📜 Data Format
Each file inside `SETS/` and `CARDS/` contains the exact JSON structure returned by the official **Altered API**, with no modification to the schema (only separated by set and language).
The only manually added information is the collectorNumber, which is no longer present in the JSON data returned by the API.

---

## 🖼️ Card Images
Card images are available here : https://drive.google.com/drive/folders/1cVqqV2HCRXk9PtipW144H-i7ObmG9TXy?usp=sharing

---

## 📖 License
MIT License – feel free to use, share, and improve.  
Please credit the community and the Altered TCG project.  
