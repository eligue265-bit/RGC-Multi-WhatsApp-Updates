# RGC Multi WhatsApp — Atualizações

Repositório público destinado **somente à distribuição de versões do aplicativo Windows**.

> **Estado atual:** em preparação. O RGC Multi WhatsApp v9.1 ainda **não possui atualização automática habilitada** e nenhuma atualização está disponível por este repositório até a publicação de uma versão oficial.

## Como funcionará

1. Uma nova versão será compilada em um instalador Windows **NSIS** usando Electron Builder.
2. O instalador, o arquivo `latest.yml` e os arquivos `.blockmap` necessários serão publicados como **assets de uma GitHub Release**.
3. Uma futura versão do aplicativo, contendo `electron-updater` e configurada para este repositório, verificará a atualização e oferecerá a instalação.
4. As sessões do WhatsApp e os dados locais deverão continuar fora da pasta de instalação. Faça backup antes da primeira migração.

## Publicação

- Repositório: `eligue265-bit/RGC-Multi-WhatsApp-Updates`
- O código-fonte, `node_modules`, arquivos `%APPDATA%`, cookies, senhas, licenças e dados de clientes **não devem ser enviados para este repositório público**.
- Para uma nova versão, crie uma **Release** em `https://github.com/eligue265-bit/RGC-Multi-WhatsApp-Updates/releases/new` e anexe os arquivos de distribuição da compilação, após testes.
- **Não publique arquivos individuais de instalação pelo botão “Add file” na aba Code**: arquivos grandes pertencem às Releases.
- Antes de distribuição comercial, considere assinar digitalmente o instalador, avaliar as dependências e testar em máquinas limpas.

## Atenção

O repositório público distribui **atualizações**, não substitui o servidor Cloudflare responsável pelas licenças. Nenhum Worker ou banco D1 precisa ser alterado para a hospedagem dos arquivos de atualização.

Para disponibilizar atualizações dentro do app, ainda será necessária uma versão inicial nova, instalada uma vez com suporte a atualização automática.
