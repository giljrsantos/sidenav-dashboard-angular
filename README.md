# SideNav Dashboard

Este projeto é um SideNav e um Dashboard. Os componentes foram criados através de linha de comando.  Para criar esses dois components, tem que esta com a biblioteca de interface `@angular/material`.

## Versões
```json
Angular CLI: 16.2.11
Node: 18.16.0
Package Manager: npm 9.5.1
```

## Criando projeto e instalando biblíoteca `@angular/material`
    1 - ng new <nomeProjeto>
    2 - ng add @angular/material

## Criando components
    1 - ng g @angular/material:nav side-nav
    2 - ng g @angular/material:dashboard dashboard


No arquivo `app.component.html` onde aparece o conteúdo da projeto, apague todo o conteúdo da página, e em seguida importa o sidenav que foi criado `<app-side-nav></app-side-nav>`

Para importar o componente `dashboard` dentro do componente `side-nav` temos que criar uma diretiva do Agular de no `ng-content`, ela permite passagem de conteúdo entre componentes.
```html
  <mat-sidenav-content>
    <mat-toolbar color="primary">
      <button type="button">
        <mat-icon aria-label="Side nav toggle icon">menu</mat-icon>
      </button>
      <span>Side Nav</span>
    </mat-toolbar>
    <ng-content></ng-content><!--ng-content-->
  </mat-sidenav-content>
```

Após colocar a diretiva `ng-content`, basta importar o componente `dashboard` dentro `side-nav` que esta no arquivo `app.component.html` como se fosse um conteúdo.
```html
<app-side-nav>
  <app-dashboard />
</app-side-nav>
```
Sendo assim, tudo que for feito no componente `dashboard` vai refletir na página.

### screen
<img src="src\assets\img\1.png" width="100%">

<h1 align="center">💻 Desenvolvido Por: Gilberto Júnior</h1>