Test JavaMail API
Ce projet utilise l'API JavaMail pour vérifier la réception d'un email provenant de l'expéditeur customer@mobilosoft.com dans un compte Outlook. Il récupère le contenu du message pour tester la configuration de l'API JavaMail.

🔧 Prérequis
Avant de commencer, assurez-vous que vous avez installé les éléments suivants :

Java 8 ou version supérieure : Vous pouvez vérifier la version de Java avec la commande java -version.

Maven : Pour gérer les dépendances et exécuter le projet.

Git : Si vous clonez ce projet à partir de GitHub.

Accès à un compte Outlook avec IMAP activé.

🚀 Étapes d'installation
Cloner le projet

Si vous n'avez pas encore cloné ce projet, utilisez la commande suivante pour le récupérer :

bash
Copier
Modifier
git clone https://github.com/yourusername/JAVAMAIL-API-TEST.git
cd JAVAMAIL-API-TEST
Configurer l'email et mot de passe

Modifiez le fichier OutlookMailChecker.java pour y insérer vos informations de connexion à Outlook.

Votre email : Remplacez your_email@outlook.com par votre adresse email.

Mot de passe d'application : Si vous avez activé l'authentification à deux facteurs, utilisez un mot de passe d'application au lieu de votre mot de passe principal.

Vérification des dépendances (pom.xml)

Le projet utilise Maven pour gérer les dépendances. Si vous avez Maven installé, il téléchargera automatiquement les bibliothèques nécessaires. Assurez-vous que le fichier pom.xml contient la dépendance suivante :

xml
Copier
Modifier
<dependencies>
    <dependency>
        <groupId>com.sun.mail</groupId>
        <artifactId>jakarta.mail</artifactId>
        <version>2.0.1</version>
    </dependency>
</dependencies>
🛠️ Exécution du projet
Compiler et exécuter le projet avec Maven

Pour compiler et exécuter le projet, utilisez les commandes suivantes :

Compiler le projet :

bash
Copier
Modifier
mvn compile
Exécuter le projet :

bash
Copier
Modifier
mvn exec:java -Dexec.mainClass="com.example.mailreader.OutlookMailChecker"
Ce programme se connecte à votre boîte de réception Outlook, vérifie si vous avez reçu un email de customer@mobilosoft.com et affiche le texte du message.

🔍 Vérification des emails
Le programme va :

Se connecter à votre compte Outlook via IMAP.

Vérifier les emails reçus dans votre boîte de réception.

Chercher un email de l'expéditeur customer@mobilosoft.com.

Afficher le contenu du message dans la console.

⚙️ Configuration IMAP dans Outlook
Si vous ne pouvez pas vous connecter, assurez-vous que l'IMAP est activé dans votre compte Outlook. Voici les paramètres recommandés :


Paramètre	Valeur
Serveur IMAP	outlook.office365.com
Port	993
Sécurité	SSL/TLS
Nom d'utilisateur	Votre adresse email Outlook
Mot de passe	Votre mot de passe d'application
Si vous utilisez l'authentification à deux facteurs (2FA), vous devez créer un mot de passe d'application.

📚 Sources
JavaMail API Documentation

Maven Documentation

GitHub Repository for JavaMail API

📌 Problèmes courants
Erreur d'authentification : Assurez-vous d'utiliser le mot de passe d'application si vous avez activé 2FA.

Connexion refusée : Vérifiez que l'IMAP est activé et que les paramètres de serveur sont corrects.

Problèmes avec Maven : Si vous rencontrez des problèmes avec les dépendances, essayez de nettoyer le projet avec mvn clean puis recompilez avec mvn compile.

📢 Avertissement
Ce projet est uniquement destiné à des fins de test. Ne partagez pas vos informations de connexion en ligne.

Si vous avez des problèmes ou des questions, n'hésitez pas à ouvrir une issue dans le dépôt.

