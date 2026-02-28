# Základní principy a struktura HTML

## 1) Co je HTML

HTML (HyperText Markup Language) je značkovací jazyk používaný pro tvorbu webových stránek.  
Není to programovací jazyk – neobsahuje podmínky ani cykly. Slouží ke strukturování obsahu (text, obrázky, odkazy, formuláře).

HTML určuje:
- co je nadpis
- co je odstavec
- co je seznam
- co je odkaz
- kde je obrázek

O vzhled se stará CSS a o interaktivitu JavaScript.

---

## 2) Historie HTML

HTML vytvořil v roce 1991 Tim Berners-Lee, zakladatel World Wide Webu.

Vývoj verzí:
- HTML 1.0 (1991)
- HTML 4.01 (1999)
- XHTML
- HTML5 (2014 – současný standard)

HTML5 přineslo nové sémantické prvky a podporu multimédií.

---

## 3) Základní struktura HTML dokumentu

Každý HTML dokument má pevnou strukturu:

```html
<!DOCTYPE html>
<html lang="cs">
<head>
    <meta charset="UTF-8">
    <meta name="description" content="Ukázková stránka">
    <meta name="author" content="Jméno">
    <title>Základní struktura HTML</title>
</head>
<body>

    <header>
        <h1>Hlavní nadpis stránky</h1>
        <nav>
            <a href="#sekce1">Sekce 1</a>
            <a href="#sekce2">Sekce 2</a>
        </nav>
    </header>

    <section id="sekce1">
        <h2>Textové prvky</h2>
        <p>Toto je odstavec textu.</p>
        <p><strong>Tučný text</strong> a <em>kurzíva</em>.</p>
        <br>
        <hr>
    </section>

    <section id="sekce2">
        <h2>Seznamy</h2>

        <h3>Neuspořádaný seznam</h3>
        <ul>
            <li>Položka 1</li>
            <li>Položka 2</li>
        </ul>

        <h3>Uspořádaný seznam</h3>
        <ol>
            <li>První</li>
            <li>Druhý</li>
        </ol>
    </section>

    <section>
        <h2>Odkazy a obrázky</h2>
        <a href="https://www.example.com" target="_blank">Externí odkaz</a>
        <br>
        <img src="obrazek.jpg" alt="Popis obrázku" width="300">
    </section>

    <section>
        <h2>Tabulka</h2>
        <table border="1">
            <tr>
                <th>Jméno</th>
                <th>Věk</th>
            </tr>
            <tr>
                <td>Jan</td>
                <td>18</td>
            </tr>
        </table>
    </section>

    <section>
        <h2>Formulář</h2>
        <form action="zpracovani.php" method="post">
            <label for="jmeno">Jméno:</label>
            <input type="text" id="jmeno" name="jmeno">

            <br><br>

            <label for="email">Email:</label>
            <input type="email" id="email" name="email">

            <br><br>

            <input type="submit" value="Odeslat">
        </form>
    </section>

    <aside>
        <p>Postranní informace</p>
    </aside>

    <footer>
        <p>&copy; 2026 Moje stránka</p>
    </footer>

</body>
</html>
```

---

## 4) Důležité pojmy k maturitě

- Tag (značka) – např. `<p>`
- Párová značka – má otevírací a uzavírací část
- Nepárová značka – např. `<br>`, `<img>`
- Atribut – doplňující informace (např. `href`, `src`)
- Sémantické prvky – header, nav, section, article, aside, footer
- Validace – kontrola správnosti HTML podle standardů W3C

---

## Shrnutí

HTML je základ webu.  
Slouží ke strukturování obsahu pomocí značek.  
Každý dokument má pevnou strukturu (DOCTYPE, html, head, body).  
Moderní HTML5 přináší sémantické prvky a multimédia.  

Bez HTML by neexistovaly webové stránky.
