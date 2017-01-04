# junest-wine-min-install
arch-linux et wine a l'iut (implique un gestionnaire de paquets et des droits root)

ATTENTION : Il faut environ 1.5 Go d'espace libre pour cette installation. 

Note : Cette installation va créer un .junest dans votre home.

On va avoir besoin de Junest

```
git clone https://github.com/fsquillace/junest
```

(Optionnel) Pour mettre junest dans la variable path et pouvoir le lancer de n'importe ou:

```
export PATH=~/CHEMIN_VERS_JUNEST/junest/bin:$PATH
```

Même si junest est dans la variable PATH, il faut le lancer avec -f pour pouvoir installer des paquets
Exemple sans avoir mis dans la variable path :

```
./junest/bin/junest -f
```

La première fois un téléchargement va être effectué.
A la fin de la procédure votre terminal va avoir changé (l'utilisateur sera root).
Junest utilise Archlinux (donc pas de apt-get mais pacman).

On va devoir installer nano :

```
pacman -Syy nano
```

On v a avoir besoin de modifier la conf de pacman :

```
nano /etc/pacman.conf
```

décommenter les deux lignes de multilib
( 'ctrl-x' puis 'y' puis la touche entrée pour sauvegarder et sortir)

Mise à jour du Arch Linux PGP keyring :

```
pacman -Syy archlinux-keyring
```

Pour finir, on l'installation de wine :

```
pacman -S wine
```

prendre les valeurs par défauts (appuyer deux fois sur entrée) et installer.

Note : ```exit``` pour quitter Junest.
