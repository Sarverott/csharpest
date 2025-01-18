# Tradycyjny Pierwszy Program 
```
▗▖ ▗▖▗▄▄▄▖▗▖   ▗▖    ▗▄▖     ▗▖ ▗▖ ▗▄▖ ▗▄▄▖ ▗▖   ▗▄▄▄ 
▐▌ ▐▌▐▌   ▐▌   ▐▌   ▐▌ ▐▌    ▐▌ ▐▌▐▌ ▐▌▐▌ ▐▌▐▌   ▐▌  █
▐▛▀▜▌▐▛▀▀▘▐▌   ▐▌   ▐▌ ▐▌    ▐▌ ▐▌▐▌ ▐▌▐▛▀▚▖▐▌   ▐▌  █
▐▌ ▐▌▐▙▄▄▖▐▙▄▄▖▐▙▄▄▖▝▚▄▞▘    ▐▙█▟▌▝▚▄▞▘▐▌ ▐▌▐▙▄▄▖▐▙▄▄▀
```
> - kategoria: #samouczek, #wprowadzenie
> - fikser: @sarverott



nic wielkiego, zwykły krok, a cieszy.

metoda małych kroków była wyborem tych którzy przeszli swoją ścieżką przeciwności do sukcesu i wielkości.

> _jeden mały krok dla człowieka, jeden wielki skok dla ludzkości_ 
> 
> ~ **Neil Armstrong**, amerykański astronauta, dowódca misji Apollo 11


---
### ALE zanim zaczniemy zabawę trzeba się przygotować

Aby zacząć się bawić z `C#` potrzebujemy przygotowania środowiska programistycznego.

