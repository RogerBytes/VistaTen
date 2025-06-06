
# VistaTen

Ce script est conçu pour automatiser le processus de personnalisation de Windows 10 en installant une suite complète de logiciels open source. De manière simple, les utilisateurs peuvent transformer leur système Windows en un environnement léger pour le jeu vidéo.
A contrario une installation supplémentaire le transformera en un environnement de travail puissant et personnalisé, idéal pour les développeurs, les créateurs de contenu, et les utilisateurs quotidiens.

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
- **Internet**: Floorp, FileZilla
- ...et beaucoup d'autres !

### Contributions

Les contributions sont les bienvenues ! Si vous avez des suggestions ou des améliorations, n'hésitez pas à soumettre une pull request ou à ouvrir une issue.

### License

Distribué sous la licence GPLv3. Voir `LICENSE` pour plus d'informations.
</details>

___

## Prérequis



<details style="background-color: #222222; border: 1px solid #ccc; border-radius: 4px;">
<summary>Afficher/Masquer</summary>

### Installer Windows 11

Vous avez besoin d'une installation fraîche de Windows 11 (à installer avant linux si vous voulez un dual boot).
Personnellement j'utilise Windows 11 Professionnel.

**N'INSTALLEZ PAS UNE VERSION N DE WINDOWS SI VOUS VOULEZ AVOIR LES CODECS PROPRIÉTAIRES, CAR SANS CES DERNIERS VOUS NE POURREZ LIRE LES VIDÉOS DANS LE NAVIGATEUR ETC**


#### Téléchargement

Télchargez l'iso depuis [le site de AtlasOS](https://docs.atlasos.net/getting-started/installation/#1-download-an-iso)
Choisir "Download Windows 11 24h2" et choisir la langue puis cliquez sur "submit"

Une fois téléchargé, mettre l'iso sur votre clef de ventoy et boot sur celle ci pour installer windows.

POUR MACHINE VIRTUELLE VIRTUALBOX
<details style="background-color: #222222; border: 1px solid #ccc; border-radius: 4px;">
<summary>Afficher/Masquer</summary>
Pensez à cocher `skip unatendeted`
</details>


une fois arrivé de connexion WIFI, **ne vous connectez pas sinon votre ordi sera lié automatiquement à un compte microsoft** pour des raisons de vie privée, je vous recommande de faire un compte local en bypassant l'obligation d'être connécté à internet pour installer window.  
Ouvrez un terminal avec `SHIFT + F10`, puis faites la commande suivante :

```powershell
oobe\BypassNRO
```

Juste après la dernière commande, il va relancer ce coup-ci vous pourrez passer outre la connexion.

Si ça marche pas, recommencez en coupant internet manuellement avec

```powershell
ipconfig /release
```

Et poursuivez l'installation de Windows.

### Drivers

Voilà, windows est bien installé, vous pouvez vous connecter au wifi ou au réseau, votre compte est bien en local.  

Attention à bien noter les étapes en notant quel matériel et quel driver vous installez, très utile en cas de soucis de driver

Sur la page `https://www.touslesdrivers.com/index.php?v_page=29`
Cliquez pour télécharger `Drivers_3.0.4.exe`
`Lancez Mes_Drivers_3.0.4.exe` et faites les installations de drivers
Installer et installer tous les drivers.

Faites les maj de windows update et de Microsoft Store

Ensuite, il faut valider avec `Win + X` puis `A`, tapez ensuite dans la fenêtre :

```powershell
irm https://get.activated.win | iex
```

Choisissez l'option `1`.
Si besoin allez dans `2` pour installer microsoft office.

POUR MACHINE VIRTUELLE VIRTUALBOX
<details style="background-color: #222222; border: 1px solid #ccc; border-radius: 4px;">
<summary>Afficher/Masquer</summary>
Une fois installé, allez sur `Aide A propos de virtualbox` pour voir la version, chez moi c'est `virtualbox 7.0.16`.

