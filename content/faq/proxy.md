---
title: "Utilisation du proxy"
date: 2020-06-21T19:17:35+01:00
tags: ["faq"]
contributor: "Jad Ezahraoui"
draft: false
---

## Proxy pour Maven

Les paramètres de proxy pour Maven se trouvent dans $HOME/.m2/settings.xml. Il existe une configuration de proxy commentée dans votre fichier settings.xml et des instructions pour le modifier.

Vos paramètres devraient ressembler à ceci:

```
<proxies>
    <proxy>
      <protocol>http</protocol>
      <host>10.23.201.11</host>
      <port>3128</port>
      <nonProxyHosts>*.google.com|ibiblio.org</nonProxyHosts>
    </proxy>
</proxies>

```

## Proxy pour Git

* Lorsque j'ai le PROXY_HOST (dans notre cas 10.23.201.11) et le PROXY_PORT (3128), je peux définir certaines variables d'environnement et dire à git d'utiliser le proxy (commande suivante):

```
  * Cas général : git config --global http.proxy "http://$PROXY_HOST:$PROXY_PRT"

  * Dans notre cas : git config --global http.proxy http://10.23.201.11:3128
```

* Pour annuler la configuration du proxy :

```
  * git config --global --unset http.proxy

  * git config --global --unset https.proxy
```

## Proxy pour NPM

* Utiliser les commandes suivantes:

```
npm config set proxy http://username:password@host:port
npm config set https-proxy http://username:password@host:port
```

* Vous pouvez faire une configuration manuelle sur le fichier ~/.npmrc :

```
proxy=http://username:password@host:port
https-proxy=http://username:password@host:port
https_proxy=http://username:password@host:port
```

## Proxy pour Yarn 

* Utiliser les commandes suivantes:

```
yarn config set proxy http://username:password@host:port
yarn config set https-proxy http://username:password@host:port
```

## Proxy pour Gradle

* Vous allez au fichier gradle.properties sen suivant les chemins :

```
- # windows gradle file
%userprofile%\.gradle\gradle.properties

- # linux gradle file
~/.gradle/gradle.properties
```
* Faire les modifications suivantes : 

```
## Proxy setup
systemProp.proxySet="true"
systemProp.http.keepAlive="true"
systemProp.http.proxyHost=host
systemProp.http.proxyPort=port
systemProp.http.proxyUser=username
systemProp.http.proxyPassword=password
systemProp.http.nonProxyHosts=local.net|some.host.com

systemProp.https.keepAlive="true"
systemProp.https.proxyHost=host
systemProp.https.proxyPort=port
systemProp.https.proxyUser=username
systemProp.https.proxyPassword=password
systemProp.https.nonProxyHosts=local.net|some.host.com
## end of proxy setup
```