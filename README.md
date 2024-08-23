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

## Gerando componentes dentro de uma pasta especifica, para melhorar a organização e otimizar as rotas de navegação com base em um objetivo claro
```sh
ng generate component site/home --inline-template=false --inline-style=false --style=scss
ng generate service site/home/home
ng generate module site/home --module app --flat=false

ng generate component site/about --inline-template=false --inline-style=false --style=scss
ng generate service site/about/about
ng generate module site/about --module app --flat=false

ng generate component site/services --inline-template=false --inline-style=false --style=scss
ng generate service site/services/services
ng generate module site/services --module app --flat=false

ng generate component site/contact --inline-template=false --inline-style=false --style=scss
ng generate service site/contact/contact
ng generate module site/contact --module app --flat=false

ng generate component site/partners --inline-template=false --inline-style=false --style=scss
ng generate service site/partners/partners
ng generate module site/partners --module app --flat=false
```
## Roteamento dos componentes

```typescript
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { HomeComponent } from './site/home/home.component';

const routes: Routes = [
  { path: 'home', component: HomeComponent }, // Rota para o ContactComponent
  { path: '', redirectTo: '/home', pathMatch: 'full' },  // Redireciona a rota base para 'home'
  { path: '**', redirectTo: '/home', pathMatch: 'full' }  // Redireciona qualquer rota não correspondida para 'home'


];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```


## Gerando um layout padronizado para todas as páginas
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
ng add @angular/material
```

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

## Step 3: Gestures by HammerJS (Gestos)

```sh
npm install --save hammerjs
```

# PrimeNG

## Step 1:
```sh
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
@import "primeicons/primeicons.css";
```


# Rodar o projeto

## Rodar o projeto para o público geral
```sh
ng serve --host 0.0.0.0 --port 4200 --disable-host-check
```

## Rodar o projeto para a rede local
```sh
ng serve --host 192.168.15.110 --port 4200 --disable-host-check
```
