# Flow TV

Interface experimental e independente para televisores LG com webOS, com visual limpo e sem banners publicitários dentro do aplicativo.

## Versão web

- Início cinematográfico, aplicativos, filmes, séries, jogos e entradas.
- Busca demonstrativa, personalização de tema e cor, perfis e navegação por teclado e controle.
- Interface estática sem backend nem dados pessoais, preparada para GitHub Pages.
- Filmes e séries exibidos são exemplos; não há sincronização com Netflix, Prime Video ou outros streamings.
- Atalhos para HDMI e aplicativos externos são demonstrativos nesta publicação, ainda não controlam a TV diretamente.

**Site previsto:** https://aton-citizen.github.io/flow-tv/ (disponível depois que o GitHub Pages for ativado e o deploy concluir).

## Ativar o GitHub Pages

Acesse **Settings → Pages → Build and deployment → Source → GitHub Actions**. O fluxo em `.github/workflows/pages.yml` tentará publicar automaticamente ao atualizar a branch `main`. Se necessário, execute a ação manualmente pela guia Actions.

## Aplicativo LG (etapa seguinte)

A pasta `webos-bridge/` contém um lançador experimental que direciona para o site online. Quando o site estiver publicado, a pasta pode ser empacotada no Windows com a CLI oficial:

```powershell
ares-package.cmd .\webos-bridge
```

O pacote gerado mantém o identificador `com.flowtv.launcher` e pode ser instalado como atualização da versão atual após testes. O aplicativo inicial instalado na LG **não** se atualiza automaticamente antes dessa etapa.

A abertura da interface por redirecionamento ainda não foi testada no modelo LG específico. Não habilitamos root nem modificamos o botão Home do webOS.

## Desenvolvimento

Esta é uma versão web autocontida em `index.html`. Para atualizar, publique mudanças nessa página: o site será republicado pelo GitHub Actions. É possível que a TV precise reabrir o aplicativo ou atualizar o cache para ver as alterações.

**Flow TV não é um produto oficial da LG.**
