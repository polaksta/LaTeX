# Klasa `agh-wi`
Klasa LaTeX do prac dyplomowych na Wydziale Informatyki Akademii Górniczo-Hutniczej w Krakowie.

## Opis
Klasa `agh-wi` została stworzona, aby ułatwić studentom Wydziału Informatyki Akademii Górniczo-Hutniczej w Krakowie skład pracy dyplomowej w systemie LaTeX. Rozszerza ona klasę *scrbook*, która wchodzi w skład zestawu klas *KOMA-Script*, oferującego europejskie zasady typografii.

Użytkownik może określić trzy parametry:
1. Język pracy dyplomowej.
2. Nazwa kierunku studiów.
3. Czy praca jest przeznaczona do wyświetlania na ekranie, czy drukowania?

Wartościami domyślnymi, tych parametrów, są, odpowiednio, *język polski*, *Informatyka* oraz *praca będzie oglądana na ekranie*.

Szczegóły użycia klasy można znaleźć w pliku `agh-wi.pdf`.

## Opcje
- **english** — praca dyplomowa jest po angielsku.
     - Teksty wstawiane automatycznie przez LaTeX (spis treści, spis rysunków itp.) są w języku angielskim.
     - Zasady dzielenia wyrazów dotyczą języka angielskiego.
     - ***Strona tytułowa jest po polsku***, ale najpierw jest widoczny angielskojęzyczny tytuł, a potem polskojęzyczny.
- **data-science** — praca dyplomowa na kierunku „Informatyka — Data Science”.
- **print** — praca dyplomowa będzie drukowana i w związku z tym na każdej stronie powinien być dodany, dodatkowy (2 cm), margines na oprawę.

### Przykłady
1. `\documentclass{agh-wi}` — Treść pracy jest w języku polskim, a na stronie tytułowej jako kierunek studiów należy umieścić napis *Informatyka*. Praca jest przeznaczona do wyświetlania (za pomocą przeglądarki PDF).
2. `\documentclass[english]{agh-wi}` — Treść pracy jest w języku angielskim, a na stronie tytułowej jako kierunek studiów należy umieścić napis *Informatyka*. Praca jest przeznaczona do wyświetlania.
3. `\documentclass[print]{agh-wi}` — Treść pracy jest w języku polskim, na stronie tytułowej jako kierunek studiów należy umieścić napis *Informatyka*. Praca będzie drukowana, a następnie oprawiana.
4. `\documentclass[english, data-science, print]{agh-wi}` — Treść pracy jest w języku angielskim, na stronie tytułowej jako kierunek studiów należy umieścić napis *Informatyka  — Data Science*. Praca będzie drukowana, a następnie oprawiana.

Możesz także używać opcji opisanych w [Podręczniku KOMA-Script](http://mirrors.ctan.org/macros/latex/contrib/koma-script/doc/scrguide-en.pdf).

## Instalacja
Uruchom komendę

```
$ pdflatex agh-wi.dtx
```
do wygenerowania plików `.ins`, `.cls`, `.pdf`, `example.tex` oraz `bibliography.bib`. 

Aby poprawnie wygenerować historię zmian oraz indeks dla dokumentacji klasy, należy uruchomić

```
$ makeindex -s gind.ist agh-wi
$ makeindex -s gglo.ist -o agh-wi.gls agh-wi.glo
$ pdflatex agh-wi.dtx
$ pdflatex agh-wi.dtx
```

(Twoje środowisko TeX może to wykonać za ciebie).

Na koniec, aby użyć wygenerowanego pliku `.cls`, przenieś go do odpowiedniej lokalizacji dla swojej dystrybucji TeX-a. Być może najłatwiejszym sposobem, aby to osiągnąć, jest wykonanie komendy

```
$ mv agh-wi.cls $(kpsewhich -var-value=TEXMFHOME)/tex/latex
```

Jeżeli chcesz udostępnić plik wszystkim użytkownikom urządzenia z systemem Unix, prawdopodobnie lepiej będzie, jak skopiujesz go do katalogu `/usr/local/texlive/texmf-local/tex/latex`, a następnie uruchomisz

```
# texhash
```

Aby mieć pewność, że instalacja się powiodła, wykonaj polecenie

```
$ kpsewhich agh-wi.cls
```
Jeśli wynikiem jest ścieżka do pliku, to znaczy, że poprawnie zainstalowałeś/aś klasę.

## Przykładowa praca dyplomowa
Ze względu na trudności związane z dostarczaniem przykładów użycia komend oraz środowisk w dokumentacji klasy, są one pokazane w oddzielnym pliku — `example.tex` — zawiera on jednocześnie przykładową pracę dyplomową. Możesz go więc potraktować jako szablon do utworzenia własnej pracy.

Aby otrzymać wynikowy dokument PDF, należy skompilować dokument źródłowy za pomocą sekwencji komend:
```
$ pdflatex -shell-escape example
$ biber example
$ makeindex example.nlo  -s nomencl.ist -o example.nls
$ pdflatex -shell-escape example
$ pdflatex -shell-escape example
```
