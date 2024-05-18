# angular

## Setup
```sh
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```
```sh
npm install -g @angular/cli
```

## Criando novos projetos

Este gera o projeto com o recurso de módulos
```sh
ng new project-name --standalone=false --minimal=true --routing=true --style=scss --ssr=true --directory .
```
Este não gera o projeto com o recurso de módulos
```sh
ng new project-name --standalone=true --minimal=true --routing=true --style=scss --ssr=true --directory .
```
```sh
ng new project-name --routing=true --style=scss --ssr=true --directory .
```
```sh
ng analytics disable
```

```sh
cd project-name
```

```sh
ng serve --open
```

## Angular Material (Mobile)

## Step 1:
```sh
npm install --save @angular/material @angular/cdk @angular/animations
```

## Step 2:
```typescript
import { NgModule } from '@angular/core';
import { BrowserModule, provideClientHydration } from '@angular/platform-browser';

import { AppRoutingModule } from './app-routing.module';
import { AppComponent } from './app.component';

import {BrowserAnimationsModule} from '@angular/platform-browser/animations';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    AppRoutingModule,
    BrowserAnimationsModule
  ],
  providers: [
    provideClientHydration()
  ],
  bootstrap: [AppComponent]
})
export class AppModule { }
```sh


## PrimeNG

```sh
npm install primeng
npm install primeng primeicons primeflex --save
```

Na pasta principal do projeto, dentro do arquivo 'angular.json' (linha 56)
```sh
"styles": [
  "src/styles.scss",
  "node_modules/primeng/resources/themes/lara-light-blue/theme.css",
  "node_modules/primeng/resources/primeng.min.css"
],
```
Na pasta 'src', no arquivo 'styles.scss'
```sh
@import "primeng/resources/themes/lara-light-blue/theme.css";
@import "primeng/resources/primeng.css";
```
