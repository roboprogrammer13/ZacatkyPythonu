# Úkol 1 - Práce s listy v Pythonu 🐍

Vítej v prvním úkolu na GitHubu! Tento repozitář je **jen tvůj** - nikdo jiný z třídy ho nevidí.

## 📝 Zadání

Vytvoř program v Pythonu, který:
1. Vytvoří list s 5 čísly
2. Přidá do listu další číslo
3. Odstraní z listu první prvek
4. Vypíše délku listu
5. Vypíše celý list

**Bonus:** Vypočítej průměr všech čísel v listu.

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

**Můžeš použít, co chceš!** Pro tento úkol doporučuji notebook.

---

## ❓ Často kladené otázky

**Q: Vidí moji práci spolužáci?**  
A: Ne, tvůj repozitář je soukromý - vidí ho jen ty a učitelka.

**Q: Můžu odevzdat vícekrát?**  
A: Ano! Můžeš nahrávat nové verze kdykoliv před deadlinem.

**Q: Jak poznám, že jsem úkol odevzdal/a?**  
A: Na GitHubu uvidíš svůj soubor v repozitáři. GitHub notebook automaticky zobrazí s výstupy. Učitelka vidí čas poslední změny.

**Q: Co když mi git příkazy nefungují?**  
A: Použij způsob 1 (přímo z Colabu) nebo způsob 2 (nahrání přes web) - je úplně v pořádku!

**Q: Musím mít spuštěný notebook před odevzdáním?**  
A: Ano! Spusť všechny buňky (`Runtime` → `Run all` v Colabu), aby byly vidět výstupy.

**Q: Jak propojím Colab s GitHubem poprvé?**  
A: Při prvním `Save a copy in GitHub` tě Colab vyzve k autorizaci - stačí potvrdit.

---

## 🆘 Potřebuješ pomoc?

- Zkus se podívat na [GitHub dokumentaci](https://docs.github.com)
- Zeptej se spolužáka
- Napiš učitelce Issue v tomto repozitáři (záložka "Issues")

---

**Deadline:** *(doplní učitelka)*  
**Hodnocení:** *(doplní učitelka)*

Hodně štěstí! 🚀