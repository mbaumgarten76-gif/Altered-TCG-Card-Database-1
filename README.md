# 🧩 Altered TCG Card Database

## Goal
This project aims to gather all non unique cards from the **Altered** TCG in a community-driven repository,
in all available languages, without overloading the official servers with API requests.

Repeated API calls can trigger throttling or server overload.  
We therefore recommend using this local JSON database first before making HTTP requests.

---

## 📂 Folder Structure

Files are stored using the following path pattern :
```bash
./
├── SETS/                        # All sets grouped here
│ ├── CORE/                      # Set folder (set code as name)
│ │ ├── CORE_EN.json             # JSON file per language
│ │ └── ...
│ └── ...
│
├── META/                        # Metadata about cards & filters
│ ├── card_types.json
│ ├── card_sets.json
│ ├── filter_factions.json
│ ├── filter_rarities.json
│ └── ...
│
└── HISTORY/                     # English-only history of card changes
├── cards_history_CORE.json
├── cards_history_COREKS.json
└── ...
```

- **SETS/** → Contains all card data grouped by set code, each set has its own folder, and inside, one file per language.  
- **META/** → Contains only metadata (types, sets, factions, rarities, etc.).  
- **HISTORY/** → Contains versioned history of card changes (English only, per set).

---

## 🌍 Supported Languages
- English (`EN`)
- French (`FR`)
- Spanish (`ES`)
- Italian (`IT`)
- German (`DE`)

---

## 📜 Data Format
Each file inside `SETS/` contains the exact JSON structure returned by the official **Altered API**,  
with no modification to the schema (only separated by set and language).

---

## 📖 License
MIT License – feel free to use, share, and improve.  
Please credit the community and the Altered TCG project.  
