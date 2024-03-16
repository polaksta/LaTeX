# Pakiet `beamerthemeAGH`
Motyw `AGH` dla prezentacji LaTeX Beamer.
## Opis
Pakiet `beamerthemeAGH` dostarcza szablonu prezentacji LaTeX Beamer opartego na jednym z oficjalnych [szablonów AGH](http://www.agh.edu.pl/uczelnia/system-identyfikacji-wizualnej/szablon-prezentacji/) dla PowerPoint-a.

Aby go użyć, umieść w preambule swojego dokumentu komendę `\usetheme{AGH}`. Szczegóły użycia pakietu można znaleźć w pliku `beamerthemeAGH.pdf`.
## Opcje
### Opcja `dark`
Jeżeli prezentacja będzie się odbywać w zaciemnionej sali, to przydatne może być użycie ciemnego tła — w takim przypadku użyj opcji _dark_, tj.  `\usetheme[dark]{AGH}`.

Możesz określić, jak bardzo ciemne ma być tło, przypisując (tej opcji) wartość całkowitą z przedziału od 50 do 90, np. `\usetheme[dark=75]{AGH}`. Domyślną wartością jest 50.
### Opcja `nosidebar`
Jeżeli chcesz ukryć pasek boczny (zawierający logo AGH plus trójkolorowy pasek) dla slajdów nietytułowych, to użyj opcji _nosidebar_, tzn.  `\usetheme[nosidebar]{AGH}`.
### Opcja `margins`
Domyślny rozmiar lewego i prawego marginesu obszaru tekstu wynosi 4em. Jeżeli chcesz ustawić inną wartość, to użyj opcji _margins_, przypisując jej żądaną wartość marginesu, np. `\usetheme[margins=1em]{AGH}`.
### Opcja `outertheme`
Domyślnie używanym motywem zewnętrznym jest **infolines**. Jeżeli chcesz użyć innego, to jego nazwę musisz wyspecyfikować jako wartość opcji _outertheme_, np.  `\usetheme[outertheme=sidebar]{AGH}`. 
| Nazwa motywu | Opis | Zrzut ekranu |
| --------   | ------- |------- |
| default    | Stonowany i minimalistyczny motyw. Tytuł slajdu jest równany do lewej strony. Slajd nie posiada ani nagłówka, ani stopki. | ![Screenshot](https://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH-default.png "Slajd") |
| infolines  | Nagłówek zawiera tytuł bieżącej sekcji oraz podsekcji. Stopka zawiera: imię i nazwisko autora, instytucję, tytuł prezentacji, aktualną datę oraz numer slajdu. | ![Screenshot](https://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH-infolines.png "Slajd") |
| miniframes | Nagłówek zawiera poziomy pasek nawigacyjny, którego elementami są małe kółka — reprezentują poszczególne slajdy sekcji. | ![Screenshot](https://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH-miniframes.png "Slajd") |
| smoothbars | Motyw ten zachowuje się bardzo podobnie do motywu **miniframe**, przynajmniej w odniesieniu do nagłówka. Jedyną różnicą są płynne przejścia kolorystyczne pomiędzy kolorami tła pasków slajdu.  Domyślnie, slajdy nie posiadają stopki. | ![Screenshot](https://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH-smoothbars.png "Slajd") |
| sidebar    | Z lewej strony slajdu znajduje się pasek ze spisem treści prezentacji. | ![Screenshot](https://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH-sidebar.png "Slajd") |
| split      | Lewa część nagłówka zawiera tytuł sekcji, a w prawa, podrozdziały bieżącej sekcji.| ![Screenshot](https://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH-split.png "Slajd") |
| shadow     | Rozszerzona wersja motywu **split** — poziome cieniowanie za tytułem slajdu oraz dodawany jest mały „cień” na dole nagłówka. | ![Screenshot](https://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH-shadow.png "Slajd") |
| tree       | Nagłówek zawiera trzy linie, które pokazują tytuł prezentacji, tytuł bieżącej sekcji oraz podsekcji. | ![Screenshot](https://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH-tree.png "Slajd") |
| smoothtree | Motyw podobny do **tree**. Główną różnicą jest płynna zmiana kolorów tła. | ![Screenshot](https://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH-smoothtree.png "Slajd") |
### Opcja `outerthemeoptions`
Niektóre z wyżej opisanych motywów mogą być konfigurowane za pomocą opcji. W celu wyspecyfikowania listy opcji należy użyć opcji _outerthemeoptions_, np.  `\usetheme[outerthemeoptions={footline=authortitle}]{AGH}`.

Wykaz opcji dla poszczególnych motywów, jak i dokładniejszy opis motywów, znajdziesz w [Podręczniku klasy 'beamer'](http://mirror.ctan.org//macros/latex/contrib/beamer/doc/beameruserguide.pdf).
### Opcja `parttitle`
Na podstawie własnego doświadczenia mogę stwierdzić, że podział dużych prezentacji (np. wykłady) na części, jest bardzo wskazany. Jeżeli za pomocą komendy `\part`, podzieliłeś/aś swoją prezentację na części, to za pomocą opcji _parttitle_ możesz spowodować, aby tytuł części był widoczny na slajdzie.
#### Przykłady
- `\usetheme[parttitle=author]{AGH}` — zamiast imienia i nazwiska autora wyświetlaj tytuł części.
- `\usetheme[parttitle=date]{AGH}` — zamiast daty wyświetlaj tytuł części.

_Opcja 'parttitle' działa tylko z tymi motywami zewnętrznymi, które umożliwiają  wyświetlanie, w stopce slajdu, imienia i nazwiska autora lub daty._
## Wersje kolorystyczne
| Domyślna                                                                                 | Z ciemnym tłem                                                                                                |
| ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| ![Screenshot](http://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH.big.png "Slajd tytułowy") | ![Screenshot](http://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH-dark.big.png "Slajd tytułowy — wersja ciemna") |

_Symbol graficzny AGH jest zastrzeżony i bez zezwolenia, nie powinien być stosowany przez osoby i instytucje niezwiązane z AGH._
## Przykładowe prezentacje
- [Prezentacja 1](http://www.icsr.agh.edu.pl/~polak/beamer.pdf)
- [Prezentacja 2](http://www.icsr.agh.edu.pl/~polak/wms/beamer.pdf)
- [Prezentacja 3 — wersja z ciemnym tłem](http://www.icsr.agh.edu.pl/~polak/wms/latex/beamer-mozliwosci.pdf)

Jeżeli powyższe przykłady przekonały Cię, że warto tworzyć prezentacje w oparciu o LaTeX Beamer, a ... nie wiesz, jak się do tego zabrać, to polecam Ci [mój kanał na youtube](https://www.youtube.com/playlist?list=PLlOvf-mh5wJEzL2onjzBdenUpssbonmO5).  :smile:
## Instalacja
Uruchom komendę
```
$ pdflatex beamerthemeAGH.dtx
```
do wygenerowania plików `.ins`, `.sty`, `.pdf` oraz `example.tex`.

Aby poprawnie wygenerować historię zmian oraz indeks dla dokumentacji pakietu, należy uruchomić
```
$ makeindex -s gind.ist beamerthemeAGH
$ makeindex -s gglo.ist -o beamerthemeAGH.gls beamerthemeAGH.glo
$ pdflatex beamerthemeAGH.dtx
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
Jeśli wynikiem są ścieżki do plików, to znaczy, że poprawnie zainstalowałeś/aś pakiet.
## Szablon przykładowej prezentacji
Ze względu na trudności związane z dostarczaniem przykładów użycia komend oraz środowisk w dokumentacji pakietu, są one pokazane w oddzielnym pliku — `example.tex` — zawiera on jednocześnie przykładową prezentację. Możesz ją więc potraktować jako szablon do utworzenia własnej prezentacji.

Aby otrzymać wynikowy dokument PDF, należy skompilować, **trzykrotnie**, dokument źródłowy za pomocą komendy `pdflatex`:
```
$ pdflatex -shell-escape example
$ pdflatex -shell-escape example
$ pdflatex -shell-escape example
```
