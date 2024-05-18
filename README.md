# Angular

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
ng analytics disable
```

Gerando componentes dentro de uma pasta especifica, para melhorar a organização e otimizar as rotas de navegação com base em um objetivo claro
```sh
ng generate component site/home --inline-template=false --inline-style=false --style=scss
ng generate component site/about --inline-template=false --inline-style=false --style=scss
ng generate component site/services --inline-template=false --inline-style=false --style=scss
ng generate component site/contact --inline-template=false --inline-style=false --style=scss
```
Gerando um layout padronizado para todas as páginas
```sh
ng generate component site/layout --inline-template=false --inline-style=false --style=scss
```
```sh
ng generate component signup --inline-template=false --inline-style=false --style=scss
ng generate component signin --inline-template=false --inline-style=false --style=scss
ng generate component home --inline-template=false --inline-style=false --style=scss
ng generate component account --inline-template=false --inline-style=false --style=scss
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
```

## Step 3: Gestures (Gestos) - by HammerJS

```sh
npm install --save hammerjs
```

## PrimeNG

## Step 1:
```sh
npm install primeng
npm install primeng primeicons primeflex --save
```

## Step 2:
Na pasta principal do projeto, dentro do arquivo 'angular.json' (linha 56)
```sh
"styles": [
  "src/styles.scss",
  "node_modules/primeng/resources/themes/lara-light-blue/theme.css",
  "node_modules/primeng/resources/primeng.min.css"
],
```

## Step 3:
Na pasta 'src', no arquivo 'styles.scss'
```sh
@import "primeng/resources/themes/lara-light-blue/theme.css";
@import "primeng/resources/primeng.css";
```
