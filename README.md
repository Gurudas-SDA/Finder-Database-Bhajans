# 🕉️ Chaitanya Academy - Multi-App Platform

Šī ir apvienota aplikācija ar trim dažādām funkcionalitātēm:
1. **Verse Finder** - Gauḍīya Vaiṣṇava pantu meklētājs
2. **Writings Database** - Chaitanya Academy rakstu datubāze
3. **Bhajan Search** - Bhajanu meklētājs un pārlūks

## 📋 Prasības

- Python 3.8 vai jaunāks
- pip (Python package manager)

## 🚀 Instalācija un palaišana

### 1. Lejupielādējiet failus

Jums nepieciešami šie faili:
- `app.py` (galvenā aplikācija ar visām trim lapām)
- `250928Versebase_app.xlsx` (pantu datubāze - **OBLIGĀTI**)
- `Bhajans.xlsx` (bhajanu datubāze - **OBLIGĀTI**)
- `requirements.txt` (Python bibliotēku saraksts)

### 2. Instalējiet nepieciešamās bibliotēkas

```bash
pip install -r requirements.txt
```

Vai manuāli:
```bash
pip install streamlit pandas openpyxl rapidfuzz
```

### 3. Pārliecinieties par failu struktūru

Failu struktūrai jābūt:
```
chaitanya-academy/
├── app.py
├── 250928Versebase_app.xlsx    # Pantu datubāze (OBLIGĀTI)
├── Bhajans.xlsx                 # Bhajanu datubāze (OBLIGĀTI)
├── requirements.txt
└── README.md
```

**⚠️ SVARĪGI: Abi Excel faili ir obligāti! Bez tiem aplikācija nestrādās.**

### 4. Palaidiet aplikāciju

```bash
streamlit run app.py
```

### 5. Atveriet aplikāciju

Aplikācija atvērsies jūsu pārlūkprogrammā adresē: `http://localhost:8501`

## 📱 Aplikācijas funkcionalitātes

### 🔍 Verse Finder
- Meklē pantus pēc fragmentiem
- Fuzzy search ar līdzības procentu
- Highlight meklētajam fragmentam
- Divkolonnu avotu saraksts
- Tulkojumi angļu valodā
- **Settings:**
  - Max verse number (5-50)
  - Min similarity % (10-80%)

### 📚 Writings Database
- Pārlūko pantus pēc avotiem
- Filtrē pēc Category un Original Source
- Sakārtoti pēc NR kolonnas
- Papildu metadati (Type, Description, Essence)
- **Settings:**
  - Max verse number (1-50)

### 🕉️ Bhajan Search
- Pārlūko bhajanus pēc:
  - Nosaukuma (A-Z)
  - Kategorijas
  - Autora
- Pārslēgšanās starp oriģinālu un tulkojumu
- Mobilajām ierīcēm draudzīgs dizains
- **Nekādi settings nav vajadzīgi**

## 📊 Excel failu formāti

### Verse Database (250928Versebase_app.xlsx)

Kolonnas:
- NR - Numurs
- IAST Verse - Panta teksts
- Original Source - Oriģinālais avots
- Author - Autors
- Context - Konteksts
- Translation - Tulkojums angļu valodā
- Cited In - Citēts tajā
- Type - Tips
- Description - Apraksts
- Essence by Gemini 2.5 Pro - Būtība

### Bhajan Database (Bhajans.xlsx)

Kolonnas:
- Category - Kategorija
- Bhajan_Title - Nosaukums
- Author - Autors
- Verse_Number - Panta numurs
- Original - Oriģinālais teksts
- English - Tulkojums angļu valodā

## 🌐 Streamlit Community Cloud izvietošana

