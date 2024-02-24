
# VistaTen

Ce script est conçu pour automatiser le processus de personnalisation de Windows 10 en installant une suite complète de logiciels open source. De manière simple, les utilisateurs peuvent transformer leur système Windows en un environnement léger pour le jeu vidéo.
A contrario une installation supplémentaire le transformera en un environnement de travail puissant et personnalisé, idéal pour les développeurs, les créateurs de contenu, et les utilisateurs quotidiens.
<details>
<summary>A régler avant première release</summary>

1. Installeurs/FoxitPDFReader20232_L10N_Setup_Prom.7z.001 en deux parties à décompresser
2. Faire une version light
3. Reformuler la documentation au propre, en s'inspirant par exemple de l'extrait suivant :

<details>
<summary>Exemple</summary>
Pour démarrer avec le script de personnalisation de Linux Mint, suivez ces étapes simples :

1. Téléchargez le script sur votre machine Linux Mint.
2. Rendez le script exécutable avec la commande : `chmod +x custom-linux-mint.sh`.
3. Exécutez le script avec : `./custom-linux-mint.sh`.

</details>
</details>

## Présentation

<details style="background-color: #222222; border: 1px solid #ccc; border-radius: 4px;">
<summary>Afficher/Masquer</summary>

### Fonctionnalités

- **Installation Semi-Automatique** : Déployez votre environnement personnalisé avec le minimum d'intervention manuelle.
- **Suite Complète** : Le script inclut une suite minimale, idéal pour les joueurs de jeux-vidéos.
- **Suite Complète** : Le script inclut des logiciels pour le développement, la bureautique, le multimédia, et plus encore.
- **Open Source** : Tous (ou prou) les logiciels installés sont open source, garantissant transparence et respect de la vie privée.
- **Thème Préconfiguré** : Profitez d'un thème sobre et fonctionnel, conçu pour une expérience utilisateur optimale.

### Liste de logiciels

Une liste non exhaustive des logiciels inclus dans ce script :

- **Développement**: Codium, Git
- **Bureautique**: LibreOffice, Thunderbird
- **Multimédia**: GIMP, Kodi
- **Internet**: Vivaldi, FileZilla
- ...et beaucoup d'autres !

### Contributions

Les contributions sont les bienvenues ! Si vous avez des suggestions ou des améliorations, n'hésitez pas à soumettre une pull request ou à ouvrir une issue.

### License

Distribué sous la licence GPLv3. Voir `LICENSE` pour plus d'informations.
</details>

___________________________________________________________________________

## Prérequis

<details style="background-color: #222222; border: 1px solid #ccc; border-radius: 4px;">
<summary>Afficher/Masquer</summary>
Une installation fraîche de Windows 10 (si vous voulez un dual boot avec un OS Linux il faut installer windows en premier).  
Lors de l'installation de windows, il faut bypass la connexion en ligne, pour ouvrir un batch shell faites `SHIFT + F10`, puis faites la commande suivante :

```batch
oobe\BypassNRO
# après reboot, quand vous serez sur la page "comment souhaitez vous configurez cet appareil" vous aurez besoin de couper internet avec
ipconfig /release
```

Juste après la dernière commande, vous pouvez cliquer sur suivant, il fera un compte local.

Ensuite, il faut mettre powershell comme terminal par défaut, `Win + X` puis `A`, tapez ensuite :

```batch
irm https://massgrave.dev/get | iex
```

Faire toutes les maj de windows, ouvrir le windows store, allez dans Bibliothèque et faites les màj, faites des reboot et reverifiez les maj system et store.

Puis 1, vous permettant de vérifier l'état de l'installation.

Ensuite dans edge, aller dans  
atlasos.net  
Cliquez sur les deux liens en haut "Atlas Playbook" et "AME Wizard"  
Décompressez les deux fichiers sur votre bureau

Restart after all updates are complete. After restarting, check again for updates repeatedly until there are no more updates that pop up

