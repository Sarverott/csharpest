# DEVNOTE: DRAFT
opis:
- ekran logowania
	- LORE= jesteś w nowonarodzonej agencji szpiegowskiej Johna Englisha i chcesz aby tajna zaszyfrowana specjalnymi hakerskimi zabawkami funkcja robiąca poufne czarymary tylko gdy hasło i login się zgadzają
		- UWAGA bez podpowiedzi jak cheatować mówiąc co to base64, co to obfuskowanie i bliskiemu zeru security tego patentu. Jeśli ktoś poda hasło specjalne to oznaczać będzie że ktoś odobfuskował kod i zobaczył wiadomość której bez inżynierii wstecznej nie odkryjesz
		  *ŚCIŚLE TAJNE* **HASŁO SPECJALNE**: **`OKOŃ`** 
		  templejtki zbywających odpowiedzi:
			  1. {james-bond} niestety gdybym odpowiedział na te pytania musiałbym was zabić
			  2. {man-in-black} nie mam pojęcia, ale wiedziałem... ostatnie co pamiętam, to to że taki pan w ciemnych okularach i w garnituże z błyskającym długopisem powiedział że to nie byli kosmici
			  3. {back-to-future} nie wiem, poprzedni developer nie zostawił dokumentacji, bo cofnął się w czasie, zaliczył swoją własną matkę zanim poznała ojca i dostał napadu przestawania istnienia... miał sztos furę, takiego tuningowanego deloriana
			  4. {sins-of-creators} jestem tak naprawdę superbohaterem będącym strażnikiem kasety czasu, a to jest pierwotnie przerobionym kodem źródłowym kosmicznego magnetowidu mocarności do podróży w czasie z użyciem VHSa przeznaczenia - czy sądzisz, że jako soulmate VHSa przeznaczenia puszczającego bieg czasu w naszym matrixie mógłbym narazić go na szwank zdradzając ci takie informacje? I TAK JUŻ WIESZ ZA DUŻO! **ZOSTAW MAGNETOWID!!!** jakby znowu się popsuł to jesteśmy w dupie, to ostatni zapasowy, a serwisy zamkneły działalności lata temu... 
			  5. nie chcesz wiedzieć... chyba że chcesz wiedzieć... ja ci nie mogę powiedzieć... rozwiążesz to i możesz sam się dowiedzieć... a jeśli liczysz na jakąś teorię spiskową z nigdy nieodkrywalnymi hakermańskimi paraniozacjami to przykro mi, zawiedziesz się wtedy jak okaże się że faktycznie jak uda ci się zalogować wszystko się odtajni
			  6. ale wy wiecie że to ma system autodestrukcji i może ulec samozniszczeniu? jak powiem to każda kopia eksploduje, a eksplozja laptopa dla kożystającego programisty jest pardzo niezdrowa
			  7. w sensie nie widzicie tajnych rzeczy? dziwne... a próbowaliście wyłączyć i znowu włączyć? (pauza, potem ew mruknięcie "mhm" kończące temat)
			  8. a bo ja wiem? ja tu tylko sprzątam, nie zadawaj mi takich dziwnych pytań
			  9. NIE INTERERE BO KICIKICI
			  10. nie interesuj się bo kociej mordy dostaniesz
			  11. ponieważ zamknij się dzbanie, ale też cichaj i tak ogólnie to jak będziesz dalej czitować to dam ci bana w realu na łakocie 
			  12. bez komentarza
			  13. pomidor
			  14. otóż są dwa typy osób, te które ekstrapolują kompletną informację na podstawie niepełnych danych
			  15. {henryk-garncarz} to część sekretnego spisku pradawnej mistycznej loży kapturowców kliki królika rządzącej światem z ukrycia, więc to musi być czarymary bite gary czyli nawet autor nie wie jak to działa
	- INITFILES= 
		- ".AGENTS_CREDENTIALS" #file #plain-text
			- plik z liniami według patternu "base64(username):base64(password)"
			- każda linia to user
				- UWAGA SPOILER jeden z nich to admin z hasłem 123456
		- "main.cs" #file #csharp-code
			- z nagłówkiem komentarza tłumaczącym że tylko w wyznaczonym miejscu można coś zmieniać bo inaczej ten folder ulegnie samozniszczeniu
			- szkielet z importowaniem "TOP_SECRET.cs" i przestrzenią kilku linii między "#editable space BEGIN" a "#editable space END"
			- 
		- `.TOP_SECRET.cs` #file #csharp-code #obfuscated
			- plik z zobfuskowanym c# kodem 
			- funkcja wprowadzenia listy userów... ale to co odczytujesz ma być jednym stringiem... wszystkich userów za jednym zamachem... z przecinkami między userami 
				- poniżej w ekstrasach replówka w jsie ( [[#ekstras 1]] ) generująca przykład takiego stringa i przykładu jak miało by to wyglądać
			- 
			- najpierw testującym czy ten fragment kodu został zmodyfikowany
			- jeśli tak 
				- wyświetlający animację ASCII ART, 
				- po animacji printujący odtajniony kod 
				- dodając dla ciekawskich mówiący jak ktoś chce zrobić sobie taki tajny przez poufny fragment kodu to poczytaj o obfuskacji `<link-do-github-repo>`
				- 
	- PSEŁDODEF= masz plik w którym każda linia jest patternem "user:pass" i według tej zasady chcemy odczyt 

#### fragmenty okołotematowe

zabawa ładnym odliczaniem w konsoli

```cs
Console.Clear();Console.Title="! ! ! WARNING ! ! !";Console.Write("### \x1b[31m[WARNING!!!\x1b[0m ENTERING DANGER ZONE ###\t\t");System.Threading.Thread.Sleep(500);Console.Write("press key to confirm that you know what you doing ");System.Threading.Thread.Sleep(3000);Console.Write("\r                                  \r\n");Console.Write("\r\t[\x1b[90m\x1b[2m>\x1b[0m\x1b[92m3\x1b[0m\x1b[90m\x1b[2m<\x1b[0m]\x0007");System.Threading.Thread.Sleep(1100);Console.Write("\r\t[\x1b[90m>\x1b[93m2\x1b[0m\x1b[90m<\x1b[0m]\x0007");System.Threading.Thread.Sleep(1200);Console.Write("\r\t[\x1b[6m\x1b[91m>\x1b[97m\x1b[41m1\x1b[40m\x1b[91m<\x1b[0m]\x0007");System.Threading.Thread.Sleep(500);Console.Write("\x0007");System.Threading.Thread.Sleep(500);Console.Write("\x0007");System.Threading.Thread.Sleep(500);Console.Write("\r\t\x1b[5m\x1b[31m[000]\x1b[0m");System.Threading.Thread.Sleep(500);Console.WriteLine("\n\n ### \x1b[32mG0ODBYE WORLD\x1b[0m, \x1b[5m\x1b[41m APOCALYPSE TIME \x1b[0m \x1b[35m ( ͡~ ͜ʖ ͡°) \n\n\x1b[7m");
```

#### informacje apropo

OBFUSKACJA: mniej opcji niż sądziłem
- https://marketplace.visualstudio.com/items?itemName=NWTSolution.CSharpObfuscator2022
- https://github.com/nwtsolution/CSharpObfuscator

---
###### ekstras 1
replówka PoC'owa zwracająca przykładową listę userów do zdefiniowania jacy userzy istnieją
```js
["admin", "TH3_dupiurz4guwnodziej", "kuropatwa", "USER", "root", "guest         ", "lord_vadermord8", "czlowiekrekakarpia", "ulegla_suczka", "dr.ruchatrupa", "tajgerbonzo4ever", "karmazyn0wySkurv1el"].map((x)=>btoa(x)).join(",")
```
powyższe daje string `"YWRtaW4=,VEgzX2R1cGl1cno0Z3V3bm9kemllag==,a3Vyb3BhdHdh,VVNFUg==,cm9vdA==,Z3Vlc3QgICAgICAgICA=,bG9yZF92YWRlcm1vcmQ4,Y3psb3dpZWtyZWtha2FycGlh,dWxlZ2xhX3N1Y3prYQ==,ZHIucnVjaGF0cnVwYQ==,dGFqZ2VyYm9uem80ZXZlcg==,a2FybWF6eW4wd3lTa3VydjFlbA=="` i dla userów `["admin", "TH3_dupiurz4guwnodziej", "kuropatwa", "USER", "root", "guest         ", "lord_vadermord8", "czlowiekrekakarpia", "ulegla_suczka", "dr.ruchatrupa", "tajgerbonzo4ever", "karmazyn0wySkurv1el"]`

###### ekstras 2
apropo komunikowania typu _"halo mamy ERROR lub ERRORY! masz listę zażaleń, pierdole nie robię dalej, awaryjny stop tu i teraz, żegnam"_  można użyć dosłownie **"wyrzucacza errorów"**, który jest kluczowym mechanizmem debugowania. 

```csharp
// oto wyrzucacz, program się wykonując zawsze jak trafia na to wdraża procedury stanu kryzysowego 
Console.Write("### ENTERING DANGER ZONE ###");
System.Threading.Thread.Sleep(3000);// delay
Console.Write("\r                                  \r\n");
Console.Write("\r\t[\x1b[90m\x1b[2m>\x1b[0m\x1b[5m\x1b[92m3\x1b[0m\x1b[90m\x1b[2m<\x1b[0m]\x0007");// step
System.Threading.Thread.Sleep(1100);// second
Console.Write("\r\t[\x1b[90m>\x1b[5m\x1b[93m2\x1b[0m\x1b[90m<\x1b[0m]\x0007");
System.Threading.Thread.Sleep(1200);// second
Console.Write("\r\t[\x1b[5m\x1b[91m>\x1b[41m1\x1b[91m<\x1b[0m]\x0007");
System.Threading.Thread.Sleep(500);// cheaty secondlings
Console.Write("\x0007"); ///// fun while advanced acsii char playing ; googled this dataOre https://learn.microsoft.com/pl-pl/dotnet/csharp/language-reference/builtin-types/char
System.Threading.Thread.Sleep(500);// cheaty second
Console.Write("\x0007");
System.Threading.Thread.Sleep(500);// cheaty second
Console.Write("\r\t\x1b[31m[000]\x1b[0m");
System.Threading.Thread.Sleep(500);// second
Console.WriteLine("\n\n ### \x1b[32mG0ODBYE WORLD\x1b[0m, \x1b[5m\x1b[41m APOCALYPSE TIME \x1b[0m \x1b[35m ( ͡~ ͜ʖ ͡°) \n\n\x1b[7m");

Console.Write("[ 3 ]");// step
System.Threading.Thread.Sleep(1000);// second   //// google<< "csharp delay" => SEARCH_RESULT bestDataOre= https://stackoverflow.com/questions/5449956/how-to-add-a-delay-for-a-2-or-3-seconds  
Console.Write("\r[ 2 ]");// step
System.Threading.Thread.Sleep(1000);// second
Console.Write("\r[ 2 ]");// step
System.Threading.Thread.Sleep(1000);// second



throw;
// neverland 


Console.WriteLine("\n\n ### \x1b[32mG0ODBYE WORLD\x1b[0m, \x1b[5m\x1b[41m APOCALYPSE TIME \x1b[0m \x1b[35m ( ͡~ ͜ʖ ͡°) \n\n\x1b[7m");


// jeśli jest cokolwiek bezpośrednio po throw tak jak ten Console.WriteLine to będzie to jałowy kod który nigdy się nie wykona - tak 



throw;
Console.WriteLine("\n\n jeśli program właśnie wypisał ten komunikat \n    to jest bardzo źle...\n errory stały się niewidzialne \n  a kluczowe fundamentalne sidła łapiące awarie, gliche i niebezpieczeństwa\n stały się bezużyteczne \n   jeśli to nie twoje eksperymenty to wywołały i nie masz pojęcia jak to naprawić \n to przygotuj się na ostrą jazdę bez trzymanki przez czeluści najgorszych piekła programistów \n\n");


```