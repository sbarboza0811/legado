# Legado — Primeiros 7 dias

PWA brasileiro para organizar as providências **imediatas** após o falecimento de um familiar: Declaração de Óbito, liberação, funerária, registro civil, velório, despedida, pertences e apoio à família. Não abrange inventário, investimentos, herança, INSS ou assuntos trabalhistas.

## Características

- Instalável em Android e outros dispositivos compatíveis com PWAs, sem loja de apps.
- Funciona offline depois da primeira abertura online e instalação do cache.
- **Sem backend, cadastro, API, banco de dados ou rastreamento**. Todos os registros ficam no `localStorage` do navegador/aplicativo.
- Roteiro sensível às circunstâncias do falecimento e à escolha entre sepultamento e cremação.
- Tarefas, responsáveis, notas, filtros, tarefas personalizadas, progresso e comunicados para a família.
- Exportação e importação de backup JSON; compartilhamento de resumo somente por ação explícita.
- Código estático: `index.html`, `style.css`, `app.js`, `manifest.webmanifest`, `sw.js` e ícones PNG.

## Publicação pelo GitHub Pages

1. Crie um repositório público chamado `legado` na conta GitHub desejada.
2. Envie **o conteúdo desta pasta** para a raiz da branch `main` (não envie a pasta como subdiretório).
3. No GitHub, vá em **Settings > Pages > Build and deployment** e escolha **Deploy from a branch** / `main` / `/(root)`. Salve.
4. Acesse `https://SEU-USUARIO.github.io/legado/` depois da publicação.
5. No Android, abra no Chrome ou Samsung Internet e use o menu **Instalar aplicativo** ou **Adicionar à tela inicial**, conforme o navegador.

> GitHub Pages serve apenas os arquivos públicos do app. Os dados e nomes inseridos pelo usuário **não são enviados ao GitHub**. Entretanto, apagar os dados do navegador pode apagar o acompanhamento. Use o backup JSON periodicamente. Não há sincronização automática entre celulares.

## Desenvolvimento local

```bash
python -m http.server 8000
```

Acesse `http://localhost:8000`. Instalação e service worker exigem HTTPS ou localhost; abrir o HTML diretamente por `file://` não habilita PWA.

## Fontes consultadas

- Ministério da Saúde: https://www.gov.br/saude/pt-br/centrais-de-conteudo/publicacoes/svsa/vigilancia/declaracao-de-obito-manual-de-instrucoes-para-preenchimento.pdf/view
- Lei de Registros Públicos: https://www.planalto.gov.br/ccivil_03/leis/l6015compilada.htm
- Kerinor (guia informativo, não oficial): https://www.kerinor.org/help/br/what-to-do-after-a-death
- MDN, PWA instalável: https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Guides/Making_PWAs_installable

Conteúdo informativo, não substitui instruções do hospital, funerária, cartório ou autoridades locais. Fluxos podem variar segundo o município e as circunstâncias.
