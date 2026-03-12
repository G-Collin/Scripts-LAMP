# Script-LAMP
Conception d'un script permettant d'installer et configurer rapidement un serveur LAMP.

### Pré-requis
Avoir une machine sous Debian 13.2.0.

==============================================================

## Contenu de install-wordpress
Ce script Bash permet d’installer et de configurer automatiquement un serveur LAMP complet sur une machine Debian, comprenant :
- Linux, Apache, MariaDB, PHP,
- DNS local via Bind9 pour le nom de domaine NOM_DE_VOTRE_MACHINE.lan,
- Système de messagerie avec Exim4 (SMTP) et Roundcube (webmail),
- WordPress installé et connecté à une base de données MariaDB,
- phpMyAdmin pour la gestion des bases de données,
- Un certificat SSL auto-signé pour les accès HTTPS.

### Le script est conçu pour être exécuté en tant que root sur un système Debian 13, et configure :
- le DNS, les hôtes locaux et la résolution de nom,
- les modules Apache nécessaires (rewrite, ssl),
- les hôtes virtuels HTTP/HTTPS,
- MariaDB avec une base et un utilisateur WordPress dédiés,
- les droits de fichiers (/var/www/wordpress),
- Exim4 et Roundcube pour la messagerie locale.

### À la fin de l’exécution, vous pouvez accéder aux services via :
- phpmyadmin : https://NOM_DE_VOTRE_MACHINE.lan
- Wordpress : https://NOM_DE_VOTRE_MACHINE.lan/phpmyadmin
- Roundcube : https://NOM_DE_VOTRE_MACHINE.lan/roundcube
