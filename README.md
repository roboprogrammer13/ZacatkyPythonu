# 18. 12. 🐍 Grafika v Pythonu: ColabTurtle & Vibecoding

Tento manuál vám pomůže rozběhnout grafické kreslení v prostředí Google Colab. Protože v cloudu nemáme běžný monitor, musíme použít speciální knihovnu **ColabTurtle**.

## 1. Příprava prostředí (Setup)
Aby nám želva fungovala, musíme do **každého nového notebooku** na začátek vložit tyto dva kroky.

**Krok A: Instalace** (spusťte tuto buňku jako první)
```python
!pip install ColabTurtle
```

**Krok B: Spuštění** (toto musí být na začátku vašeho kódu)
```python
from ColabTurtle.Turtle import *
#initializeTurtle()  # window?size = (800,500)
initializeTurtle(initial_speed=5,initial_window_size=(500,200)) # 13 je maximální rychlost
```

---

## 2. Tahák příkazů (Cheat Sheet)
Zde je seznam příkazů, které `ColabTurtle` umí. Pozor: Neumí všechno co klasická želva (např. neumí `circle`).

| Příkaz | Příklad | Co to udělá |
| :--- | :--- | :--- |
| **Pohyb** | | |
| `forward(číslo)` | `forward(100)` | Jde dopředu o X pixelů. |
| `backward(číslo)` | `backward(50)` | Couvá o X pixelů. |
| `left(úhel)` | `left(90)` | Otočí se doleva o X stupňů. |
| `right(úhel)` | `right(45)` | Otočí se doprava o X stupňů. |
| `getx()` | `gety()` | Vrátí souřadnice želvy.|
| `setheading(úhel)` | `setheading(45)` | Otočí od východního směru. |
| **Vzhled** | | |
| `penup()` | `penup()` | Zvedne pero (nekreslí při pohybu). |
| `pendown()` | `pendown()` | Položí pero (začne kreslit). |
| `color('barva')` | `color('cyan')` | Změní barvu čáry (red, blue, white, cyan, magenta...). |
| `width(číslo)` | `width(5)` | Změní tloušťku čáry. |
| `bgcolor('barva')` | `bgcolor('black')` | Změní barvu pozadí celého plátna. |
| **Ostatní** | | |
| `goto(x, y)` | `goto(100, 200)` | Skočí na konkrétní souřadnice. |
| `speed(číslo)` | `speed(10)` | Rychlost kreslení (1 = pomalu, 13 = max). |

---

## 3. První pokus: Základní čtverec
Vyzkoušejte si, zda vše funguje. Tento kód nakreslí jednoduchý čtverec.

```python
from ColabTurtle.Turtle import *
initializeTurtle()

color('orange')
width(3)

# Opakuj 4x pro čtverec
for _ in range(4):
    forward(150)
    left(90)

## 4. Vibecoding: Pokročilé příklady
Vibecoding je o stylu. Používáme černé pozadí, zajímavá barevná schémata a matematickou symetrii. Zkuste se inspirovat matematickými  vzory.

### Vzor A: The Digital Pulse (Digitální puls)
Tento příklad využívá trik se změnou tloušťky čáry (`width`) během kreslení. Vypadá to, jako by obrazec dýchal nebo pulzoval.

**Vysvětlení kódu:**
*   Používáme úhel `59` stupňů (ne 60). Díky tomu se trojúhelníky nikdy přesně nepotkají a vznikne chaos.
*   `width(i % 10 + 1)` neustále mění tloušťku čáry od 1 do 10.

```python
from ColabTurtle.Turtle import *

initializeTurtle(initial_speed=13)
bgcolor('black') # Základ pro vibe
colors = ['cyan', 'blue', 'white']

for i in range(120):
    color(colors[i % 3])    # Střídání 3 barev
    width(i % 10 + 1)       # Mění tloušťku čáry (Puls efekt)
    
    forward(i * 3)          # Stále delší čáry
    left(59)                # Nepravidelný úhel rotace


---



---
# 4. 12. Práce s listy v Pythonu 🐍

## 📝 Zadání

S pomocí generativního AI chatbotu (Claude), GitHub Copilot, ChatGPT, Gemini ) vytvořte seznam s vnořeným seznamem, řetězcem nebo tuple, např. seznam tramvají z Prahy ve formátu: (typ, maximální_rychlost_km_h, rok_první_výroby) a databázi smysluplným způsobem zpracujte:

filtrování seznamu, řazení podle různých atributů, výpočet popisných statistik, grafická reprezentace - histogram.

**Inspirace pro tvorbu datasetu:**

* největší města světa (název, počet obyvatel, kontinent)
* státy (název, rozloha, počet obyvatel, hlavní město)
* pražské tramvajové tratě (číslo linky, délka tratě, rok vzniku)
* evropské řeky (název, délka, země, do které ústí)
* filmové databáze (název filmu, rok vydání, hodnocení)
* sporty (název, počet hráčů, olympijský/neolympijský)


**Formát odevzdání:** Jupyter notebook (`.ipynb`) nebo Python soubor (`.py`)

## 📂 Jak odevzdat