Allez dans le dossier "AME Wizard Beta"
et lancez `AME Wizard Beta.exe`
En haut à droite, vérifiez que le programme n'a pas de mise à jour.
Depuis le dossier "AtlasPlaybook_v*.*.*" glissez le fichier `AtlasPlaybook_v*.*.*.apbx` dans la fenêtre de AME Wizard.
Suivez les indications de l'installateur après avoir cliqué sur "Run action" de "Disable Security"
Ca vous ouvre une fenêtre dans les options de sécurité (j'ai oublié le nom fr) où vous aurez 4 options à désactiver.  

Poursuivez l'installation, choisissez waterfox comme navigateur. A la fin il va reboot de lui même.

Au reboot, Atlas sera installé. Mais on va poursuivre un peu plus.

Dans Atlas/1. Software/ :

1. Lancez "Install Software.ps1" et choisissez

- Discord
- Playnite
- Everything
- Mozilla Thunderbird
- foobar2000
- Git
- PuTTY
- Ditto
- 7-Zip
- OBS Studio
- MSI Afterburner
- CPU-Z
- GPU-Z
- Notepad++
- VSCodium
- BCUninstaller
- HWiNFO
- ShareX

Playnite demande de désactiver nahimic, il faut faire `Win + R` et taper "services.msc", l'arrêter dans la liste, et via clic droit propriété, le dtype d démarrage sur "désactiver"

utiliser ce projet avec les options par défaut
https://github.com/Raphire/Win11Debloat

Ensuite il faut utiliser O&O ShutUp10++ depuis le site pour être à jour https://www.oo-software.com/en/shutup10
dans Actions choisir "Appliquer tous les paramètres recommendés" (il faut le refaire à chaque màj de windows)
Ensuite faire l'installation des drivers avec le site :

Sur la page `https://www.touslesdrivers.com/index.php?v_page=29`
Cliquez pour télécharger `Drivers_3.0.4.exe`
`Lancez Mes_Drivers_3.0.4.exe` et faites les installations de drivers

</details>

___________________________________________________________________________

## Installation

<details style="background-color: #222222; border: 1px solid #ccc; border-radius: 4px;">
<summary>Afficher/Masquer</summary>

### 1. Utilitaires  basiques

copiez "Outils" dans
C:\Program Files
Créez 4 dossier de téléchargement dans le dossier "Téléchargements"
Téléchargements navigateur
Téléchargements JD
Téléchargements torrent
Téléchargements ferdium

dans "Installeurs" installez nexus dock, copiez "wsbackup.wbk" dans
C:\Users\Public\Documents\Winstep
et importez les réglages dans l' avant dernière fenêtre d'options avec le bouton "Restaurer"
Installez également "JDownloaderSetup.exe", "FoxitPDFReader20232_L10N_Setup_Prom.exe" et "pCloud_Windows_3.11.17_x64.exe"
C:\Program Files (x86)\Foxit Software\Foxit PDF Reader

Dans jdownloader faire l'importation des options : dans 'Fichier choisissez "Export/Import" et "Importez les paramètres" et choisissez "JD2-Dark-Theme.jd2backup",
Pensez à corriger le chemin de téléchargements.

Attention JE VOUS D2CONSEILLE de Déplacer le dossier utilisateur sur une autre partition, si vous devez passer par un shell ça va foutre en l'air vos liens système et niquer possiblement d'autre processus côté back, ewindows c'est de la merde.

### 2. Chocolatey

Ouvrez powershell en administrateur avec 'Win+X' Puis 'A' :

```powershell
Get-ExecutionPolicy
```

puis :

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('<https://chocolatey.org/install.ps1>'))
```

Ensuite lancez "install executer en tant qu'administrateur.bat" via 'clic droit' "executer en mode administrateur"

### 3. Debloater et shutup10

Ouvrez powershell en administrateur 'WIN+X' puis 'A'

puis
Set-ExecutionPolicy Unrestricted -Force

puis
cd "C:\Program Files\Outils\Windows10Debloater"
copiez le chemin où se trouve Windows10Debloater

puis
./Windows10DebloaterGUI.ps1

Et choisissez ce que vous voulez nettoyer.
Chez moi
"Remove All Bloatware"
"Disable Cortana"
"Stop Edge PDF Takeover"
"Uninstall OneDrive"
"Disable Telemetry/Tasks"
"Enable dark theme"

Fermez la fenêtre et le powershell,
dans
C:\Program Files\Outils
lancez "OSU10.exe"
Aller dans "Actions" et choisir "Appliquer tous les paramètres recommandés", puis "OUI"
Fermez et choisissez "Redémarrer le système".

### 4. Winget

Installez le depuis le microsoft store (recherche "winget" et choisissez "Programme d'installation d'application"
Redémmarez
Commande pour lister les dépôts dans cmder

```batch
winget search | sort
```

Dans le powershell en administrateur, importez les pré réglages avec

```powershell
winget import --accept-package-agreements --accept-source-agreements "C:\Program Files\Outils\winget.txt"
```

Ensuite dans un powershell non admin le refaire.

Le faire au moins 2x de suite pour être sûr d'avoir tout récupéré, en ce moment se relance seulement portmaster.

Facultatif, si vous voulez exporter votre propre liste d'app :

```powershell
winget export "C:\Program Files\Outils\winget.txt"
```

et la radio à installer depuis [apps.microsoft.com](https://apps.microsoft.com/store/detail/9WZDNCRDR0C2?hl=fr-fr&gl=FR)

dans
`C:\Program Files\Outils`
`Lancez Mes_Drivers_3.0.4.exe` et faites les installations de drivers

Et lancez imageGlass depuis le menu et faite les confirmations du premier démarrage, mettez le par défaut quand demandé.

### 5. Lecteur PDF

Pour Foxit reader ouvrez-le, avec la commande

```batch
"C:\Program Files (x86)\Foxit Software\Foxit PDF Reader\FoxitPDFReader.exe"
Choisir "set as default pdf reader"
```

Aller dans "File/Preferences"
"Language" et cochez "Use system local language" puis "OK" et "Restart Now"
Aller dans Fichiers/Préférences
Dans "Accessibilité
Cocher "Remplacer les couleurs du document"
Cocher "Couleur personnalisé"
Mettre arrière-plan de page en noir
Mettre texte du document en blanc
Aller dans l'onglet "Général"
Tout en bas tout décocher dans l'encadré "Démarrage de l'application"
Cocher "Désactiver toutes les fonctionnalités qui exigent une connexion à internet"
Cliquer sur "OK" et quitter
Allez en haut à gauche, Fichier, Apparence, et choisir "sombre"

### 6. Cmder

Ouvrez Cmder, allez dans les options avec 'Win+Alt+P"

Allez dans "General>Confirm" et décochez le dernier de la liste (dans "miscellaneous") :
"Show '...brought ConEmu OnTop. Revert' confirmation box"

Cliquez sur "Save settings"

Redémmarez

après reboot faire une màj avec

```batch
clink update
```

Win+Alt+P et aller dans "General/Confirm"
et décochez en bas "Show`...brought ConEmu OnTop. Revert ?` confirmation box.

Ensuite
dans "General" aller à "Choose your startup task" et mettez
{Shells::cmd (Admin)}

### 7. Démarrage rapide

Je recommande aussi de désactiver le démarrage rapide de windows, ou plutôt c'est indispensable si vous comptez avoir plusieurs OS sur votre ordinateur.

Allez dans les options d'arrêt avec la commande

```batch
%windir%\system32\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings
```

ou en allant dans
`Panneau de configuration\Matériel et audio\Options d’alimentation\Paramètres système`

Cliquez sur "Modifier les paramètres actuellement non disponibles"
Décochez le bouton "Activer le démarrage rapide (recommandé)" puis sur "Enregistrer les modifications"

### 8. Icônes et souris

Allez dans
`C:\Program Files\Outils\icones\Souris theme la capitaine`
'Clic droit' sur "install.inf" et "Installer"
Ensuite clic droit sur le bureau et choisissez "personnaliser", puis dans "Thèmes" et
cliquez sur "Curseur de la souris"
Pointez le fichier "install.inf" se trouvant dans le dossier "souris"
Dans l'onglet "Pointeurs" choisissez dans "Modèles" le thème "Capitaine Cursors"
Dans l'onglet "Options du pointeur" décochez "Améliorer la précision du pointeur"
Profitez en pour régler la vitesse de votre souris si besoin (800 dps est bien en passant
si vous avez un logiciel tier)
Cliquez sur "Appliquer" et "OK"

`C:\Program Files\Outils\icones\7tsp GUI v0.6(2019).exe`
Cliquez sur "ajouter un pack" et dans
C:\Program Files\Outils\icones
Choisissez "7TSP Kora"
Ensuite cliquez sur "Démarrage" en bas à droite.
L'ordi redémmarre avec les nouvelles icones.

### 9. Menu démarrer

Et faites un backup de menu démarrer start menu

`C:\ProgramData\Microsoft\Windows\Start Menu`

`%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Start Menu`
dans
`C:\Program Files\Outils\Backup Menu demarrer`

Ensuite pouvez nettoyer la liste des applications sans craintes dans les deux dossiers.

### 10. Explorateur de fichiers

Pour revenir à un affichage plus conventionnel, sans groupes, cliquez du bouton droit sur une zone inoccupée de l’explorateur de fichiers, pointez Regrouper par et cliquez sur (aucun) :

Pour avoir un menu à l'ancienne et des fenêtres d'explorateur plus sobres, dans "StartIsBack"
`%USERPROFILE%\Desktop\Windows CALM\StartIsBack`
lancez "StartIsBack-2.9.17.0"

Pour rechanger des options c'est dans
`C:\Program Files\Outils`
StartIsBackCfg.exe
Lancez-le

Menu démarrer
Ne cocher que "Rechercher dans les programmes et les paramètres.
Cacher tous les éléments de la colonne de droite sauf votre nom d'utilisateur, panneau de configuration et paramètres.

Menu Apparence
Le 2e
Le 1e
Le 1e
Tout décocher
Allez dans (en bas) "personnaliser la barre des tâches" et cocher "Centrer les icones dans la barre des taches"

Règle d'affichage
Ne cocher que "L'afficher sur la barre des tâches principales"

Avancé
Ne cocher que "Activer les animations du menu Démarrer et de la barre des tâches"

A propos
Mises à jour : ne jamais vérifier.

Fermez le logiciel

Puis 'clic droit' sur la barre de menu, "Paramètres de la barre des tâches"

Cochez
"Utilisez des petits boutons dans la barre des tâches
Et position de la barre des tâches, choisissez "En Haut"
Décochez "Afficher les actualités et les centres d'intérêt dans la barre des tâches"

Puis 'clic droit' sur la barre de menu, décochez "Afficher le bouton Cortana"
Puis 'clic droit' sur la barre de menu, "Rechercher" et choisissez "Masquée"

Puis 'clic droit' sur un endroit vide du bureau, "Personnaliser"

Allez dans Couleur et "Choisissez votre couleur" = Sombre
Descendez la fenêtre jusqu'à "Couleurs Windows" et cliquez sur "Couleur personnalisée"
"Plus"
et entrez
`#191919`
Puis "OK"

