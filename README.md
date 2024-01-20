# angular

## Setup
```sh
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```
```sh
npm install -g @angular/cli
```

## Criando novos projetos

```sh
ng new project-name --minimal=true --routing=true --style=scss --ssr=true
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
