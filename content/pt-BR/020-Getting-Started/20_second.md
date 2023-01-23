---
title: "Atualize o código e inicie o aplicativo"
chapter: false
weight: 20
locale: "pt-BR"
---

## Atualize a configuração do App

- Abra o arquivo `/static/js/genesyscloud.js`
- Ajuste as constantes `clientId`, `redirectUrl` e `environment` para os valores que você obteve do Genesys Cloud antes, por exemplo:

```js
const clientId = "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx";
const redirectUrl = "http://localhost";
const environment = "mypurecloud.ie"; // YouSeu ambiente Genesys Cloud (por exemplo, mypurecloud.com, mypurecloud.de)
```

Encontre seu ambiente [aqui](https://developer.genesys.cloud/platform/api/)

## Execute o App

- Instale a extensão [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) no Visual Studio Code
- Tenha certeza que o arquivo `index.html` esteja aberto no editor
- Clique em`Go Live` para iniciar o web server local.

Você deve ser capaz de ver a seguinte página:

![First launch](../images/app_first_launch.jpg)

## Como usar seu App

### Iniciando uma nova solicitação

- Clique no botão `New Request`
- Selecione o tipo de pedido
  - `Delete` anonimizará o [PII](https://en.wikipedia.org/wiki/Personal_data) do usuário
  - `Export` exportará as atividades de um usuário dentro do Genesys Cloud. O arquivo exportado é um conjunto de arquivos CSV e JSON.
  - `Update` atualizará os detalhes de um usuário em toda a Genesys Cloud.
- Digite um nome, um endereço, um número de telefone ou um endereço de e-mail. Apenas um desses campos é obrigatório, mas você pode inserir quantos quiser para encontrar a pessoa certa.
- Clique em `Search`
- Clique em `Select and Submit` depois de ter identificado a pessoa correta

![Search Subject](../images/app_search_subject.jpg)

- Se a solicitação for bem-sucedida, você deverá ver o seguinte:

![Searching](../images/app_searching.jpg)

- Os pedidos normalmente demoram entre 24h e 48h a serem processados. Você pode verificar o status da sua solicitação atualizando a página.

Em seguida, vá para [Incorporando o aplicativo](30_third.html) para inserior este App em sua organização Genesys Cloud.
