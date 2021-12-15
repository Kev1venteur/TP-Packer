## Prérequis
Installer toutes les dépendanes de virtualisation.
```bash
dnf install '@Virtualization Host'
```
Vérifier que l'IP [ici](rocky-8.pkr.hcl#L22) correspond à l'adresse donnée par la commande :
```bash
hostname -I
```

## Kickstart

```BASH
# Cloner le repo
git clone git@github.com:Kev1venteur/TP-Packer.git && cd TP-Packer

# Lancer le build packer 
packer build rocky-8.pkr.hcl

# Le mot de passe de la vm créée par packer est %Serveur44
``` 

## Debug

#### Augmenter le niveau de log de packer

Avant de lancer Packer définissez la variable d'environnement 'PACKER_LOG'.

```bash
export PACKER_LOG=1
```