Můžeš použít **tři způsoby** - vyber si, který ti vyhovuje!

---

### 🚀 ZPŮSOB 1: Přímo z Google Colabu (nejrychlejší!)

**První nastavení** (uděláš jen jednou):
1. V Colabu otevři: `File` → `Save a copy in GitHub`
2. Colab si vyžádá **přístup k GitHubu** - klikni "Authorize"
3. Potvrď přístup

**Odevzdání úkolu:**
1. Pracuj na svém notebooku v Colabu
2. Klikni: `File` → `Save a copy in GitHub`
3. V dialogu vyber:
   - **Repository:** `nazev-tvoje-organizace/ukol-1-tvoje-jmeno`
   - **File path:** `ukol_listy.ipynb` (nebo ponech původní název)
   - **Commit message:** "Odevzdání úkolu - práce s listy"
4. Klikni **OK**

✅ Hotovo! Tvůj notebook je automaticky na GitHubu.

**Tip:** Každou další změnu uložíš stejně - Colab přepíše starší verzi.

---

### 🖱️ ZPŮSOB 2: Stažení a nahrání přes web

**Z Google Colabu:**
1. V Colabu: `File` → `Download` → `Download .ipynb`
2. Ulož soubor jako `ukol_listy.ipynb`

**Z VS Code:**
3. Ulož notebook jako `ukol_listy.ipynb`

**Nahrání na GitHub:**
4. Otevři tento repozitář na GitHubu (kde právě čteš tenhle text)
5. Klikni na **"Add file"** → **"Upload files"**
6. Přetáhni svůj soubor `ukol_listy.ipynb` do okna
7. Dole napiš krátkou zprávu (např. "Odevzdání úkolu")
8. Klikni **"Commit changes"**

✅ Hotovo! Tvůj notebook je odevzdaný a GitHub ho pěkně zobrazí.

---

### 💻 ZPŮSOB 3: Pomocí git příkazů (pokročilejší)

Tento způsob se hodí, pokud chceš pracovat rychleji a profesionálněji.

#### A) První nastavení (uděláš jen jednou)

**1. Nainstaluj Git:**
- Windows: [git-scm.com](https://git-scm.com)
- Mac: už máš nainstalovaný
- Linux: `sudo apt install git`

**2. Nastav své jméno a email** (otevři terminál/příkazový řádek):
```bash
git config --global user.name "Tvoje Jméno"
git config --global user.email "tvuj@email.cz"
```

**3. Naklonuj repozitář** (stáhni ho k sobě do počítače):
```bash
git clone https://github.com/tvoje-organizace/ukol-1-tvoje-jmeno.git
cd ukol-1-tvoje-jmeno
```

*(URL najdeš na GitHubu pod zeleným tlačítkem "Code")*

#### B) Práce na úkolu

**4. Vytvoř nebo zkopíruj svůj soubor:**
- Z Google Colabu: stáhni `.ipynb` soubor a přesuň ho do složky repozitáře
- Ve VS Code: otevři složku repozitáře a vytvoř notebook přímo tam

**5. Nahraj změny na GitHub:**
```bash
git add ukol_listy.ipynb
git commit -m "Odevzdání úkolu - práce s listy"
git push
```

**Co dělají tyto příkazy:**
- `git add` = připrav soubor k nahrání
- `git commit` = ulož změnu se zprávou
- `git push` = pošli to na GitHub

✅ Hotovo! Tvůj notebook je na GitHubu.

#### C) Pokud děláš změny později

Už máš repozitář naklonovaný, stačí:
```bash
git add .
git commit -m "Oprava a vylepšení"
git push
```

---

### 🎯 VS Code - ještě jednodušší způsob

Pokud pracuješ ve VS Code s notebooky, nemusíš psát příkazy! Můžeš použít grafické rozhraní:

1. **Otevři složku repozitáře** ve VS Code
2. Vytvoř/uprav soubor `ukol_listy.ipynb`
3. V levém menu klikni na **Source Control** (ikona větvičky)
4. Uvidíš změněné soubory - klikni na **"+"** u souboru (staging)
5. Nahoře napiš zprávu (např. "Odevzdání úkolu")
6. Klikni na **✓ Commit**
7. Klikni na **"..."** → **Push**

---

## 📓 Jupyter Notebook vs Python soubor

**Jupyter Notebook (.ipynb):**
- ✅ Vidíš výstupy přímo v GitHubu
- ✅ Můžeš přidat markdown buňky s vysvětlením
- ✅ Ideální pro dokumentaci postupu
- ✅ Funguje skvěle s Google Colabem

**Python soubor (.py):**
- ✅ Jednodušší, čistý kód
- ✅ Menší velikost souboru
- ✅ Vhodný pro skripty bez výstupů

---

## 🆘 Potřebuješ pomoc?

- Zkus se podívat na [GitHub dokumentaci](https://docs.github.com)



## sdílení pro studenty
Klikněte na Settings → Manage access (nebo "Access" / "Manage access").
Klikněte na "Invite a collaborator" / "Invite teams" a zadejte GitHub uživatelské jméno nebo e‑mail.