Cochez (juste en dessous) :
Démarrer,barre des tâches et centre de notifications
Barre de titre et bordures de fenêtres

### 11. OldNewExplorer

Dans
`C:\Program Files\Outils\OldNewExplorer`
lancer "OldNewExplorerCfg.exe"

Cocher seulement

Use classical drive grouping in This PC
Use command bar instead of Ribbon
Hide caption text in File Explorer windows
Hide caption icon in File Explorer windows
Show status bar

puis "Install"

### 12. Avoir les permissions sur les fichiers

Allez dans

`C:\Program Files\Outils\EcMenu`
Lancez EcMenu_x64.exe

Tout en bas
cochez "Prendre possession" dans "Menu contextuel des dossiers" et "Menu contextuel des fichiers"
Cliquez sur l'icone de souris avec un "+" vert en haut à gauche, et fermez.

### 13. Enlever la barre de commande

Allez dans
`%windir%\Resources\Themes\Aero\Shell\NormalColor`

C'est le thème par défaut, changez le répertoire si vous en utilisez un autre (il sont généralement déjà patchés).
Copiez "shellstyle.dll" sur votre bureau

Dans
`C:\Program Files\Outils\Resource Hacker`
Lancez ResourceHacker.exe, puis 'CTRL+0'

Allez dans
`%windir%\Resources\Themes\Aero\Shell\NormalColor`
C'est le thème par défaut, changez le répertoire si vous en utilisez un autre (il sont généralement déjà patchés).
et choisissez shellstyle.dll sur le bureau

