---
title: "Utveckla .NET applikationer i Visual Studio Code"
date: 2020-10-19
author: Andreas Hagsten, systemutvecklare
tagline: "Den här bloggposten är en enkel steg för steg-post för att komma igång med utveckling av .NET core i Visual Studio Code. En kollega berättade nyligen att han precis hade gått över från Visual Studio till Visual Studio Code som sin primära editor när det kommer till .NET-applikationer. Jag hade koll på att det var klart möjligt men trodde inte att det var så pass moget att gå över till helt. Det lät intressant och det började givetvis klia i fingrarna."
header:
  overlay_image: https://www.infozone.se/wp-content/uploads/2020/10/close-up-of-hands-contemporary-website-developer-man-typing-and-code-picture-id1167467556.jpg
  teaser: data:image/png;base64,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
categories:
  - blog
tags:
  - microsoft
  - systemutveckling
---
För att utveckla med .NET core i Visual Studio Code behövs till att börja med givetvis Visual Studio Code som du kan ladda hem [här](https://code.visualstudio.com/download), du behöver även [.NET Core SDK och Runtime](https://dotnet.microsoft.com/download).

# Installera tillägg
VSCode är en text editor snarare än en IDE – dock med det lilla extra! Med editorn följer många bra funktioner som auto complete, intelliSense och inbyggt GIT-stöd. Men för att få ut maximalt av editorn behöver du installera tillägg (och många finns det…). Ett tillägg som måste installeras för att komma vidare är [C# extension](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp) som kan hämtas via föregående länk eller via ”Extentions” inne i editorn.

Andra bra tillägg för att komma närmre känslan av en IDE likt Visual Studio är [.NET Core Test Explorer](https://marketplace.visualstudio.com/items?itemName=formulahendry.dotnet-test-explorer) samt [NuGet Package Manager](https://marketplace.visualstudio.com/items?itemName=jmrog.vscode-nuget-package-manager).

# Fördelar med Visual Studio Code
Vänta nu, varför vill man gå över till Visual Studio Code när Visual Studio är en så pass bra IDE? Även om denna artikel egentligen inte handlar om VSCode jämfört med Visual Studio så vill jag kort belysa några av de stora fördelarna.

- Cross platform – det betyder att du kan utveckla på Windows, macOS och Linux
- Gratis både för privat och kommersiellt bruk
- Lättviktigt och fokuserat på det dagliga systemutvecklingsarbetet som kodning, testning, debuging samt versionshantering av källkod

# Sätt upp en .NET Core applikation
Öppna upp editorn och navigera till ”Open Folder…” under ”File”-menyn. Skapa en ny mapp på valfritt ställe och välj den. Det är dags att skapa ett .NET core projekt. Som beskrivet tidigare behövs [.NET Core SDK och Runtime](https://dotnet.microsoft.com/download).

Öppna en ny terminal (via ”Terminal”-menyn) om en inte redan är öppen. Skriv in ”dotnet new webapi” för att skapa en ny applikation via mallen för ett WebAPI,  och tryck Enter.

Om det är första gången du gör detta kommer det installeras en del mjukvaror som behövs för att kompilera och debugga applikationen, t.ex. OmniSharp och Razor Language Server. Det ser ut ungefär så här:

```powershell
Installing C# dependencies...
Platform: win32, x86_64
Downloading package 'OmniSharp for Windows (.NET 4.6 / x64)' (35884 KB).................... Done!
Validating download...
Integrity Check succeeded.
Installing package 'OmniSharp for Windows (.NET 4.6 / x64)'
Downloading package '.NET Core Debugger (Windows / x64)' (42010 KB).................... Done!
Validating download...
Integrity Check succeeded.
Installing package '.NET Core Debugger (Windows / x64)'
Downloading package 'Razor Language Server (Windows / x64)' (50489 KB).................... Done!
Installing package 'Razor Language Server (Windows / x64)'
Finished
```

Om du öppnar en C#-fil kommer du känna igen färgkodningen från t.ex. Visual Studio, så kallad syntax highlighting. Är du observant ser du även funktionen ”code lens” (0 referenses) precis som i Visual Studio.

![Färgkodning i C# samt funktionen code lens](https://www.infozone.se/wp-content/uploads/2020/10/syntax_codelens.png)

Det ser rätt trevligt och bekant ut, eller hur? Om du börjar skriva lite kod märker du snabbt att det finns intellisense precis som du är van vid och om du håller musen över en funktion får du information densamma, som du får i Visual Studio.

![Trevligt med intellisense](https://www.infozone.se/wp-content/uploads/2020/10/intellisence.png)

# Debugging i Visual Studio Code
Nu har du förhoppningsvis fått upp ett webbprojekt och hunnit klicka runt lite i filerna. Det är dags att köra igång projektet och testa debuggern. Klicka på symbolen för debug i vänstermenyn. Här måste du skapa en ”launch.json”-fil, det gör du enklast genom att klicka på länken ”create a launch.json file” och välj ”.NET Core” i menyn som dyker upp. Efter detta är du redo att köra igång.

![](https://www.infozone.se/wp-content/uploads/2020/10/configure_debug.png)

Låt filen som genereras vara som den är, det intressanta för vår del nu är att det nu finns en debugknapp högst upp i vänsterpanelen. Sätt en brytpunkt någonstans i Get-funktionen och starta debuggern (via F5 eller klick på knapp). Webbläsaren bör ladda in https://localhost:5001, men där finns inget. Navigera istället till https://localhost:5001/weatherforecast för att komma till brytpunkten.

![](https://www.infozone.se/wp-content/uploads/2020/10/debug-e1601558240871.png)

I vänsterpanelen finns bekanta ting som brytpunkter, lokala variabler och bevakade egenskaper, det finns även en Debugkonsoll där uttryck kan skrivas och inspekteras. Att lägga till bevakade egenskaper, så kallade ”watches” fungerar på samma sätt som i Visual Studio (t.ex. genom att högerklicka på variabeln…).

För att stega i koden används bekanta tangenter som t.ex. F10, F11 samt F5. Bekant är ordet.

# Enhetstester i Visual Studio Code
Det sista jag tänkte gå igenom är hur du kör enhetstester, här rekommenderar jag tillägget [.NET Core Test Explorer](https://marketplace.visualstudio.com/items?itemName=formulahendry.dotnet-test-explorer).

![Enhetstester i Visual Studio Code](https://www.infozone.se/wp-content/uploads/2020/10/unittests.png)

Testbiblioteket som används är xUnit, det och tillägget ovan är det enda som behövs för att finna projektets alla enhetstester. Text-explorern tillåter en köra testerna i alla nivåer – med eller utan debugger. En liten bonusfunktion är att kontextmenyn har alternativ som ”Run Tests in context” och ”Debug Tests in context” vilket kör det test som markören står i, eller alla test i en klass om markören står utanför en testmetod – tjusigt!

Jag hoppas du fått upp ögonen för att det faktiskt inte är en hög tröskel att börja använda Visual Studio Code för dina .NET-core projekt. Tänker mig att jag ska ge editorn en ärlig chans i ett riktigt projekt nu, kanske kommer en mer ingående artikel på det temat i framtiden.
  
