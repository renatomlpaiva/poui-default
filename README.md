# Template POUI (estrutura minima para iniciar um projeto)

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 18.2.12.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.

## Start project Angular by layout PO-UI (Totvs)

Start comand

ng new [project name] --no-standalone --routing --ssr=false

Renato Paiva


# PO Theme - Totvs Default Theme

Tema padrão da Totvs para aplicações desenvolvidas com [PO UI](http://po-ui.io).

:warning: __Uso exclusivo dos produtos TOTVS e Clientes.__

### Como iniciar o tema

Para utilizar o **PO UI**, seguir passos do link.

https://po-ui.io/guides/getting-started

### Pré-requisitos

Para começar a utilizar o **PO UI** é pré-requisito ter o `Node.js` instalado (versão 18.19.x ou acima) e o seu gerenciador de pacote favorito na versão mais atual. Caso você ainda não tenha instalado o pacote `@angular/cli`, instale-o via `npm` ou `yarn`.

Instalando com npm:

```
npm i -g @angular/cli@18
```

Caso prefira instalar com o yarn:

```
yarn global add @angular/cli@18
```

### Passo 1 - Crie o seu primeiro projeto

  >  Caso você já tenha um projeto criado e deseje apenas incluir o Po, pule esta etapa e vá para o Passo 1.1.

O `Angular CLI` se encarrega de construir toda estrutura inicial do projeto. Para isso, execute o seguinte comando:

```
ng new my-po-project --skip-install
```

  >  O parâmetro `--skip-install` permite criar o projeto, contudo, não instalará as dependências automaticamente.

### Passo 1.1 - Instalando as dependências

Antes de executar a instalação ou inserir o **Po** no seu projeto existente, é necessário verificar as dependências do seu projeto, algumas delas precisam estar de acordo com a versão do Po e Angular (elas podem ser encontradas no arquivo `package.json` localizado na raiz da aplicação).

Veja abaixo a lista de dependências e as versões compatíveis, elas devem ser conferidas e se necessário, ajustadas no seu projeto.

```json
  "dependencies": {
    "@angular/animations": "~18.0.1",
    "@angular/common": "~18.0.1",
    "@angular/compiler": "~18.0.1",
    "@angular/core": "~18.0.1",
    "@angular/forms": "~18.0.1",
    "@angular/platform-browser": "~18.0.1",
    "@angular/platform-browser-dynamic": "~18.0.1",
    "@angular/router": "~18.0.1",
    "rxjs": "~7.8.1",
    "tslib": "^2.6.2",
    "zone.js": "~0.14.4"
    ...
  },
  "devDependencies": {
    "@angular-devkit/build-angular": "~18.0.2",
    "@angular-devkit/schematics": "~18.0.2",
    "@angular/cli": "~18.0.2",
    "@angular/compiler-cli": "~18.0.1",
    ...
    "typescript": "~5.4.5"
  }
```

Após verificar se estas dependências do seu projeto estão com as versões compatíveis declaradas acima, acesse a pasta raiz do seu projeto e execute o comando abaixo:

Instalando com npm:

```
npm install
```

Caso prefira instalar com o yarn:

```
yarn install
```

### Passo 2 - Adiconando o pacote @po-ui/ng-components

Utilizando o comando `ng add` do `Angular CLI`, vamos adicionar o Po em seu projeto e o mesmo se encarregará de configurar o tema, instalar o pacote e importar o módulo do **Po**. Além de importar também o modulo **HttpClientModule**.

Execute o comando abaixo na pasta raiz do seu projeto:

```
ng add @po-ui/ng-components
```

  >  Ao executar o comando acima, será perguntado se deseja incluir uma estrutura inicial em seu projeto com menu lateral, página e toolbar, utilizando componentes do Po, caso desejar, apenas informe: Y.

### Passo 3 - Rode o seu projeto

Agora basta executar mais um comando para subir a aplicação e ver o seu projeto rodando no browser ;).

```
ng serve
```

Abra o browser e acesse a url `http://localhost:4200`. Pronto! Se você escolheu incluir uma estrutura inicial em seu projeto, ele deve estar parecido com essa imagem:

### Como usar o tema **PO UI** fornecido pela TOTVS

O **PO UI** possui o seu próprio tema, mas disponibilizamos um tema com os padrões da TOTVS.

Para utilizá-lo, instale o pacote `@totvs/po-theme` conforme abaixo:

```
npm i @totvs/po-theme
```

Em seguida, atualize o arquivo `angular.json` para utilizar o tema.

```json
"styles": [
  "node_modules/@totvs/po-theme/css/po-theme-default-variables.min.css",
  "node_modules/@totvs/po-theme/css/po-theme-default.min.css",
  "node_modules/@po-ui/style/css/po-theme-core.min.css",
]
```

> Leia mais sobre [como criar seu próprio tema customizado do PO UI][create-theme-customization].

[create-theme-customization]: https://po-ui.io/guides/create-theme-customization


### Create component 

Utilizar linha de comando `Angular Cli`.

> No exemplo criamos a `Home` da aplicação.

```
 ng g c features/home
```

| O comando cria os arquivo:| Arquivos                       |
| --------------------------| ------------------------------ |
| CREATE | src/app/features/home/home.component.css          | 
| CREATE | src/app/features/home/home.component.html         | 
| CREATE | src/app/features/home/home.component.spec.ts      | 
| CREATE | src/app/features/home/home.component.ts           | 
| UPDATE | src/app/app.module.ts                             | 