Allez dans
`UIFILE > 1 : 1033`

'CTRL+F' et copiez

```bash
<style resid="FolderBandStyle">
```

Juste en dessous de la ligne copiez :

```bash
<Element padding="rect(0rp,0rp,0rp,-35rp)"/>
```

F5 pour lancer la compilation
dans la fenêtre de ressource hacker, allez dans "File/save as" et sauvez le ailleurs.

et CTRL + S pour sauvegarder, il créera une archive "shellstyle_original.dll" sur le bureau.

Allez dans
`%windir%\Resources\Themes\Aero\Shell\NormalColor`
Clic droit sur shellstyle.dll et "Prendre possession"
renommez "shellstyle.dll" en "shellstyle_default.dll"

Et copiez le nouveau "shellstyle.dll"

Ensuite lancez cmder

```batch
taskkill /f /im explorer.exe
```

puis relancer l'explorateur de fichier avec

```batch
start explorer.exe
```

Ensuite dans l'explorateur de fichier on va cacher la 2e barre d'état :
'Alt' le menu apparaît,on va dans "Outils/Options des dossiers..." allez dans l'onglet "Affichage",
et décochez "Afficher la barre d'état".

### 14. Derniers réglages

Dans l'explorateur de fichiers clic droit sur "Accès rapide" dans la navbar à gauche et "Options"
Décochez "Afficher les dossiers récemment utilisés dans Accès rapide"

