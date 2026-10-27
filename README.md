# Relief pour macOS

Relief lit une montre Garmin en USB (lecture seule) ou des fichiers FIT, et les rend lisibles : activités, records sur
1, 5 et 10 km, totaux par semaine ISO, temps par zone cardiaque, allure, mesures de santé. Les données restent sur le Mac.
Aucun compte, aucune télémétrie. Application indépendante, non affiliée à Garmin.

Ce dépôt ne contient que les versions à installer. Le code source n'est pas public.

## Ce qu'il faut

- un Mac à puce Apple (M1 ou plus récent) ;
- macOS 26 ou plus.

## Installer

Dans Terminal (Cmd + Espace, « Terminal »), une seule commande, qui installe aussi les mises à jour :

```
curl -fsSL https://raw.githubusercontent.com/LucasHRCHatReply/relief-releases/main/installer.sh | zsh
```

Le script télécharge la dernière version, vérifie l'empreinte SHA-256 du zip, l'identifiant de l'app et sa signature
(équipe Apple `JT9FY7PP7K`, `codesign --verify --deep --strict`), copie l'app dans ~/Applications, puis l'ouvre.
Une fois installée, Relief propose elle-même ses mises à jour (onglet « Mises à jour », mêmes contrôles).

Autre voie : télécharger `Relief.dmg` dans les [Releases](../../releases/latest), l'ouvrir, glisser Relief sur
Applications. Le disque est signé, non notarisé : au premier lancement, clic droit sur l'app › Ouvrir.
