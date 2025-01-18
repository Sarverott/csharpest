# DEVNOTE: DRAFT
opis:
- fabryka fiszek - 
	- LORE= miejsce: biurko z kompem; misja: zcyfryzować przytłaczającą ilość karteczek samoprzyklejnych przyklejonych do monitora... choć go nie widać pod sticknotesami to faktycznie jest to monitor
	- PSEŁDODEF= uruchamiając program chcemy komunikat, że tworzymy plik TXT na pulpicie, wypisać listę plików TXT jakie tam są, Console Read nazwa notki bez ".txt" i Console Read treści pliku. enter i enter ma zamknąć plik i zakończyć program {pętla do..while(!isEmpty(input)) } 
	- DIY IDEAS= chciałbyś mieć lepszy tool do tego? no to znakomicie, udoskonal to, przykładowo:
		- dając main menu wyświetlającego pliki txt, inputem wybieranych numerowanych opcji z 0 jako EXIT i pętlą main menu puki (opcja!=0)
		- opcje usuń, nadpisz plik, stwóż nową notkę, zmień folder na notki z domyślnego Desktop
		- sprawdzanie czy plik istnieje, walidacja nazwy pliku z ucinaniem wprowadzonej nazwy po kropce (wykluczenie sytuacji typu "evil_nota.duposkrypt.txt")