Donc en après avoir cherché [ici](https://download.virtualbox.org/virtualbox/), j'ai bien un `VBoxGuestAdditions_7.0.16.iso` dans `7.0.16`
Donc le lien est [https://download.virtualbox.org/virtualbox/7.0.16/VBoxGuestAdditions_7.0.16.iso](https://download.virtualbox.org/virtualbox/7.0.16/VBoxGuestAdditions_7.0.16.iso)

Le monter via "Prefiphérique/lecteurs optiques/choose a disk vile" et pointer "VBoxGuestAdditions_7.0.16.iso"

Faire l'installation, reboot, et on peut ejecter le cd après

Dans virtualbox, dans configuration/Général/avancé, activer bidirectionnel pour "presse papier partagé et pour "glisser dépooser"
</details>


### Installer AtlasOS

LA DOC :
https://docs.atlasos.net/getting-started/installation/

En gros c'est bon, vous pouvez aller sur [atlasos.net](https://atlasos.net/)


Cliquez sur `Get Started Now` et choisissez `I'm Following the guide, show me the downloads` en bas.  
Cliquer sur `ATLAS Playbook` pour le DL.  
Cliquer sur `AME Wizard` pour le DL

Aller dans les parametres de windows, puis "Windows Update", rechercher les màj, et les faire toute, y compris facultatices, jusqu'à ce qu'il n'y en ai plus du tout.  
Ouvrir le microsoft store pour tout Màj (dans le bouton latéral "telechargements").  
Penser à reboot et çà reverfier les màj de microsoft update et de microsoft store.  
Vérifiez une dernière fois que toutes les maj de windows sont faites.


Ensuite ouvrir `AME Wizard Beta.exe` depuis `AME Wizard Beta`.
Dans le repertoire `AtlasPlaybook_v0.4.1` glissez `AtlasPlaybook_v*.*.*.apbx` dans la fenetre de l'app `AME WIZARD`, puis suivez les instructions.

Poursuivez l'installation, choisissez waterfox comme navigateur. A la fin il va reboot de lui même.

### Dernier néttoyage de Windows

Au reboot, Atlas sera installé. Mais on va poursuivre un peu plus.

Ensuite faire :  
```powershell
& ([scriptblock]::Create((irm "https://debloat.raphi.re/")))
```

Choisissez l'option 1.

Ensuite il faut utiliser `O&O ShutUp10++` depuis [leur site](https://www.oo-software.com/en/shutup10).
Ensuite lancez le et dans `Actions` choisissez `Appliquer tous les paramètres recommendés` (il vous faudra le refaire à chaque màj de windows)  
Fermez `O&O ShutUp10++` et acceptez de redémarrer quand il vous le propose.
</details>

___

## Installation


<details style="background-color: #222222; border: 1px solid #ccc; border-radius: 4px;">
<summary>Afficher/Masquer</summary>

Téléchargez [la dernière version de VistaTen](https://github.com/RogerBytes/VistaTen/releases/latest).  
Décompressez l'archive.

### 1. Utilitaires  basiques

copiez `Outils` dans `C:\Program Files`  
Créez 4 dossier de téléchargement dans le dossier `Téléchargements` :  
- Téléchargements navigateur
- Téléchargements JD
- Téléchargements torrent
- Téléchargements ferdium

Dans `Installeurs` installez `nexus dock`, copiez `wsbackup.wbk` dans `C:\Users\Public\Documents\Winstep\Backup`  
et importez les réglages dans l' avant dernière fenêtre d'options (`CTRL` + `clic droit` et `Préférences`) avec le bouton `Restaurer` (il sera caché pour l'instant, c'est normal).  
Décompressez `FoxitPDFReader20232_L10N_Setup_Prom.7z.001` avec `nanazip` et installez `JDownloaderSetup.exe`, `FoxitPDFReader20232_L10N_Setup_Prom.exe` et `pCloud_Windows_3.11.17_x64.exe` 

Dans jdownloader faire l'importation des options : dans `Fichier` choisissez `Export/Import` et `Importez les paramètres` et choisissez `JD2-Dark-Theme.jd2backup`, pensez à corriger le chemin de téléchargements.

**En passant, ne déplacez le dossier utilisateur sur une autre partition, j'ai déjà voulu le faire dans l'espoir de fusionner mes dossier user entre mon système linux et mon système windows, ça va détruire tous les liens logiques de windows en rendre inutilisable de nombreuses applications**


### 2. Chocolatey

Infos depuis [cette page](https://chocolatey.org/install#individual)

`WIN+X` puis `A`, ça ouvre le PowerShell

On vérifie si  `Get-ExecutionPolicy` retourne "Unrestricted" sinon utiliser la commande `Set-ExecutionPolicy AllSigned` ou `Set-ExecutionPolicy Bypass -Scope Process`

Ensuite lancer l'installation avec :
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Lancez `install executer en tant qu'administrateur.bat` via `clic droit` et `executer en mode administrateur`


### 3. Winget

Commande pour lister les dépôts dans cmder

```batch
winget search | sort
```

Dans le powershell en administrateur, importez les pré réglages avec

```powershell
winget import -i "C:\Program Files\Outils\winget.json" --accept-package-agreements --accept-source-agreements
winget install --id 9WZDNCRDR0C2  --accept-package-agreements --accept-source-agreements
```

Ensuite dans un powershell non admin le refaire.

Le faire au moins 2x de suite pour être sûr d'avoir tout récupéré, en ce moment se relance seulement portmaster.

Facultatif, si vous voulez exporter votre propre liste d'app :

```powershell
winget export "C:\Program Files\Outils\winget.json"
```

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

### 8. Fix pour regroupement auto de l'explorateur de fichiers

Téléchez ce [logiciel](https://lesferch.github.io/WinSetView/

Lancer "WinSetView-Setup.exe" et faire l'installation

Lance-le.

Il suffit de regarder la 1er partie "Global"
Le mettre sur "Détails", le par groupe est sur (Aucun), il suffit de cliquer sur le bouton "Soumettre", ça va régler la vue pour l'explorateur

Ca évite, dans l'explorateur, de faire à chaque dossier : 'clic droit'/Regrouper par/Aucun


### 9. Plugin son

déplacer ear trumpet aussi
Dans la barre du haut allez dans le sous menu masqué et remplacer l'icone du son par celle de ear trumpet


### 10. Réglage du menu OpenShell

Ouvrir open shell, aller dans ses paramètres, activer "show all settings" et aller dans l'onglet "Main Menu", dans la partie (la première) "All Programs style" cocher "Open Automatically"

Puis ok, fermer, allez dans
C:\Program Files\Open-Shell\

et supprimer 
ClassicExplorer64.dll
ClassicExplorer32.dll


ENSUITE installer StartIsBack avec la commande

```powershell
winget install StartIsBack.StartAllBack --scope machine
```


Les options de StartAllBlack s'ouvrent (sinon les ouvrir depuis
C:\Program Files\StartAllBack et StartAllBackCfg.exe )

allez dans l'onglet "Démarrer" et décochez (tout en haut la 1ere options) "Utiliser le menu démarrer classique amélioré"

Faites les réglages de barre, à ajouter dans les modif dureadme VERFIER CE QUI SUIT ----> -> ->
Dans startallback  
démarrer -> cocher tout sauf "Ouvrir le menu de recherche Windows pour voir plus détails"  
Barre des tâches -> Taille des icone "S" Marge des icone "S", Emplacement de la barre des tâches à l'écran" : Haut, et "Centrer les icones de programmes" (séparé du bouton de démarrage)  
Icones de la barre des tâches -> Dans activer ou descativer des icones systeme activer tout sauf la loupe, clavier tactile et le stylet;  
	tout activer sauf "Panneau de détails dans la zone inférieure" et "Appliquer la couleur d'accentuation système sur tous les éléments", et mettre "XL" pour la marge des icones  
Explorateur -> tout activer sauf "Panneau de détails dans la zone inférieure" et "Appliquer la couleur d'accentuation système sur tous les éléments", choisir barre de commande de windows 7  

Sinon pour améliorer l'explorateur dans le dossier atlas c'est dans `4. iNTRERFACE TWEAKS/Start Menu/` et lancer "ExplorerPatcher" pour l'installer  
ET AUSSI LE TAKE OWNERSHIPT DANS "4. iNTRERFACE TWEAKS/CONTEXT MENU/`"


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
