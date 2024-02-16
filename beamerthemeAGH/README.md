# Pakiet `beamerthemeAGH`
Motyw `AGH` dla prezentacji LaTeX Beamer.
## Opis
Pakiet `beamerthemeAGH` dostarcza szablonu prezentacji LaTeX Beamer opartego na jednym z oficjalnych [szablonów AGH](http://www.agh.edu.pl/uczelnia/system-identyfikacji-wizualnej/szablon-prezentacji/) dla PowerPoint-a.

Aby go użyć, umieść w preambule swojego dokumentu komendę `\usetheme{AGH}`. Szczegóły użycia pakietu można znaleźć w pliku `beamerthemeAGH.pdf`.
## Opcje
### Opcja `parttitle`
Na podstawie własnego doświadczenia mogę stwierdzić, że podział dużych prezentacji (np. wykłady) na części, jest bardzo wskazany. Jeżeli za pomocą komendy `\part`, podzieliłeś/aś swoją prezentację na części, to za pomocą opcji *parttitle* możesz spowodować, aby tytuł części był widoczny na slajdzie.
#### Przykłady
-  `\usetheme[parttitle=leftfooter]{AGH}` — umieść tytuł części w lewej stopce (zamiast nazw autora oraz instytutu).

-  `\usetheme[parttitle=rightfooter]{AGH}` — umieść tytuł części w prawej stopce (zamiast daty).
### Opcja `dark`
Jeżeli prezentacja będzie się odbywać w zaciemnionej sali, to przydatne może być użycie ciemnego tła — w takim przypadku użyj opcji *dark*, tj. `\usetheme[dark]{AGH}`.

Możesz określić, jak bardzo ciemne ma być tło, przypisując (tej opcji) wartość całkowitą z przedziału od 50 do 90, np. `\usetheme[dark=75]{AGH}`. Domyślną wartością jest 50.
### Opcja `nosidebar`
Jeżeli chcesz ukryć pasek boczny (zawierający logo AGH plus trójkolorowy pasek) dla slajdów nietytułowych, to użyj opcji *nosidebar*, tzn. `\usetheme[nosidebar]{AGH}`.
### Opcja `margins`
Domyślny rozmiar lewego i prawego marginesu obszaru tekstu wynosi 4em. Jeżeli chcesz ustawić inną wartość, to użyj opcji *margins*, przypisując jej żądaną wartość marginesu, np. `\usetheme[margins=1em]{AGH}`.
## Wersje kolorystyczne
| Domyślna | Z ciemnym tłem |
|--------------------|----------------------------------|
| ![Screenshot](http://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH.big.png "Slajd tytułowy") | ![Screenshot](http://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH-dark.big.png "Slajd tytułowy — wersja ciemna") |

*Symbol graficzny AGH jest zastrzeżony i bez zezwolenia, nie powinien być stosowany przez osoby i instytucje niezwiązane z AGH.*
## Przykładowe prezentacje
* [Prezentacja 1](http://www.icsr.agh.edu.pl/~polak/beamer.pdf)
* [Prezentacja 2](http://www.icsr.agh.edu.pl/~polak/wms/beamer.pdf)
* [Prezentacja 3 — wersja z ciemnym tłem](http://www.icsr.agh.edu.pl/~polak/wms/latex/beamer-mozliwosci.pdf)

Jeżeli powyższe przykłady przekonały Cię, że warto tworzyć prezentacje w oparciu o LaTeX Beamer, a ... nie wiesz, jak się do tego zabrać, to polecam Ci [mój kanał na youtube](https://www.youtube.com/playlist?list=PLlOvf-mh5wJEzL2onjzBdenUpssbonmO5). :smile:
## Instalacja

Uruchom komendę
```
$ pdflatex beamerthemeAGH.dtx
```
do wygenerowania plików `.ins`, `.sty`, `.pdf` oraz `example.tex`.

Aby poprawnie wygenerować historię zmian oraz indeks dla dokumentacji klasy, należy uruchomić
```
$ makeindex -s gind.ist beamerthemeAGH
$ makeindex -s gglo.ist -o beamerthemeAGH.gls beamerthemeAGH.glo
$ pdflatex beamerthemeAGH.dtx
```
(Twoje środowisko TeX może to wykonać za ciebie).

  
Na koniec, aby użyć wygenerowanych plików `.sty`, przenieś je do odpowiedniej lokalizacji dla swojej dystrybucji TeX-a. Być może najłatwiejszym sposobem, aby to osiągnąć, jest wykonanie komendy
```
$ mv *.sty $(kpsewhich -var-value=TEXMFHOME)/tex/latex
```

Jeżeli chcesz udostępnić plik wszystkim użytkownikom urządzenia z systemem Unix, prawdopodobnie lepiej będzie, jak skopiujesz go do katalogu `/usr/local/texlive/texmf-local/tex/latex`, a następnie uruchomisz
```
# texhash
```
Aby mieć pewność, że instalacja się powiodła, wykonaj polecenie
```

$ kpsewhich beamercolorthemeAGH.sty beamerthemeAGH.sty

```
Jeśli wynikiem jest ścieżka do pliku, to znaczy, że poprawnie zainstalowałeś/aś klasę.

 
## Szablon przykładowej prezentacji

Ze względu na trudności związane z dostarczaniem przykładów użycia komend oraz środowisk w dokumentacji klasy, są one pokazane w oddzielnym pliku — `example.tex` — zawiera on jednocześnie przykładową prezentację. Możesz ją więc potraktować jako szablon do utworzenia własnej prezentacji.

Aby otrzymać wynikowy dokument PDF, należy skompilować dokument źródłowy za pomocą  komendy:
```
pdflatex -shell-escape example
```
