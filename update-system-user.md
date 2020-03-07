Lösche zunächst ```@angular/cli``` .
```
sudo npm uninstall -g @angular/cli (falls global installiert)

npm uninstall @angular/cli

npm cache verify

rm -rf ~/node_modules/

```

Danach die gewünschte Version installieren.

```
npm install @angular/cli@8.3.20
```

Zum Überprüfen muss Du jetzt ein Test-Projekt anlegen ```ng new test-angular```, dann in den Ordner ```test-angular``` wecheln und ```ng version``` aufrufen.

Die Ausgabe sollte nun so aussehen:
```elixir
     _                      _                 ____ _     ___
    / \   _ __   __ _ _   _| | __ _ _ __     / ___| |   |_ _|
   / △ \ | '_ \ / _` | | | | |/ _` | '__|   | |   | |    | |
  / ___ \| | | | (_| | |_| | | (_| | |      | |___| |___ | |
 /_/   \_\_| |_|\__, |\__,_|_|\__,_|_|       \____|_____|___|
                |___/
    

Angular CLI: 8.3.20
Node: 10.17.0
OS: linux x64
Angular: 8.2.14
... animations, common, compiler, compiler-cli, core, forms
... language-service, platform-browser, platform-browser-dynamic
... router

Package                           Version
-----------------------------------------------------------
@angular-devkit/architect         0.803.20
@angular-devkit/build-angular     0.803.20
@angular-devkit/build-optimizer   0.803.20
@angular-devkit/build-webpack     0.803.20
@angular-devkit/core              8.3.20
@angular-devkit/schematics        8.3.20
@angular/cli                      8.3.20
@ngtools/webpack                  8.3.20
@schematics/angular               8.3.20
@schematics/update                0.803.20
rxjs                              6.4.0
typescript                        3.5.3
webpack                           4.39.2
    
```
