# MovieX TV (Windows)

Application Windows autonome : rien à installer, le serveur est inclus.

## Installation (PowerShell)

```powershell
$ProgressPreference = 'SilentlyContinue'
$dir = "$env:LOCALAPPDATA\MovieX-TV"
New-Item -ItemType Directory -Force $dir | Out-Null
Invoke-WebRequest https://github.com/Flow-js-cloud/moviex-tv/releases/latest/download/MovieX-TV-Windows.zip -OutFile "$dir\app.zip"
Expand-Archive "$dir\app.zip" -DestinationPath $dir -Force
Remove-Item "$dir\app.zip"
Start-Process "$dir\MovieX TV-win32-x64\MovieX TV.exe"
```

Pour relancer plus tard : `Start-Process "$env:LOCALAPPDATA\MovieX-TV\MovieX TV-win32-x64\MovieX TV.exe"`

Pour mettre à jour : relancer la commande d'installation.

## Utilisation

- Bouger la souris fait apparaître les boutons en haut à droite (fenêtre/plein écran, fermer).
- `F11` : plein écran. `Échap` : retour. `Alt+F4` : fermer.
