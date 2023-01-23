---
title: "Primeiros Passos"
chapter: false
weight: 10
locale: "pt-BR"
---

## Requisitos

- [Visual Studio Code](https://code.visualstudio.com/)
- Git
- Genesys Cloud organization

## Criar um Cliente OAuth

O web-site usará o Genesys Cloud OAuth para autenticar os usuários, então primeiro você precisa criar um novo identificador OAuth de cliente de concessão implícita ( `implicit grant` ) em sua organização Genesys Cloud.

- Abra o Genesys Cloud, siga até `Administrador` e clique em `OAuth` (dentro de  `Integrações`)
- Clique em `Add Client`
- De um nome a seu App (por exemplo,  `Pedidos GDPR`). Descrição é opcional.
- Selecione `TConcessão implícita de token (Navegador)` (Token Implicit Grant (Browser))
- Digite `http://localhost:3000` como a  `URIs de redirecionamento` (Redirect URI)
- Na sessão `Escopo` (Scope), selecione `gdpr` e `gdpr:readonly`
- Clique `Salvar` e anote o valor do `Client ID`

## Faça download do código fonte

- Execute `git clone https://github.com/PierrickI3/genesyscloud-gdpr-requests` para obter o código mais recente
- Use vscode para abrir os arquivos:
  - `cd genesyscloud-gdpr-requests`
  - `code .`

Em seguida, siga para [Atualize o código e inicie o aplicativo](20_second.html) para rodar seu APP localmente.
