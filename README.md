# ClickPulse

Ein schlichter Autoklicker für Windows 10/11 (64-Bit), erstellt mit C# und WPF.

## Download

Die fertige Einzeldatei wird automatisch über GitHub Actions gebaut und als GitHub Release veröffentlicht:

- [Neueste ClickPulse-Version herunterladen](https://github.com/NiceSpotuuid/ClickPulse/releases/latest/download/ClickPulse.exe)
- [Alle Releases ansehen](https://github.com/NiceSpotuuid/ClickPulse/releases)

Die veröffentlichte EXE ist als Self-contained Single-File für `win-x64` konfiguriert und enthält die .NET-Laufzeit. Eine separate .NET-Installation ist für Nutzer nicht erforderlich.

## Funktionen

- Globaler F6-Hotkey zum Starten und Stoppen
- Intervall in Stunden, Minuten, Sekunden und Millisekunden
- Linke, rechte und mittlere Maustaste; Einzel- oder Doppelklick
- Aktuelle Mausposition oder feste Bildschirmkoordinaten
- Optionale zufällige Intervall-Abweichung
- Optionale Statusbenachrichtigung beim Start und Stopp
- Helle Windows-typische Oberfläche mit nativer Titelleiste

## Website

Die Projektseite liegt in `index.html` und wird mit GitHub Pages veröffentlicht. Die Pages-Quelle muss in den Repository-Einstellungen auf **GitHub Actions** gestellt sein, falls sie noch nicht aktiviert wurde.

## Projekt erstellen

1. .NET 8 SDK installieren.
2. Das Projektarchiv `ClickPulse-CSharp-Projekt-v3.zip` entpacken.
3. `ClickPulse/ClickPulse.sln` in Visual Studio 2022 öffnen oder im Projektordner folgenden Befehl ausführen:

```powershell
dotnet publish ClickPulse.csproj -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true -p:IncludeNativeLibrariesForSelfExtract=true -p:EnableCompressionInSingleFile=true
```

## Automatischer Build

Bei Änderungen am Projektarchiv oder am Build-Workflow führt GitHub Actions den Windows-Build aus und aktualisiert das Release. Der Workflow befindet sich unter `.github/workflows/build-release.yml`.

Verwende automatisierte Mausklicks nur in Anwendungen, in denen sie erlaubt sind.
