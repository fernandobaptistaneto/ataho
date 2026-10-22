# Ataho

**Atalhos inteligentes para sistemas web.**

Extensão para Chrome que acelera o dia a dia no Tasy: troque de perfil, abra funções e volte exatamente para onde você estava, tudo pelo teclado.

![Demonstração do Ataho](assets/tasy-flow-demo.gif)

<p align="center">
  <img src="assets/tasy-flow.png" alt="Paleta Alt+P do Ataho" width="440" />
</p>

> **Versão 1.7.44** · Projeto independente. Não é um produto oficial da Bionexo ou do Tasy.

[![Downloads](https://img.shields.io/github/downloads/fernandobaptistaneto/ataho/total?label=downloads)](https://github.com/fernandobaptistaneto/ataho/releases)

## Download

| Versão | Para quem | Link |
| --- | --- | --- |
| **1.7.44 (mais recente)** | Quer as novidades abaixo | [Ataho.zip](https://github.com/fernandobaptistaneto/ataho/releases/latest/download/Ataho.zip) |
| **1.5.25 (estável)** | Prefere a versão mais testada | [Ataho.zip](https://github.com/fernandobaptistaneto/ataho/releases/download/v1.5.25/Ataho.zip) |

## Novidades da 1.7.44

- **Troca de estabelecimento (Alt + I) com a função em uso:** fecha as funções abertas e reabre a que você estava usando, se estiver liberada no novo estabelecimento.
- **PEP na troca de estabelecimento:** com o PEP aberto, se o destino tiver atendimentos recentes, você escolhe qual abrir depois da troca (ou troca sem atendimento).
- **Caminho na troca de estabelecimento:** se a função em uso tiver filtro/caminho salvo no destino, o Ataho pergunta se quer retomar esse caminho ou só reabrir a função limpa.
- **Atendimentos do PEP por estabelecimento:** no Alt + O a lista mostra só os atendimentos do estabelecimento atual. Se o atendimento não for encontrado, aparece um aviso.
- **Mapear tela (Alt + M):** modos **Mapear blocos** e **Selecionar área** (clique e arraste). Botão claro para ver todos os valores.
- **Mini tutorial** na primeira vez (também em **Ver tutorial**, no ícone da extensão).
- **Atalhos Alt + I e Alt + M** pedem permissão do site na primeira vez, igual ao Alt + P e Alt + O.
- Mantém o que já havia antes: abrir função com último filtro/caminho, troca de perfil com reabertura, busca nos menus e listas.

## Atalhos

| Atalho | O que faz |
| --- | --- |
| **Alt + P** | Trocar perfil |
| **Alt + O** | Abrir função (com último filtro e caminho) |
| **Alt + I** | Trocar estabelecimento |
| **Alt + M** | Mapear os campos da tela |
| **Alt + 1**, **Alt + 2**... | Escolher a opção numerada nas perguntas da paleta |

Na paleta: **↑ ↓** navegam, **Enter** seleciona e **Esc** fecha.

> Se algum atalho não funcionar, ajuste em `chrome://extensions/shortcuts`.

## Instalação

1. Baixe o **Ataho.zip** (tabela acima) e extraia em uma pasta permanente.
2. Abra `chrome://extensions` em uma aba do Google Chrome.
3. Ative **Modo do desenvolvedor**.
4. Clique em **Carregar sem compactação** e selecione a pasta `ataho` (a que contém o `manifest.json`).
5. Abra o Tasy e pressione **Alt + P**. Na primeira vez, o Chrome pede para autorizar o endereço do Tasy.

![Guia de instalação do Ataho](assets/guia-instalacao.jpg)

### Atualizar para uma versão nova

1. Baixe o novo **Ataho.zip** e extraia por cima da pasta antiga (substituindo os arquivos).
2. Em `chrome://extensions`, clique no botão de recarregar do Ataho.
3. Atualize a página do Tasy (**F5**).

## Como usar

### Trocar perfil

1. Com o Tasy aberto, pressione **Alt + P**.
2. Digite parte do nome do perfil (acentos e maiúsculas não importam).
3. **Enter** para trocar. Se houver função aberta, escolha se quer reabri-la.
4. Se escolher reabrir, o Ataho volta para a mesma tela: filtro, registro aberto, menu e abas. Telas de cadastro com formulário aberto voltam para a grade, nunca para o formulário.

A função só é reaberta se estiver liberada no perfil de destino.

No **PEP**, o Ataho reabre o mesmo atendimento que estava aberto. Isso depende de o perfil de destino ter acesso ao setor do paciente; se não tiver, aparece um aviso e basta clicar na tela para fechá-lo.

### Abrir função

![Abrir função com o último caminho](assets/abrir-funcao-caminho.png)

1. Pressione **Alt + O** e digite parte do nome da função.
2. **Enter** abre a função.
3. Se aparecer uma linha com a etiqueta **filtro** ou **caminho** embaixo da função (como **Particular › Convênio** na imagem), selecione essa linha: o Ataho abre a função e reconstitui o último caminho, com filtro, registro, menu e abas em que você estava.

#### PEP com atendimento

![Abrir o PEP já com um atendimento](assets/pep-atendimento.jpg)

1. No **Alt + O**, escolha **Prontuário Eletrônico Paciente - PEP**.
2. O Ataho pergunta o atendimento: escolha um dos últimos da lista (do estabelecimento atual) ou digite o número do atendimento.
3. **Abrir** (**Alt + 1**) abre o PEP já no atendimento escolhido. **Agora não** (**Alt + 2**) abre o PEP sem escolher atendimento (ou só traz o PEP para frente, se já estiver aberto).
4. Com o PEP já aberto (etiqueta **EM FOCO**), selecione-o de novo e escolha outro atendimento para trocar de paciente direto.

O Ataho guarda só o **último** filtro e caminho de cada função, separado por estabelecimento. Filtros que já vêm preenchidos pelo Tasy (como "Situação: Ativos") não contam.

### Trocar estabelecimento

1. Pressione **Alt + I**.
2. Escolha a empresa (se houver mais de uma) e depois o estabelecimento.
3. As funções abertas serão fechadas. A função em uso é reaberta no novo estabelecimento, se estiver liberada.
4. Com o **PEP** aberto, se houver atendimentos salvos no destino, o Ataho pergunta qual abrir depois da troca.
5. Com outra função aberta, se houver filtro/caminho salvo no destino, o Ataho pergunta se quer retomar esse caminho.

### Busca nos menus e listas

Ao abrir um menu ou uma lista do Tasy, o Ataho coloca um campo **Filtrar** no topo. Digite parte do texto (acentos e maiúsculas não importam) para encontrar a opção sem rolar a lista.

**Menu de navegação da função** (ex.: Convênio, Regras, Preços…):

![Filtro no menu de navegação](assets/busca-menu-navegacao.png)

**Menu de três pontinhos**, com todas as abas que não cabem na tela:

![Filtro no menu de três pontinhos](assets/busca-tres-pontos.png)

![Menu de três pontinhos filtrado](assets/busca-tres-pontos-filtrado.png)

**Campos de seleção** nos filtros e nos formulários de inserção de dados:

![Filtro em campo de seleção](assets/busca-select-campo.png)

A busca pode ser desligada em **Preferências**, no ícone do Ataho.

### Mapear tela

Mostra, para cada campo de uma tela do Tasy, as informações técnicas que normalmente exigem abrir o dicionário de dados: atributo, tabela, tipo, tamanho, obrigatoriedade e a lista de valores aceitos.

**1. Escolha a área.** Pressione **Alt + M**. Na barra superior escolha **Mapear blocos** (clique em um bloco) ou **Selecionar área** (clique e arraste). **Esc** cancela.

![Selecionar a área para mapear](assets/mapear-selecionar.png)

**2. Leia o relatório.** O painel **ATAHO MAP // RELATÓRIO** abre ao lado, com um cartão por campo:

- **Label**, **Atributo** (ex.: `CD_CATEGORIA`), **Tabela** (ex.: `CONVENIO_AMB`), **Tipo de atributo**, **Tamanho**, **Obrigatório** (S/N) e **Módulo**.
- A etiqueta no canto do cartão indica o tipo do campo (ex.: **Cadastro**, **Livre**).
- Em **Valores do campo** aparecem os códigos aceitos e suas descrições (ex.: `1 - Particular`, `2 - Desconto AMB`).
- No rodapé, o total de campos mapeados e quantos são obrigatórios.

![Relatório do mapeamento](assets/mapear-relatorio.png)

**3. Veja todos os valores.** Quando o campo tem muitos valores, o cartão mostra só os primeiros e, embaixo, um link como **+34 valores**. Clique nele para abrir a lista completa.

![Campo com +34 valores](assets/mapear-mais-valores.png)

**4. Pesquise e copie na lista completa.** A janela de valores mostra o nome do campo (com botão para copiar o atributo), uma busca por **valor ou descrição** e a quantidade de itens. Ordene clicando em **Valor** ou **Descrição**, navegue com **↑ ↓**, copie o código com **Enter** e feche com **Esc**.

![Lista completa de valores do campo](assets/mapear-valores.png)

**5. Use o relatório.**

- **Filtrar pela label, atributo ou valor** encontra um campo rapidamente.
- **Copiar** manda o relatório para a área de transferência.
- **Salvar .txt / Salvar .json** baixa o relatório como arquivo, pelo download normal do Chrome.
- **Mapear de novo** volta para a seleção de área.
- O indicador **LIVE** acende enquanto o Ataho está lendo os campos; a barra no rodapé mostra o progresso. **—** minimiza e **×** fecha.

O mapeamento só lê a tela. Nada é alterado no Tasy.

## Privacidade

Tudo roda no navegador, na sessão que você já tem no Tasy. Não há servidor próprio, telemetria, nem coleta de senha, cookie ou token. O Ataho não grava nada no Tasy: só navega pela tela como você faria. As permissões de perfil e função continuam sendo as do Tasy.

O último filtro e caminho ficam salvos apenas no seu navegador. Em telas de atendimento ou paciente, o caminho completo fica só durante a troca de perfil e é apagado logo depois.

Este repositório publica o pacote de instalação. O código-fonte **não** é open source.

## Compatibilidade

Chrome e Tasy EMR. Telas e endpoints variam entre ambientes. Teste antes de usar em rotina crítica.

## Problemas e sugestões

Abra uma [issue](https://github.com/fernandobaptistaneto/ataho/issues) com a versão do Chrome, a versão do Tasy e o que aconteceu. **Não publique dados de pacientes, credenciais, tokens nem prints com informação sensível.**

---

Created by Fernando Baptista