### 1. Izveidojiet GitHub repozitoriju
1. Dodieties uz [github.com](https://github.com) 
2. Izveidojiet jaunu public repozitoriju
3. Augšupielādējiet **VISUS** failus:
   - `app.py`
   - `250928Versebase_app.xlsx` (**OBLIGĀTI**)
   - `Bhajans.xlsx` (**OBLIGĀTI**)
   - `requirements.txt`
   - `README.md`

### 2. Izvietojiet Streamlit Community Cloud
1. Dodieties uz [share.streamlit.io](https://share.streamlit.io)
2. Piesakieties ar GitHub kontu
3. Izveidojiet jaunu aplikāciju:
   - **Repository:** `jūsu-lietotājvārds/chaitanya-academy`
   - **Branch:** `main`  
   - **Main file path:** `app.py`
4. Nospiediet "Deploy!"

### 3. Rezultāts
Jūs iegūsiet publisko URL: `https://jūsu-app.streamlit.app`

## 🎯 Lietošana

1. **Atveriet aplikāciju** - palaižot streamlit vai atverot web URL
2. **Izvēlieties lapu** - sidebar kreisajā pusē ir radio pogas:
   - Verse Finder
   - Writings Database
   - Bhajan Search
3. **Izmantojiet izvēlēto funkcionalitāti** - katra lapa saglabā savas settings

## ⚙️ Navigācija

- **Sidebar kreisajā pusē** - radio pogas lapu pārslēgšanai
- Katra lapa ir pilnīgi neatkarīga ar saviem settings
- Pārslēdzoties uz citu lapu, settings netiek zaudēti

## 🔧 Pielāgošana

### Dizaina maiņa
CSS stili ir definēti `app.py` failā. Varat pielāgot:
- Krāsas
- Fontus
- Izkārtojumu
- Atstarpes

### Jaunu datu pievienošana
1. Atveriet attiecīgo Excel failu
2. Pievienojiet jaunas rindas
3. Saglabājiet failu
4. Ja izmantojat GitHub, augšupielādējiet atjaunināto failu
5. Streamlit automātiski atjauninās aplikāciju

## ⚠️ Svarīgi

1. **Excel failu nosaukumi:**
   - `250928Versebase_app.xlsx` - **OBLIGĀTI** (Verse Finder un Writings Database)
   - `Bhajans.xlsx` - **OBLIGĀTI** (Bhajan Search)
2. **Abi Excel faili ir nepieciešami** - bez tiem aplikācija nestrādās!
3. **Kolonnu nosaukumi:** Izmantojiet tieši tos pašus nosaukumus
4. **Failu izvietojums:** Visi faili jābūt vienā mapē
5. **Encoding:** Excel faili jābūt UTF-8 formātā

## 📞 Problēmu risināšana

### Aplikācija nesākas
```bash
# Pārbaudiet Python versiju
python --version

# Pārinstalējiet bibliotēkas
pip install --upgrade streamlit pandas openpyxl rapidfuzz
```

### Excel fails netiek atrasts
- Pārliecinieties, ka Excel faili ir tajā pašā mapē kā `app.py`
- Pārbaudiet failu nosaukumus (lieto/mazie burti ir svarīgi)

### Dati neparādās pareizi
- Atveriet Excel failu un pārbaudiet kolonnu nosaukumus
- Pārliecinieties, ka nav tukšu rindu starp datiem
- Pārbaudiet, vai fails ir UTF-8 encoding

### Sidebar neparādās
- Nospiediet `>` ikonu lapas augšējā kreisajā stūrī
- Vai izmantojiet tastatūras īsceļu

## 🙏 Pateicības

Šī aplikācija ir veidota, lai palīdzētu Gauḍīya Vaiṣṇava kopienu dalīties un meklēt svētās dziesmas, mantras un rakstus. 

**Hare Kṛṣṇa! 🕉️**

---

## 📝 Versiju vēsture

### v1.0.0 - Sākotnējā versija
- Verse Finder funkcionalitāte
- Writings Database funkcionalitāte
- Bhajan Search funkcionalitāte
- Apvienota navigācija ar sidebar radio pogām
