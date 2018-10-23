# JAVA_SPRING_BOOT
Preparation pour un environnement SPRING BOOT sous MACOS MOJAVE 10.14

## USEFULL TOOLS
```
 brew install tree wget
```

## INSTALLATION JAVA JDK 8
Machine virtuel et espace de dev
 * https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
```
  $ java --version
  $ export JAVA_HOME=$(/usr/libexec/java_home)
  $ echo $JAVA_HOME
```

## INSTALLATION HOMEBREW
Gestionnaire de paquets
```
 /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
 $ brew -v
```

## INSTALLATION TOMCAT
 source : https://wolfpaulus.com/mac/tomcat/
```
 $ cd /Download
 $ wget http://apache.mirror.colo-serv.net/tomcat/tomcat-9/v9.0.12/bin/apache-tomcat-9.0.12.zip
 $ unzip apache-tomcat-9.0.12.zip
 $ sudo mv apache-tomcat-9.0.12 /usr/local/
 $ sudo ln -s /usr/local/apache-tomcat-9.0.12 /Library/Tomcat-9
 $ sudo chown -R nicolas /Library/Tomcat-9
```
 * testons sur http://localhost:8080
``` 
 $ /Library/Tomcat-9/bin/startup.sh
```
 * vous devez obtenir : Apache Tomcat/9.0.12
``` 
 $ /Library/Tomcat-9/bin/shutdown.sh
```

## INSTALLATION ECLIPSE
```
 $ brew search eclipse
 ... homebrew/cask/eclipse-java...
 $ brew cask install eclipse-java
```
 * workspace : /home/nicolas/Documents/eclipse-workspace
 * Puis vérification au démarrage de bien être sur la version "Eclipse IDE for Java Developers"
 * fermer l'ongler "Welcome" pour aller sur l'environnement de dev

## CONNEXION ECLIPSE TOMCAT

### INSTALLER LE MODULE SERVER
 * Help -> Install New Software
 * Choisir "Photon - http://download.eclipse.org/releases/photon" site
 * rechercher "JST"
 * selectionner JST Server Adapters Extentions
 * redémarrer eclipse

 Afficher l'onglet server
 * Window -> Show View -> Other et rechercher "server"

### AJOUTER TOMCAT DANS ECLIPSE
 * dans l'onglet SERVER, cliquer sur "No server available..."
 * cliquer sur Apache et choisir TOMCAT 9
 * choisir le dossier /usr/local/apache-tomcat-9.0.12 pour tomcat