Dans Cmder en mode administrateur

```batch
C:\ProgramData\chocolatey\lib\mpv.install\tools\mpv-install.bat
```

Dans la fenêtre qui s'ouvre choisir "Configurer les programmes par défaut"

Courrier = Thunderbird

Lecteur de musique = foobar2000

Visionneuse de photo = ImageGlass

Lecteur vidéo = mpv

Naviguateur web = Vivaldi

### 15. Le theme

[deviantart.com/niivu](https://www.deviantart.com/niivu/art/Installing-Windows-Themes-UPDATED-708835586)
[deviantart.com/niivu/art/](https://www.deviantart.com/niivu/art/ARC-X-for-Windows-10-772549960)

le theme ARC X marche que pour windows 10

pour voir la version 'Win+R' puis 'winver'

Sinon pour le theme j'utilise "ThemeTool.exe" de https://github.com/namazso/SecureUxTheme

Allez dans
`C:\Program Files\Outils\theme\ARC X`
Dans BIB3 for Windows copiez les fichiers dans
Windows/Resources/Themes

Lancez "ThemeTool.exe" en admin via clic droit,
Cochez tout sauf "ignore color"
choisisissez "Arc Dark" puis "Patch & Apply"
Dans l'encadré "Installation"
Cochez tout sauf "Hook explorer(!)", puis "Install"

Ca redémarre
L'install est faite proprement

### 16. Finalité finale

afficher les extensions
Dans l'explorateur de fichiers, alt pour faire apparaître la barre de menu puis outils/ "Options de dossiers", "Affichage"
et décochez "Masquer les extensions de fichiers dont le type est connu"

déplacer ear trumpet aussi
Dans la barre du haut allez dans le sous menu masqué et remplacer l'icone du son par celle de ear trumpet
</details>

___________________________________________________________________________

## Todo

<details style="background-color: #222222; border: 1px solid #ccc; border-radius: 4px;">
<summary>Afficher/Masquer</summary>

1. Faire un script de customisation pour une nouvelle session
2. Faire un script pour rétablir les customisations de thème après une upgrade hasardeuse
3. Corriger le lien des MDP de Vivaldi, et ajouter les options corrigées de ~/.config/vivaldi à l'archive
4. Supprimer du .hidden le dossier Games
5. Refaire le lisez-moi
6. Faire la liste de toutes les applications
7. Faire une application simple pour changer sa version de Java

</details>

___________________________________________________________________________

## Auteurs

- [Harry RICHMOND](https://github.com/RogerBytes)
