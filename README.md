
Comment puis-je convertir un fichier .pem en fichier .ppk, et inversement, sous Windows et Linux ?
Date de la dernière mise à jour : 2020-08-27

Comment puis-je convertir mon fichier Privacy Enhanced Mail (.pem) Amazon Elastic Compute Cloud (Amazon EC2) en fichier PuTTY Private Key (.ppk) ? Ou convertir un fichier .ppk en fichier .pem ?
Brève description
PuTTY ne prend pas en charge de manière native le format de clé privée (.pem) généré par Amazon EC2. Vous devez convertir votre clé privée en fichier .ppk avant de pouvoir vous connecter à votre instance à l'aide de PuTTY. Vous pouvez utiliser l'outil PuTTYgen pour effectuer cette conversion. 
Résolution
Windows - installer PuTTYgen

PuTTY est installé sur la plupart des systèmes d'exploitation Windows. Si ce n'est pas le cas de votre système, téléchargez et installez PuTTYgen.

Windows - convertir un fichier .pem en fichier .ppk

Démarrez PuTTYgen, puis convertissez le fichier .pem en fichier .ppk. Pour en savoir plus sur la marche à suivre, consultez la section Convertir votre clé privée à l'aide de PuTTYgen.

Windows – convertir un fichier .ppk en fichier .pem

Démarrez PuTTYgen. Pour Actions, sélectionnez Load (Charger), puis accédez à votre fichier .ppk.
Sélectionnez le fichier .ppk, puis Open (Ouvrir).
(Facultatif) Pour Key passphrase (Phrase clé secrète), entrez une phrase clé secrète. Pour Confirm passphrase (Confirmer la phrase clé secrète), saisissez à nouveau votre la phrase clé secrète.
Remarque :même si une phrase clé secrète n'est pas obligatoire, vous devez en spécifier une comme mesure de sécurité pour protéger la clé privée d’une utilisation non autorisée. L’utilisation d’une phrase clé secrète complique le processus d'automatisation, car une intervention humaine est nécessaire pour se connecter à une instance ou pour copier des fichiers vers une instance.
Dans le menu supérieur de PuTTY Key Generator, sélectionnez Conversions, Export OpenSSH Key (Exporter la clé OpenSSH).
Remarque : si vous n'avez pas saisi de phrase clé secrète, PuTTYgen générera un avertissement. Sélectionnez Yes (Oui).
Attribuez un nom au fichier et ajoutez l'extension .pem.
Sélectionnez « Save » (Enregistrer).


//////
VS code 
ajouter Extension Remote SSH
Open SSH configuration File

Host NOM_DE_LACONNECTION
    HostName ND DU VPS OU DE INSTANCE
    User NOM UTILISATEUR
    IdentityFile CHEMIN VERS LA CLE SOUS FORME PEM EX C:\Users\MONOM\.ssh\cle.pem