Dla ułatwienia tego pierwszego kroku użyjemy czegoś takiego jak [**Mono**](https://github.com/mono/mono) - dostępne jest na prawie każdy współczesny system operacyjny i pozwala na dużą elastyczność w działaniu 

###### instalacja:
- WINDOWS: https://www.mono-project.com/docs/getting-started/install/windows/
- LINUX: https://www.mono-project.com/docs/getting-started/install/linux/
- macOS: https://www.mono-project.com/docs/getting-started/install/mac/
- __**`only for PRO ->`**__ Docker: https://www.mono-project.com/download/stable/#download-docker

### jak wypisać "Hello World" z użyciem `C#`

Są dwie drogi: 
- **ortodoksyjna** czyli najbardziej poprawna tak jak perfekcjonistycznie powinny wyglądać nasze programy
- **leniwa** czyli ta droga którą wybierzemy, bo najpierw trzeba w praktyce zakumać podstawy

Oficjalny Getting Started: https://www.mono-project.com/docs/getting-started/mono-basics/

#### no to wio moje drogie leniwce

Otwórzcie swoje konsole, powinniście mieć dostęp do tych komend, zróbcie kopiuj-wklej poniższych komend z przełącznikiem `-h` do wypisania podstawowego HELP'a tej komendy:  
- `csc -h`: kompilator, na razie pomińmy
- `mono -h`: wykonywator, też pomińmy
- `csharp --help`: nasza piaskownica od której zaczniemy

---
###### czy śledzisz co robimy? jeśli tak to...
##### utkneliśmy! ale to dobrze

__krok 1:__ naciśnij kilka razy **Enter**, jeśli nie widzisz w tym momencie na ekranie:

```
csharp>
csharp>
csharp>
```

to to nie jesteś w [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop), wykonaj komendę `csharp` w swojej konsoli i idź do __krok 1__

###### oto mały przykład psełdokodu z algorytmem krokowym - w praktyce to się robi proste, prawda `;)` 

nie wiemy jeszcze jak wyjść, ale zdradzę wam jak zrobić **hello world** - wklejcie sobie poniższą linijkę:

```
Console.WriteLine("Hello world");
```
po wciśnięciu ENTER powinno już pisać

###### siadać! zanim was z tąd puszczę chcę z wami przyjżeć się teorii

w kolorach będzie to bardziej widoczne:

```cs
Console.WriteLine("Hello world");
```

Ci którzy znają już jakieś podstawy czarowania windowsów mogli korzystać z **powershell** czyli niebieskiego ulepszonego `CMD` (konsola podstawowa w windows to CMD.exe). hello world w **powershellu** wygląda tak:

```powershell
Write-Output "Hello world"
```

odpowiednik w CMD i linuxowym Shellu:

```bash
echo Hello world
```

chcąc wypisać nasz "OUTPUT" w C# trzeba odwołać się do obiektu `Console` który daje nam możliwość użycia funkcji tego obiektu `WriteLine` do wyświetlania "OUTPUT". **A teraz wpiszcie poniższe z palca, bez kopiuj-wklej!**

```cs
Console.Write("OUTPUT"); // bez zakończenia '/n' ( /n to znak ascii "nowa linia", ENTER to w rzeczywistości kiedyś było "nowa linia" i "powrót kursora do lewej", czyli "/n/r" )
```

Wielkości liter są ważne w kodzie, pisząc możecie zauważyć, że wyskakują sugestie

Dobra, czas ewakułować się z tego [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop)a

```cs
Environment.Exit(200); // EFEKT TEJ LINII: program csharp kończy pracę kodem 200
// CO ROBIMY W TEJ LINII:
// chwytając z obiektu "Environment"
// używamy metodę "Exit"  
// wykonujemy z jednym argumentem wejściowym - 666 
```

jeśli chcemy szybkiego leniwego hello world w jednej linii na szybko

```bash
csharp -e 'Console.WriteLine("hello world")'
```

Przydatna wiedza, ale to technicznie rzecz biorąc jeszcze nie pełnoprawny program C#

#### robiąc własny Ortodoksyjny wypisywacz konsolowy

Zacznijmy od tego, że jak już wspominaliśmy po zainstalowaniu powinniśmy mieć takie bajery:

- `csc` lub `mcs` w niektórych przypadkach
- `mono`
- `csharp`

tak wygląda klasyczny kod Hello World, jest to przykład z [Mono Basics](https://www.mono-project.com/docs/getting-started/mono-basics/):


```cs
using System;

public class HelloWorld
{
    public static void Main(string[] args)
    {
        Console.WriteLine ("Hello Mono World");
    }
}

```

W poprzednim leniwym wydaniu mogliśmy sobie pozwolić na wiele pominięć i uproszczeń, ale faktyczny program ma swoją własną ustaloną maskaradę. powyższy kod zapisz jako `main.cs`, następnie z tego samego miejsca odpal takie komendy:

```bash
csc main.cs
mono main.exe
```

> **PROBLEM?** jeśli występuje problem, bo `csc` nie istnieje, to na linuxie nie instalujcie "chicken-bin" - to fałszywy trop, jeśli działa `csharp --help` pewnie da się wyczytać, że to `mcs` się odzywa, mówiąc co potrafi robić, zamiast `csharp`... możecie kombinować albo podążać według [download manuals](https://www.mono-project.com/download/stable/) `¯\_(ツ)_/¯`

#### :tada: DZIAŁA! mamy nasz hello world jako plik EXE :sparkles:

---

# :zap: czas to ulepszyć :zap:

POMYSŁ: zrobić własny `Write-Output`  

weźmy znowu nasz HELLO-WORLD przykład, przyjżyjmy się mu:

```cs
using System;

public class EloSwiecie // tą nazwę można zmieniać
{
    public static void Main(string[] args) // ciekawe to args...
    {
        Console.WriteLine ("Witaj świecie"); // to zastąpimy czymś
    }
}

```

#### zacznijmy od tematu: czym są argumenty?

argumenty to zmienne wejściowe, używamy ich już dłuższą chwilę:

```cs
Console.WriteLine ("argument"); // tutaj
```

w konsoli też mamy argumenty, wygląda to tak:

```bash
echo argument inny_argument kolejny_argument
```

więc drogą dedukcji modyfikując kod

```cs
using System;

public class EchowaczPierwszy // tą nazwę można zmieniać
{
    public static void Main(string[] args) // ciekawe to args...
    {
        //Console.WriteLine ("Witaj świecie"); 
        Console.WriteLine( args );
    }
}

```

i kompilując kod 

```bash
csc main.cs
mono main.exe
```

powinniśmy widzieć coś... ciekawego

nie wiem jak wy ale ja widzę `System.String[]` - jest to tablica, z której za chwilę nauczycie się korzystać.

eksperymentujmy dalej w takim razie :smiling_imp: spróbujmy wypisać informacje o `args`... może długość?


```cs
using System;

public class EchowaczPierwszy // tą nazwę można zmieniać
{
    public static void Main(string[] args) // ciekawe to args...
    {
        //Console.WriteLine ("Witaj świecie"); 
        //Console.WriteLine( args ); // OUTPUT: System.String[]
        Console.Write( "ile itemów jest w ARGS: " );
        Console.WriteLine( args.Length ); // nie wiedziałem to wygooglałem i wyczytałem: https://learn.microsoft.com/pl-pl/dotnet/api/system.array.length?view=net-9.0
    }
}

```

zpreparowałem sobię na szybko tutaj komendę `csc main.cs && mono main.exe` żeby przyspieszyć monotonię w naszej zabawie. O! woła `ile itemów jest w ARGS: 0` a jak odpalamy `mono main.exe dasdasdasdsdads` to mamy `ile itemów jest w ARGS: 1`... 

### JEDZIEMY DALEJ

zmieńmy nazwę pliku na `KRZYCZ.cs`

```cs
using System;

public class EchowaczDrugi // tą nazwę można zmieniać
{
    public static void Main(string[] args) // ciekawe to args...
    {
        //Console.Write( "ile itemów jest w ARGS: " );
        //Console.WriteLine( args.Length );

        Console.WriteLine( args[0] ); // tak łapie się pierwszy przedmiot w ARRAY, robimy to indeksem 0, co wyjaśni się dlaczego tak jest w akcji podczas następnych questów
    }
}
```

w tym momencie `csc KRZYCZ.cs && mono KRZYCZ.exe Wypisuje sie piknie` po części działa... bo w końcu widzimy `Wypisuje`... czyż nie?

### NEXT

chcąc mieć funkcjonalność echo musimy jakoś wypisać wszystkie argumenty... jak w większości języków można **użyć pętli**, typu **FOR** czy **WHILE** które służą standardowo do [iteracji](https://pl.wikipedia.org/wiki/Iteracja), ale nie znamy ich jeszcze... 

#### użyjmy narzędzia do zszywania kolekcji stringów :underage:

mając array _(po polsku mówi się tablica)_ jako ARGS `System.String[]` możemy skorzystać z [JOINa](https://learn.microsoft.com/pl-pl/dotnet/api/system.string.join?view=net-8.0)... mętnie to tu tłumaczą, więc long story short:

```cs
using System;

public class EchowaczDrugi // tą nazwę można zmieniać
{
    public static void Main(string[] args) // ciekawe to args...
    {
        string[] kolekcjaStringow = {"czerwone", "różowe", "prowokujące", "pantalony"};
        char klej = '+';
        Console.WriteLine( kolekcjaStringow );// było
        Console.WriteLine( kolekcjaStringow.Length );// też było
        Console.WriteLine( kolekcjaStringow[0] );// również już było
        // to będzie nowe
        Console.WriteLine( 
            String.Join(
                klej,
                kolekcjaStringow
            )
        );
        // OUTPUT powinien być:
        /*
        System.String[]
        4
        czerwone
        czerwone+różowe+prowokujące+pantalony
        */

    }
}
```

sprawdzanko `csc KRZYCZ.cs && mono KRZYCZ.exe Wypisuje sie piknie`

# OK... co teraz
#### wszystko co wam potrzeba już dostaliście, teraz chcemy widzieć `Wypisuje sie piknie` - KMIŃTA JAK TO WYCZAROWAĆ
spoiler alert! poniżej rozwiązanie
---

```cs
using System;

public class Krzykacz 
{
    public static void Main(string[] args) 
    {
        // nasza własna komenda ECHO
        Console.WriteLine( 
            String.Join(
                ' ',
                args
            )
        );
    }
}
```

---

# OK, jak rozgrzani wszyscy samouczkiem to może coś trudniejszego?

> A **zaawansowanie**, choć wydawałoby się niemożliwe to istnieje: 
> - niech `Krzykacz` zamiast zwyczajnie robić print-out pisze czcionką ASCII z nagłówka pliku

#### [POWRÓT DO QUESTBOARDA](../index.md)