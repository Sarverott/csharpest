# DEVNOTE: DRAFT
opis:
- arraye z regułami internetu, odczyt plików z rozwinięciem i wytłumaczeniem o co biega
	- PSEŁDODEF&LORE:
		- hardcoded array z listą nazw, i 20 plików wg. patternu "18.txt"
			- UWAGA: bez spoilerowania o indexowaniu, niech faktor zaskoczeniowy, że pierwszy element to index 0 będzie selfexperience
		- print forem wg. patternu "20. ostatnia z 20"
		- prompt inputowy -> numerek=liczba
			- UWAGA: zasugeruj sprawdzanie numeru 7
		- odczyt odpowiedniego pliku jako KMINA
			- UWAGA: bez spoilerów apropo nazw plików, końcowo potem sprawdzając poproś o pierwszą i ostatnią regułę - będą niezgodne z tym co powinno być i jest to celowe, pliki są od 1 do 20, a indexy od 0 do 19... cholera ktoś nie miał pojęcia jak działa array jak je tworzył, zapytaj kursantów co można zrobić; znane rozwiązania:
				- **`potem wyrazić aprobatę pierwszej osobie która rzuci jakimkolwiek pomysłem i osobie która da jakimkolwiek rozwiązanie, bo inicjatywa w brainstormingu lepsza jest niż cisza`** _(żartobliwe teksty, które będą zabawne też zokejkować - rozluźnienie atmosfery spiętego zespołu to klarowniejsze myśli kolektywnego przekminiania... a spięte poślady z kijem w dupie to zaparcie które jest niezdrowe dla tworzonych kodów)_
				- **easy, jak ktoś to zaproponuje to pozytywny sygnał beginerski, upierdliwe i lepsze niż brak pomysłów, pierwszy pomysł co robić**-> zmiana nazw plików uwzględniając start od index 0 jako pierwszy: solvuje, ale repetytywnie trzeba z palca każdą nazwę zmieniać... mi na przykład się nie chce, jestem leniwy. Argumentem jak ktoś usprawiedliwia że to prostsze to można dodać "poza tym dostałeś te pliki, więc jak zostanie potem dodana 21 to będzie dupa"
				- **bardziej cwane, proste i najbardziej wszyscy są happy, to wybieramy z opcji** PREINKREMENTACJA NUMEREK czyli INKREMENTACJA WARTOŚCI Z INPUTU PRZED ZASTOSOWANIEM W NAZWIE PLIKU: innymi słowy najpierw +1 zmienną i zapisz ile to, potem daj co w zmiennej... oto słowo promyczkowe... niech potęga światła będzie z wami padawani
				- _jeśli pojawią się inne pomysły - **dopisać dla przyszłych pokoleń** to wtedy będzie ładny przykład do obrazowania, że mimo że jest to  { mi się nie chce kminić co można wykminić, my job is done, bo jestem leniwy, z góry dziękuję ;) }_
		- print nazwy reguły z numerem
		- print 20 myślników
		- print sentencji z książki znajdujący się w zmiennej KMINA
	- DIY IDEAS= walidacja czy pozycja pod podanym numerem istnieje, jeśli to liczba z dupy to można zakodować krzyczenie komunikatem "nie ma takiej liczby, takie coś nie istnieje, dalsze działanie jest niemożliwe" ; najlepiej krzyczą ERRORY, można dać gotową linijkę z [[#ekstras 2]]

#### dane przerobowe
- INTERNET ARCHIVE: https://archive.org/stream/RulesOfTheInternet/RulesOfTheInternet..txt
- raw plain text format: https://ia601605.us.archive.org/21/items/RulesOfTheInternet/RulesOfTheInternet..txt