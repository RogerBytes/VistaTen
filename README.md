
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
Une installation fraîche de Windows 11 (si vous voulez un dual boot avec un OS Linux il faut installer windows en premier).

https://docs.atlasos.net/getting-started/installation/#1-download-an-iso
Choisir "Download Windows 11 24h2" et choisir la langue puis cliquez suyr "submit"

POUR MACH8NE VIRTUELLE VIRTUYALVBOX
Penser à cocher "skip unatendeted"

une fois arrivé à l'écran des choix (là où ils demandent de se connecter à son compte)
Lors de l'installation de windows, il faut bypass la connexion en ligne, pour ouvrir un batch shell faites `SHIFT + F10`, puis faites la commande suivante :

```batch
oobe\BypassNRO
# après reboot, quand vous serez sur la page "comment souhaitez vous configurez cet appareil" vous aurez besoin de couper internet avec
ipconfig /release
```

Juste après la dernière commande, vous pouvez cliquer sur suivant, il fera un compte local.

Si ça marche pas, recommencez en coupant internet manuellement.

Ensuite, il faut mettre powershell comme terminal par défaut, `Win + X` puis `A`, tapez ensuite :

```batch
irm https://massgrave.dev/get | iex
```

Choisir l'option 1


POUR MACH8NE VIRTUELLE VIRTUYALVBOX
Une fois installer, aller sur "Aide A propos de virtualbox" pour voir la version., moi virtualbox 7.0.16
https://download.virtualbox.org/virtualbox/7.0.10/VBoxGuestAdditions_7.0.10.iso
Le monter via "Prefiphérique/lecteurs optiques/choose a disk vile" et pointer "VBoxGuestAdditions_7.0.10.iso"

Faire l'installation, reboot, et on peut ejecter le cd après

Dans virtualbox, dans configuration/Général/avancé, activer bidirectionnel pour "presse papier partagé et pour "glisser dépooser"
FIN VIRTUAL BOX MANPIE



INSTALLER ATLAS OS
LA DOC :
https://docs.atlasos.net/getting-started/installation/

En gros c'est bon, aller sur
https://atlasos.net/

Cliquer sur "Get Started Now" et choisir "I'm Following the guide, show me the downloads" en bas.
Cliquer sur ATLAS Playbook pour le DL
Cliquer sur AME Wizard pour le DL

Aller dans les parametres de windows, puis "Windows Update", rechercher les màj, et les faire toute, y compris facultatices, jusqu'à quy'il y en ai plus du tout
Ouvrir le microsoft store pour tout Màj (dans le bouton latéral "telechargements")
Penser à reboot et çà reverfier les màj de microsoft update et de microsoft store



Faire toutes les maj de windows, ouvrir le windows store, allez dans Bibliothèque et faites les màj, faites des reboot et reverifiez les maj system et store.

Ensuite ouvrir "AME Wizard Beta.exe" depuis "AME Wizard Beta"
Da,s le repertoir "AtlasPlaybook_v0.4.1" glissez "AtlasPlaybook_v0.4.1.apbx" dans la fenetre de l'app "AME WIZARD", opuis suivre les instructions

Poursuivez l'installation, choisissez waterfox comme navigateur. A la fin il va reboot de lui même.

Au reboot, Atlas sera installé. Mais on va poursuivre un peu plus.

Dans Atlas/1. Software/ :

Dans C:\Windows\AtlasDesktop\1. Software lancez Install Software.cmd  :

LibreWolf
Steam
Playnite
Everything
Mozilla Thunderbird
foobar2000
Git
PuTTY
Ditto
OBS Studio
MSI Afterburner
CPU-Z
GPU-Z
Notepad++
VSCodium
BCUninstaller
HWiNFO
ShareX
Powershell 7
UniGetUI


utiliser ce projet avec les options par défaut
`https://github.com/Raphire/Win11Debloat`

NORMALEMENT LA COMMAND ESRT : (dans powershell adminà)
& ([scriptblock]::Create((irm "https://win11debloat.raphi.re/")))

