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


