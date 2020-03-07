# Angular aktualisieren
Bevor Du Angular aktualisierst sichere Dir die Dateien ```package.json``` und ```package-lock.json```. ( z.B. commit in git ) 

Nun musst Du überprüfen, welche Version installiert ist.

```elixir
$ ng version

     _                      _                 ____ _     ___
    / \   _ __   __ _ _   _| | __ _ _ __     / ___| |   |_ _|
   / △ \ | '_ \ / _` | | | | |/ _` | '__|   | |   | |    | |
  / ___ \| | | | (_| | |_| | | (_| | |      | |___| |___ | |
 /_/   \_\_| |_|\__, |\__,_|_|\__,_|_|       \____|_____|___|
                |___/
    

Angular CLI: 8.1.1
Node: 10.16.3
OS: linux x64
Angular: 8.1.1
... animations, cli, common, compiler, compiler-cli, core, forms
... language-service, platform-browser, platform-browser-dynamic
... router

Package                           Version
-----------------------------------------------------------
@angular-devkit/architect         0.801.1
@angular-devkit/build-angular     0.801.1
@angular-devkit/build-optimizer   0.801.1
@angular-devkit/build-webpack     0.801.1
@angular-devkit/core              8.1.1
@angular-devkit/schematics        8.1.1
@angular/cdk                      8.0.2
@angular/http                     7.2.15
@angular/material                 8.0.2
@ngtools/webpack                  8.1.1
@schematics/angular               8.1.1
@schematics/update                0.801.1
rxjs                              6.5.2
typescript                        3.4.5
webpack                           4.35.2

```

Danach stellst Du mit ```ng update``` fest, was alles installiert werden muss.

```elixir
$ ng update

Using package manager: 'npm'
Collecting installed dependencies...
Found 37 dependencies.
    We analyzed your package.json, there are some packages to update:
    
      Name                               Version                  Command to update
     --------------------------------------------------------------------------------
      @angular/cdk                       8.0.2 -> 8.2.2           ng update @angular/cdk
      @angular/cli                       8.1.1 -> 8.3.7           ng update @angular/cli
      @angular/core                      8.1.1 -> 8.2.9           ng update @angular/core
      @angular/material                  8.0.2 -> 8.2.2           ng update @angular/material
      rxjs                               6.5.2 -> 6.5.3           ng update rxjs

``` 

Informiere Dich bei https://update.angular.io, ob vorher noch weitere Schritte ausgeführt werden müssen, ehe Du mit der Aktualisierung fortfährst.

Jetzt mit ```ng update @angular/cli @angular/core @angular/cdk @angular/material rxjs``` aktualisieren. Wenn Du Dir unsicher bist, füge noch Schalter ```-d``` für ```dry-run``` hinzu.

Treten __vulnerabilities__ auf, führe ```npm audit fix``` aus.

Sollte folgende Ausgabe 

```
npm WARN @angular-devkit/build-angular@0.803.7 requires a peer of typescript@>=3.1 < 3.6 but none is installed. You must install peer dependencies yourself.
```

erscheinen, ist typescript mit dem Befehl ```npm i typescript@3.5.3 --save-dev --save-exact``` zu installieren. 

Welche Version, Du installieren musst, findest Du unter https://www.npmjs.com/.

Anschließend mit ```ng version``` die neue Version anzeigen lassen.

```elixir
$ ng version


     _                      _                 ____ _     ___
    / \   _ __   __ _ _   _| | __ _ _ __     / ___| |   |_ _|
   / △ \ | '_ \ / _` | | | | |/ _` | '__|   | |   | |    | |
  / ___ \| | | | (_| | |_| | | (_| | |      | |___| |___ | |
 /_/   \_\_| |_|\__, |\__,_|_|\__,_|_|       \____|_____|___|
                |___/
    

Angular CLI: 8.3.7
Node: 10.16.3
OS: linux x64
Angular: 8.2.9
... animations, common, compiler, compiler-cli, core, forms
... language-service, platform-browser, platform-browser-dynamic
... router

Package                           Version
-----------------------------------------------------------
@angular-devkit/architect         0.803.7
@angular-devkit/build-angular     0.803.7
@angular-devkit/build-optimizer   0.803.7
@angular-devkit/build-webpack     0.803.7
@angular-devkit/core              8.3.7
@angular-devkit/schematics        8.3.7
@angular/cdk                      8.2.2
@angular/cli                      8.3.7
@angular/material                 8.2.2
@ngtools/webpack                  8.3.7
@schematics/angular               8.3.7
@schematics/update                0.803.7
rxjs                              6.5.3
typescript                        3.5.3
webpack                           4.39.2
```

Zur Überprüfung gibst Du ```ng update``` ein. Ist alles glatt gelaufen, wird Dir folgende Ausgabe anzeigt.

```
$ ng update

Using package manager: 'npm'
Collecting installed dependencies...
Found 36 dependencies.
    We analyzed your package.json and everything seems to be in order. Good work!

```


## Zurückdrehen
Sollte auf dem oben beschriebenen Weg, irgendetwas schief gehen, dann kannst Du alles wieder zurückdrehen.

Stelle den alten Zustand der Dateien ```package.json``` und ```package-lock.json``` wieder her, lösche den Ordner ```node_modules``` und führe ```npm install``` aus.










