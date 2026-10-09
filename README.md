# Ataho

**Atalhos inteligentes para sistemas web.**

Extensão para Chrome que acelera o dia a dia no Tasy: troque de perfil, abra funções e volte exatamente para onde você estava, tudo pelo teclado.

![Demonstração do Ataho](assets/tasy-flow-demo.gif)

<p align="center">
  <img src="assets/tasy-flow.png" alt="Paleta Alt+P do Ataho" width="440" />
</p>

> **Versão 1.7.4** · Projeto independente. Não é um produto oficial da Bionexo ou do Tasy.

[![Downloads](https://img.shields.io/github/downloads/fernandobaptistaneto/ataho/total?label=downloads)](https://github.com/fernandobaptistaneto/ataho/releases)

## Download

| Versão | Para quem | Link |
| --- | --- | --- |
| **1.7.4 (mais recente)** | Quer as novidades abaixo | [Ataho.zip](https://github.com/fernandobaptistaneto/ataho/releases/latest/download/Ataho.zip) |
| **1.5.25 (estável)** | Prefere a versão mais testada | [Ataho.zip](https://github.com/fernandobaptistaneto/ataho/releases/download/v1.5.25/Ataho.zip) |

## Novidades da 1.7.4

- **Abrir função (Alt + O):** pesquise qualquer função liberada no seu perfil. As funções já abertas aparecem no topo.
- **Último filtro e último caminho no Alt + O:** embaixo de cada função aparece o último filtro que você aplicou e o último lugar em que estava (registro aberto, menu e abas). Selecione essa linha para abrir a função já filtrada e no mesmo lugar.
- **Troca de perfil volta para onde você estava:** ao trocar de perfil e escolher reabrir, o Ataho reabre a função, aplica o filtro, entra no registro, seleciona o menu e as abas em que você estava.
- **Atendimento do PEP na troca de perfil:** com um atendimento aberto no Prontuário Eletrônico do Paciente, ao trocar de perfil o Ataho reabre o PEP já no mesmo atendimento. Se o novo perfil não tiver acesso ao setor do paciente, aparece um aviso.
- **Mapear tela (Alt + M):** clique em uma área da tela e o Ataho lista todos os campos dela: label, atributo, tabela, tipo, tamanho, obrigatoriedade, valor atual e a lista de valores possíveis de cada campo. Dá para filtrar, copiar e salvar o relatório em .txt ou .json.
- **Trocar estabelecimento (Alt + I):** escolha a empresa e o estabelecimento pela paleta.
- **Busca nos menus dropdown:** um campo de pesquisa aparece nos menus de três pontinhos e nas listas dropdown do Tasy. Dá para desligar no ícone da extensão.
- **Tela de carregamento própria** enquanto o Ataho aplica filtro e caminho, para você saber que ele está trabalhando.

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

1. Pressione **Alt + O** e digite parte do nome da função.
2. **Enter** abre a função.
3. Se aparecer uma linha com a etiqueta **filtro** ou **caminho** embaixo da função, selecione essa linha para abrir já com o último filtro e no último lugar em que você estava.

O Ataho guarda só o **último** filtro e caminho de cada função, separado por estabelecimento. Filtros que já vêm preenchidos pelo Tasy (como "Situação: Ativos") não contam.

### Trocar estabelecimento

1. Pressione **Alt + I**.
2. Escolha a empresa (se houver mais de uma) e depois o estabelecimento.

### Mapear tela

1. Pressione **Alt + M** e clique na área da tela que deseja mapear (**Esc** cancela).
2. O relatório lista cada campo com label, atributo, tabela, tipo, tamanho, se é obrigatório e o valor atual.
3. Clique na quantidade de valores de um campo para ver a lista completa de códigos e descrições; **Enter** copia o valor selecionado.
4. Use **Filtrar** para achar um campo, **Copiar** para a área de transferência ou **Salvar .txt / .json** para guardar o relatório no seu computador.
5. **Mapear de novo** refaz a leitura em outra área.

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
