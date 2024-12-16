# Script PowerShell pour le Téléchargement FTP avec Notification par E-mail

Ce script PowerShell permet de télécharger un fichier depuis un serveur FTP et d'envoyer une notification par e-mail pour indiquer si l'opération a réussi ou échoué.

---

## Fonctionnalités
- Connexion à un serveur FTP.
- Téléchargement d'un fichier spécifié par l'utilisateur.
- Enregistrement du fichier dans un dossier local (avec création automatique si nécessaire).
- Notification par e-mail en cas de succès ou d'échec.

---

## Prérequis
1. **PowerShell**
   - Assurez-vous d'avoir PowerShell installé sur votre machine.
2. **Accès au serveur FTP**
   - Adresse du serveur FTP.
   - Chemin complet du fichier à télécharger.
3. **Configuration SMTP valide**
   - Fournissez une adresse e-mail valide pour l'envoi des notifications.
   - Si vous utilisez Gmail :
     - Activez "Applications moins sécurisées" ou utilisez un mot de passe d'application.

---

## Utilisation
1. Clonez ou téléchargez ce répertoire sur votre machine.
2. Exécutez le script dans PowerShell.
3. Suivez les instructions interactives :
   - Entrez l'adresse du serveur FTP (par ex., `ftp://172.29.229.246`).
   - Spécifiez le chemin complet du fichier à télécharger (par ex., `/srv/ftp/monarchive.tar.gz`).
4. Le fichier sera téléchargé dans `C:\archive` par défaut.

---

## Variables Clés
### À Modifier dans le Script :
- `$smtpServer` : Adresse du serveur SMTP (par ex., `smtp.gmail.com`).
- `$smtpPort` : Port SMTP (par ex., `587`).
- `$emailFrom` : Adresse e-mail de l'expéditeur.
- `$emailPassword` : Mot de passe de l'expéditeur (ou mot de passe d'application).
- `$adminEmail` : Adresse e-mail du destinataire des notifications.

---

## Exemple d'exécution
```plaintext
Entrez l'adresse du serveur FTP (par exemple, ftp://172.29.229.246) : ftp://172.29.229.246
Entrez le chemin complet du fichier sur le serveur FTP (par exemple, /srv/ftp/monarchive.tar.gz) : /srv/ftp/monarchive.tar.gz
Dossier local créé : C:\archive
Téléchargement en cours de : ftp://172.29.229.246/srv/ftp/monarchive.tar.gz
Téléchargement réussi.
E-mail envoyé avec succès.
```

---

## Gestion des Erreurs
### Scénarios Courants :
1. **Erreur d'authentification SMTP** :
   - Assurez-vous que l'adresse e-mail et le mot de passe sont corrects.
   - Si vous utilisez Gmail, activez "Applications moins sécurisées" ou créez un mot de passe d'application.

2. **Erreur d'accès FTP** :
   - Vérifiez que le fichier spécifié existe sur le serveur.
   - Assurez-vous que l'adresse FTP est correcte.

3. **Problèmes de Permissions Locales** :
   - Vérifiez que vous avez les droits pour créer des fichiers dans le dossier local.

---

## Licence
Ce projet est sous licence MIT. Vous êtes libre de l'utiliser et de le modifier selon vos besoins.


