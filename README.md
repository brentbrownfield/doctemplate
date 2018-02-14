\# Document Title

* Content for this guide is in Asciidoc format and the entry file is `contents/index.adoc`.
* Place new images under `contents/images`.
* Add testable code snippets to `src` folder as appropriate for this guide.
* To build documentation run `./gradlew asciidoctor` and find the results in `build/asciidoc/html5`.
* To test code snippets run `./gradlew check`.

## Gradle Properties

Properties for gradle can be placed in gradle.properties in the .gradle folder in the user's home directory.

```
systemProp.http.proxyHost=<Proxy IP or Host Name>
systemProp.http.proxyPort=<Proxy Port>
systemProp.http.proxyUser=username
systemProp.http.proxyPassword=password
systemProp.http.nonProxyHosts=*.<localdomain>|localhost
systemProp.https.proxyHost=<Proxy IP or Host Name>
systemProp.https.proxyPort=<Proxy Port>
systemProp.https.proxyUser=username
systemProp.https.proxyPassword=password
systemProp.https.nonProxyHosts=*.<localdomain>|localhost
```

## Atom

If using [atom](http://atom.io) as your text editor you may need to set several atom configuration options.
Atom configuration options can be set from the command line using the following apm command:

    apm config set <key> <value>

|Key | Value|
| ---| -----|
|http-proxy | "http://username:password@<Proxy IP or Host Name\>:<Proxy Port\>"
|https-proxy | "http://username:password@<Proxy IP or Host Name\>:<Proxy Port\>"
|strict-ssl | false

## ERD

If you need to generate entity relationship diagrams with ERD install it as follows:

1. Download and install haskell
1. Download and install graphviz
1. git clone git://github.com/BurntSushi/erd
1. cabal install parsec
1. cabal install graphviz
1. cd erd
1. cabal configure
1. cabal build
1. Copy dist/build/erd/erd.exe to path