Ensuite il faut utiliser O&O ShutUp10++ depuis le site pour être à jour `https://www.oo-software.com/en/shutup10`
dans Actions choisir "Appliquer tous les paramètres recommendés" (il faut le refaire à chaque màj de windows)
Ensuite faire l'installation des drivers avec le site :

Sur la page `https://www.touslesdrivers.com/index.php?v_page=29`
Cliquez pour télécharger `Drivers_3.0.4.exe`
`Lancez Mes_Drivers_3.0.4.exe` et faites les installations de drivers
Installer et installer tous les drivers.

`Win + X` et `A` et faites

```batch
winget install startallback
```




ou téléchargez le depuis `http://www.startallback.com`

Dans startallback
démarrer -> cocher tout sauf "Ouvrir le menu de recherche Windows pour voir plus détails"
Barre des tâches -> Taille des icone "S" Marge des icone "S", Emplacement de la barre des tâches à l'écran" : Haut, et "Centrer les icones de programmes" (séparé du bouton de démarrage)
Icones de la barre des tâches -> Dans activer ou descativer des icones systeme activer tout sauf la loupe et le stylet;
	tout activer sauf "Panneau de détails dans la zone inférieure" et "Appliquer la couleur d'accentuation système sur tous les éléments", et mettre "XL" pour la marge des icones
Explorateur -> tout activer sauf "Panneau de détails dans la zone inférieure" et "Appliquer la couleur d'accentuation système sur tous les éléments"


Lancer "StartAllFix.exe" et pour trouver le fichier c'est dans `C:\Program Files\StartAllBack`
C'est dans ce dossier pour changer des options.

Sinon pour améliorer l'explorateur dans le dossier atlas c'est dans `3. Configuration/Start Menu/` et lancer "ExplorerPatcher" pour l'installer



%LOCALAPPDATA%\StartAllBack

StartAllBackCfg.exe

dans Avancé faire "Désactiver ce logiciel pour l(utilisateur actuel

https://github.com/WitherOrNot/StartXBack/releases/tag/release

Copy dll in

%LOCALAPPDATA%\StartAllBack

et lancer startxback.cmd
Attendre qu'il corrige le bug


%LOCALAPPDATA%\StartAllBack

StartAllBackCfg.exe

dans Avancé DECOCHER "Désactiver ce logiciel pour l(utilisateur actuel




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



SEMBLME FACLTATIF, DEJA INSTALLE EN PREREQUIS JE PENSE
Ouvrez powershell en administrateur avec 'Win+X' Puis 'A' :

```powershell
Get-ExecutionPolicy
```

puis :

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
PAS FADCULTATIF

Ensuite lancez "install executer en tant qu'administrateur.bat" via 'clic droit' "executer en mode administrateur"

### 3. Winget

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

### 4. Lecteur PDF

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

### 5. Cmder

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
{PowerShell::PowerShell as Admin}

### 6. Icônes et souris

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

### 7. Menu démarrer

Et faites un backup de menu démarrer start menu

`C:\ProgramData\Microsoft\Windows\Start Menu`

`%USERPROFILE%\AppData\Roaming\Microsoft\Windows\Start Menu`
dans
`C:\Program Files\Outils\Backup Menu demarrer`

Ensuite pouvez nettoyer la liste des applications sans craintes dans les deux dossiers.

### 8. Explorateur de fichiers

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

### 9. OldNewExplorer

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

### 10. Avoir les permissions sur les fichiers

Allez dans

`C:\Program Files\Outils\EcMenu`
Lancez EcMenu_x64.exe

Tout en bas
cochez "Prendre possession" dans "Menu contextuel des dossiers" et "Menu contextuel des fichiers"
Cliquez sur l'icone de souris avec un "+" vert en haut à gauche, et fermez.



### 11. Derniers réglages

Dans l'explorateur de fichiers clic droit sur "Accès rapide" dans la navbar à gauche et "Options"
Décochez "Afficher les dossiers récemment utilisés dans Accès rapide"

Dans CMDER
winget install -e --id VideoLAN.VLC

### 12. Finalité finale

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
8. Faire un dossier ToDO pour simplifier la gestion projet

</details>

___________________________________________________________________________

## Auteurs

- [Harry RICHMOND](https://github.com/RogerBytes)
