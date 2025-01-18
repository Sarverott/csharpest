# DEVNOTE: DRAFT
opis:
- wypluwacz znaków ascii od 0 do 255
	- pierdoła obrazująca czym jest tekst
	- helper merytoryczny pod gist
    - zabawy z ascii

#### fragmenty okołotematowe

UNICODE ZALGO

```csharp 
// lowest grounding env of SolutionChain is powershell
// PSEUDOCODE::|  SolutionChain = XSSfromwebapp->encodeURI()->END.return|||CHANGE_ENVIROMENT|||CS_receiver.result->decodeURI()->string.saveTo("Console.Title");
// console's window title to text with zalgo glitching


// ISSUE: Untrustworthy textfiles processing in windows, unsure behaviour of csharp in widescale contact rawZalgoString in code and diffrent configs of residential enviroment, versions and OSs on various ocasions
// NOTE: at first attempt of base64 encoding fails - 
 
// UNICODE ZALGO
Console.Title=System.Uri.UnescapeDataString("!%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%AB%20%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%AB!%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%AB%20%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%AB!%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%AB%20%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%ABW%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%ABA%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%ABR%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%ABN%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%ABI%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%ABN%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%ABG%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%AB%20%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%AB!%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%AB%20%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%AB!%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%AB%20%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%AB!%CC%8D%CC%8E%CC%84%CC%85%CC%BF%CC%91%CC%86%CC%90%CD%92%CD%97%CD%91%CC%87%CC%88%CC%8A%CD%82%CC%96%CC%97%CC%98%CC%99%CC%9C%CC%9D%CC%9E%CC%9F%CC%A0%CC%A4%CC%A5%CC%A6%CC%A9%CC%AA%CC%AB");
// UNICODE ZALGO

// yes... this is overpowered idea of fancy swaggy broken title generation on webapp opened in human-mimicing headless web browser with js injected and while transition of broken unicode that string is encoded treating it as url encoded before returning by virtWebApp ogar and decoded after receiving by troyMinion from wrath division... on linux with "csharp -e 'code '" it's not working... fuck

// even exiting is enoying >:[

Environment.Exit(666);

```

#XSSfromwebapp puppetier albo inny headless crawlerkompatybilny ogarek

```js
/* PSEUDOCODE but after reconsilyation looks IMPLEMENTABLE, i will be back here.. i hope so xd */
XSSfromwebapp={
	url:"http://zalgo.it/", // todo: research this one, reverse enginering and developement of own zalgo generator, investigate suspisions parts of web app, search for reverse repl or other threats  
	afterLoad:(windowHook)=>{
		//this.return = encodeURIComponent( // shitcode, reason why it does what it then done is unknown and behaviour of that was not as predicted, can it be broken or can it breaks orginal data while encoding?
		//	windowHook.$("#display_out")[0].innerText
		//);
		this.return = encodeURI( // works well, screw encodeURIComponent
			windowHook.$("#display_out")[0].innerText
		);
	},
	return:String //hardcore url encoded string, block of text above
}
```

szybki csharp z przykładem zabawy kolorowymi escape codes 

```bash
csharp -e 'Console.WriteLine("[\x1b[90m>\x1b[5m\x1b[92m3\x1b[0m\x1b[90m<\x1b[0m]");'
```

wypasiony jednoliniowiec, pokazujący co można wyczarowywać

```bash
csharp -e 'Console.Clear();Console.Title="! ! ! WARNING ! ! !";Console.Write("### \x1b[31m[WARNING!!!\x1b[0m ENTERING DANGER ZONE ###\t\t");System.Threading.Thread.Sleep(500);Console.Write("press key to confirm that you know what you doing ");System.Threading.Thread.Sleep(3000);Console.Write("\r                                  \r\n");Console.Write("\r\t[\x1b[90m\x1b[2m>\x1b[0m\x1b[92m3\x1b[0m\x1b[90m\x1b[2m<\x1b[0m]\x0007");System.Threading.Thread.Sleep(1100);Console.Write("\r\t[\x1b[90m>\x1b[93m2\x1b[0m\x1b[90m<\x1b[0m]\x0007");System.Threading.Thread.Sleep(1200);Console.Write("\r\t[\x1b[6m\x1b[91m>\x1b[97m\x1b[41m1\x1b[40m\x1b[91m<\x1b[0m]\x0007");System.Threading.Thread.Sleep(500);Console.Write("\x0007");System.Threading.Thread.Sleep(500);Console.Write("\x0007");System.Threading.Thread.Sleep(500);Console.Write("\r\t\x1b[5m\x1b[31m[000]\x1b[0m");System.Threading.Thread.Sleep(500);Console.WriteLine("\n\n ### \x1b[32mG0ODBYE WORLD\x1b[0m, \x1b[5m\x1b[41m APOCALYPSE TIME \x1b[0m \x1b[35m ( ͡~ ͜ʖ ͡°) \n\n\x1b[7m");Console.WriteLine("JK nothing malicious here, these are not viruses you are looking, keep scanning elsewhere...")'
```

#### konceptualnie przykład w innym języku
- https://gist.github.com/Sarverott/c6008f7a5685ff69d8556ed1aa2cc36e
- https://gist.github.com/Sarverott/e789a577bae65704e7f862694f44bff5
- https://gist.github.com/Sarverott/ccee32daaeb22716fc048bff61875229