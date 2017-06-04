# beamer-AGH

[![Download](https://img.shields.io/badge/Download-Latest_Release-brightgreen.svg?style=flat)](https://github.com/polaksta/beamer-AGH/releases/latest)

| English version | Wersja polska |
|-----------------|---------------|
|A LaTeX Beamer theme based on one of the official [AGH-UST PowerPoint templates](http://www.agh.edu.pl/en/university/agh-ust-visual-identity/presentation-templates/). In order to use it, put `\usetheme{AGH}` in the preamble of your LaTeX document, and compile your document **twice** or **three times**:smile: (if necessary).|Motyw dla prezentacji LaTeX Beamer, oparty na jednym z oficjalnych [szablonów AGH](http://www.agh.edu.pl/uczelnia/system-identyfikacji-wizualnej/szablon-prezentacji/) dla PowerPoint-a. Aby go użyć, umieść w preambule swojego dokumentu komendę `\usetheme {AGH}`, a następnie skompiluj ten dokument **dwa razy** lub **trzy razy**:smile: (jeśli to konieczne).|

## Options / Opcje
| English version                                                     | Wersja polska                                          |
|---------------------------------------------------------------------|--------------------------------------------------------|
| Based on my own experience, I can say that the division of big presentations (e.g. lectures) into parts is very indicated.  If you defined parts using `\part` command, you can use the *parttitle* option to make the part title visible on the slide: <ul><li>`\usetheme[parttitle=leftfooter]{AGH}` - put the part title in the left footer (instead of author's and institute name)</li><li>`\usetheme[parttitle=rightfooter]{AGH}` - put the part title in the right footer (instead of date)</li></ul> | Na podstawie własnego doświadczenia mogę stwierdzić, że podział dużych prezentacji (np. wykłady) na części, jest bardzo wskazany. Jeżeli za pomocą komendy `\part`, podzieliłeś swoją prezentację na części, to za pomocą opcji *parttitle* możesz spowodować, aby tytuł części był widoczny na slajdzie: <ul><li>`\usetheme[parttitle=leftfooter]{AGH}` - umieść tytuł części w lewej stopce (zamiast nazw autora oraz instytutu)</li><li>`\usetheme[parttitle=rightfooter]{AGH}` - umieść tytuł części w prawej stopce (zamiast daty)</li></ul> |
|If the presentation will be in a darkened room, it may be useful to use a dark background - in this case use the *dark* option, i.e. `\usetheme [dark]{AGH}`.|Jeżeli prezentacja będzie się odbywać w zaciemnionej sali, to przydatne może być użycie ciemnego tła - w takim przypadku użyj opcji *dark*, tj. `\usetheme [dark]{AGH}`.|
|You can specify how dark the background should be, by assigning (to this option) an integer value from 50 to 90, eg `\usetheme[dark=75]{AGH}`. The default value is 50.|Możesz określić jak bardzo ciemne ma być tło, przypisując (tej opcji) wartość całkowitą z przedziału od 50 do 90, np. `\usetheme[dark=75]{AGH}`. Domyślną wartością jest 50.|

## Color versions / Wersje kolorystyczne
| Default / Domyślna | Dark background / Z ciemnym tłem |
|--------------------|----------------------------------|
| ![Screenshot](http://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH.big.png "Title slide") | ![Screenshot](http://www.icsr.agh.edu.pl/~polak/wms/beamer-AGH-dark.big.png "Title slide - dark version") |

*The AGH-UST graphic symbol is proprietary and should not be used outside AGH-UST without permission.*
*Symbol graficzny AGH jest zastrzeżony i bez zezwolenia, nie powinien być stosowany przez osoby i instytucje niezwiązane z AGH.*
  
## Example presentations (in Polish) / Przykładowe prezentacje
* [Prezentacja 1](http://www.icsr.agh.edu.pl/~polak/beamer.pdf?github)
* [Prezentacja 2](http://www.icsr.agh.edu.pl/~polak/wms/beamer.pdf?github)
* [Prezentacja 3 - wersja z ciemnym tłem](http://www.icsr.agh.edu.pl/~polak/wms/latex/beamer-mozliwosci.pdf?github)

Jeżeli powyższe przykłady przekonały Cię, że warto tworzyć prezentacje w oparciu o LaTeX Beamer, a ... nie wiesz jak się do tego zabrać, to polecam Ci [mój kanał na youtube](https://www.youtube.com/playlist?list=PLlOvf-mh5wJEzL2onjzBdenUpssbonmO5) :smile:
