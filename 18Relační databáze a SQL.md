# Relační databáze a SQL

## 1) Co je databáze

Databáze je **organizovaný soubor dat**, který umožňuje:
- ukládání dat
- vyhledávání dat
- úpravu dat
- mazání dat

Používá se například pro:
- e-shopy
- bankovní systémy
- školní informační systémy
- webové aplikace

---

## 2) Relační databáze

Relační databáze ukládá data do **tabulek (relací)**.

Každá tabulka obsahuje:
- sloupce (atributy)
- řádky (záznamy)

Příklad tabulky STUDENTI:

| id | jméno | věk |
|----|-------|-----|
| 1  | Jan   | 18  |
| 2  | Petra | 19  |

---

## 3) Základní pojmy

- Primární klíč (PRIMARY KEY) – jednoznačně identifikuje záznam
- Cizí klíč (FOREIGN KEY) – propojuje tabulky
- Atribut – sloupec
- Entita – objekt (např. student)
- Relace – vztah mezi tabulkami

---

## 4) Vztahy mezi tabulkami

### 1 : 1 (jedna ku jedné)
Např. osoba – občanský průkaz

### 1 : N (jedna ku mnoha)
Např. učitel – studenti

### M : N (mnoho ku mnoha)
Např. studenti – předměty  
(řeší se pomocí spojovací tabulky)

---

## 5) Co je SQL

SQL (Structured Query Language) je jazyk pro práci s databázemi.

Používá se pro:
- vytváření tabulek
- vkládání dat
- úpravu dat
- mazání dat
- dotazování (vyhledávání)

---

## 6) Základní SQL příkazy

### Vytvoření tabulky

```sql
CREATE TABLE studenti (
    id INT PRIMARY KEY,
    jmeno VARCHAR(50),
    vek INT
);
```

---

### Vložení dat

```sql
INSERT INTO studenti (id, jmeno, vek)
VALUES (1, 'Jan', 18);
```

---

### Výběr dat

```sql
SELECT * FROM studenti;
```

Výběr konkrétních sloupců:

```sql
SELECT jmeno, vek FROM studenti;
```

---

### Podmínka (WHERE)

```sql
SELECT * FROM studenti
WHERE vek > 18;
```

---

### Úprava dat

```sql
UPDATE studenti
SET vek = 19
WHERE id = 1;
```

---

### Mazání dat

```sql
DELETE FROM studenti
WHERE id = 1;
```

---

## 7) Spojování tabulek (JOIN)

Příklad dvou tabulek:
- studenti
- predmety

```sql
SELECT studenti.jmeno, predmety.nazev
FROM studenti
JOIN predmety
ON studenti.id = predmety.student_id;
```

JOIN umožňuje spojit data z více tabulek podle cizího klíče.

---

## 8) Agregační funkce

```sql
SELECT COUNT(*) FROM studenti;
SELECT AVG(vek) FROM studenti;
SELECT MAX(vek) FROM studenti;
SELECT MIN(vek) FROM studenti;
```

Používají se pro statistiku.

---

## 9) Výhody relačních databází

- přehledná struktura
- minimalizace duplicity dat
- integrita dat
- podpora vztahů
- rychlé vyhledávání

---

## 10) Shrnutí

Relační databáze ukládají data do tabulek propojených klíči.  
SQL je jazyk pro práci s těmito databázemi.  
Umožňuje vytvářet tabulky, upravovat data a provádět dotazy.  

Relační databáze jsou základem většiny moderních webových aplikací.
