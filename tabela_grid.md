📅 Tabela Grid
===
*Descrição da tabela e dos dados apresentados*
<br>

### Como funciona

O grid, localizado na parte baixa da tela, apresenta os dados dos equipamentos que estão atualmente no gráfico. Você pode descê-lo com o botão do meio do mouse ou com a barra lateral.

![](/imgs/gifs/scroll-tabela.gif "Text to show on mouseover")

> ⚠️: Em alguns casos onde a tela seja pequena, a tabela precisará ser deslizada horizontalmente. Para melhor visualização, encolha o menu lateral como mostrado abaixo.
>
>![](/imgs/gifs/left-scroll-tabela.gif "Text to show on mouseover")

É possível também ordenar os dados com base nas colunas. Clicando no topo da coluna que deseja, a tabela automaticamente se ordena a partir do menor ao maior. Caso queira do maior para menor, apenas clique novamente na coluna.

![](/imgs/gifs/ordering.gif "Text to show on mouseover")

### Dados dinâmicos
Uma das funcionalidades da tabela são os dados dinâmicos, onde clicando em um local do gráfico, ou no quantitativo de estado, a tabela filtra os dados a partir da onde voce clicou, conforme o exemplo:

![](/imgs/gifs/ordering-treemap-table.gif "Text to show on mouseover")

Ao clicar na máquina, a tabela automaticamente se atualiza com os dados apresentados no gráfico. Isso também pode ser feito com o estado do equipamento na esquerda. Exemplo abaixo:

![](/imgs/gifs/ordering-treemap-status.gif "Text to show on mouseover")

### Colunas
Uma descrição de cada coluna apresentada na tabela:

- __Área__ - Nome da área onde o equipamento se encontra.
- __Setor__ - Nome do setor onde o equipamento se encontra.
- __Conjunto__ - Nome e tag do conjunto (ou máquina) em que o equipamento faz parte.
- __Equipamento__ - Nome e tag do equipamento.
- __Data__ - Última data medida do equipamento.
- __Dispositivo__ - Serial Number do dispositivo.
- __Direção__ - Eixo de medição do dispositivo(X, Y, Z).
- __Versão__ - Versão do dispositivo.
- __Gateway__ - Serial Number do gateway que transmitiu esta medida.
- __Bateria__ - A porcentagem de bateria do sensor.
- __Sinal__ - Nível do sinal BLE em porcentagem do dispositivo.
- __Temperatura__ - Temperatura medida pelo dispositivo em Celsius.
- __Status__ - Cor do estado do equipamento.

### Botão para análise

Na última coluna do grid, um ícone é exibido em cada equipamento. Ao clicar nesse botão, voce será redirecionado para a página de análise do equipamento selecionado (tela de "Analisador"), conforme o exemplo a seguir: 

![](/imgs/gifs/analisador.gif "Text to show on mouseover")
<br>

---

### [👋Início](README.md)

### [🔨Status do Equipamento](status_equipamento.md)

### [📊Gráfico Tree Map](grafico_treemap.md)

### [❗ Funcionalidades Extras](func_extras.md)

### [🖥️Para Desenvolvedores](for_devs.md)

---
