---
title: "Incorporando o aplicativo"
chapter: false
weight: 30
locale: "pt-BR"
---

## Publicando seu App

O aplicativo agora está pronto para ser usado no Genesys Cloud. Existem várias maneiras de usá-lo:

### Usando localhost

Isso é o que você tem feito até agora. Você pode manter o aplicativo em execução localmente e usá-lo em sua organização Genesys Cloud, porém **vai funcionar apenas dentro de seu computador**.

### Usando seu domínio

Você pode copiar o código-fonte em seu(s) próprio(s) servidor(es) da web. Verifique se o aplicativo pode ser acessado por meio de um URL acessível publicamente (por exemplo, `https://mydomain.com/gdpr-requests`).

### Páginas Github (Github pages)

Você pode hospedar este site estático usando o Github Pages se tiver uma conta do Github. Isso é prático porque lhe dará uma URL `https`. As credenciais em `static/js/genesyscloud.js` não são críticas, pois exigem que qualquer pessoa que as use também insira seu nome de usuário e senha para autenticar.

Uma página de amostra está disponível [aqui](https://github.com/purecloudgdprrequests/purecloudgdprrequests.github.io). Neste caso, a `Authorized redirect URI` é `https://purecloudgdprrequests.github.io/index.html`

## Incorpore o aplicativo em sua organização

Para incorporar seu site diretamente no PureCloud, você precisa criar uma nova `Integração`

- Siga para `Adminstração/Integrações` e clique em `+Integrações` no canto superior direito para adicionar um novo aplicativo cliente
- Na aba `Detalhes`
  - Insira um nome para o novo aplicativo cliente
- Na aba `Configuration`, entre o seguinte:
  - Application URL: O caminho completo para a página inicial do seu site (e.g. [https://purecloudgdprrequests.github.io](https://purecloudgdprrequests.github.io))
  - Application Type: widget
  - Application Category: (deixe em branco)
  - Iframe Sandbox Options: allow-scripts,allow-same-origin,allow-forms,allow-modals (valor default)
  - Group Filtering: Selecione um grupo de usuários que podem acessar este aplicativo cliente. Você pode ter que criar um novo grupo primeiro em `Adminstração/Grupos`
  - Clique em `Salvar`
- Volte para a aba `Detalhes` e clique em `Active` para ativar sua aplicação

Pode ser necessário sair e entrar novamente para visualizar o aplicativo dentro da sessão `Aplicativos` (Apps) no lado esquerdo.

![Embedded app](../images/app_icons.jpg)

Pule para sessão de [Conclusão](../090-Conclution/_index.html) para ler sobre o que conseguiu.
