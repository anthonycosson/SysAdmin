# Gestion des utilisateurs

## En ligne de commande

### Créer un USERNAME admin : 


* dscl . -create /Users/USERNAME
* dscl . -create /Users/USERNAME UserShell /bin/bash
* dscl . -create /Users/USERNAME RealName "Prénom Nom"
* dscl . -create /Users/USERNAME UniqueID "1050"
* dscl . -create /Users/USERNAME PrimaryGroupID 80
* dscl . -create /Users/USERNAME NFSHomeDirectory /Users/USERNAME
* dscl . -append /Groups/admin GroupMembership USERNAME
* dscl . -passwd /Users/USERNAME PASSWORD

Autres commandes :

* Lister les comptes utilisateurs : dscl . list /Users grep -v “^_”
* Pour vérifier les comptes admin : dscacheutil -q group -a name admin
* Supprimer un compte utilisateur : sudo /usr/bin/dscl . -delete "/Users/USERNAME"
* Pour passer un compte admin en utilisateur standard : sudo dseditgroup -o edit -d NOMDUUSER -t user admin














