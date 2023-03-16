📊 Gráfico Tree Map
===
*Agrupamento de equipamentos da planta e seus respectivos estados.*
<br>

### Como funciona
O gráfico é separado em um agrupamento de seções: **Planta** -> **Área** -> **Setor** -> **Máquina** -> **Equipamento**. A **planta** é o local onde os **equipamentos** estão situados ([selecionado anteriormente](README.md)), fazendo parte de uma corporação. Nome da **planta** é definido pela localização. Tudo estará dentro desta seção, e é identificada no topo do gráfico em preto.

> Dica: Para expandir o bloco, basta clicar no nome ao topo da seção. Para retrair o bloco, clique na seção desejada no topo do gráfico ou novamente no nome. Exemplo abaixo.
>
>![](/imgs/gifs/expandind-blocks.gif "Text to show on mouseover")

As **áreas**, então, são apresentadas como blocos no interior da **planta**, onde dentro das **áreas**, são agrupados os **setores**.

![](/imgs/areas.jpg "Áreas indicadas com setas vermelhas.")
![](/imgs/setor.jpg "Setor expandido. Nome do setor indicado por uma seta.")

No interno do **setor**, temos um agrupamento de **máquinas** (ou **coleções**) que dentro de cada **máquina**, existem os **equipamentos** da mesma.

![](/imgs/maquina.jpg "Máquina e seus equipamentos. Nome da máquina indicado por uma seta.")

### Leitura e interpretação dos dados do gráfico
Em uma visão geral, conseguimos identificar cores em cada seção apresentada, apenas com exceção da **planta** no topo do gráfico.

De dentro para fora, temos os **equipamentos**, cada cor representa o status do **equipamento** (explicado na página de [Status do Equipamento](status_equipamento.md)). Para o conjunto que agrupa essas informações (no caso, a **máquina**), a cor é representada por uma média dos estados contidos na seção.

A coloração da **máquina** é representada por uma média dos status dos **equipamentos**. Se a maioria dos **equipamentos** estiverem em estado "alerta🔴", a coloração do bloco da **máquina** se transforma em um tom vermelho. Em caso de maioria em estado "normal🟢", a coloração é verde e, em caso de "parado⚪", a coloração é cinza.

![](/imgs/maquina-alerta.jpg "Máquina alerta, e seus equipamentos.") 
![](/imgs/maquina-normal.jpg "Máquina normal, e seus equipamentos.")
![](/imgs/maquina-parada.jpg "Máquina parada, e seus equipamentos.")

O mesmo se aplica para os outros blocos. O **setor** se colore baseado na média de estado das **máquinas** e a **área** se colore baseado na média de estado dos **setores**.

A partir desses dados, o analista pode decidir as prioridades de onde serão as próximas análises.


---

### [🔨Status do Equipamento](status_equipamento.md)

### [📅Tabela Grid](tabela_grid.md)

### [❗ Funcionalidades Extras](func_extras.md)

### [🖥️Para Desenvolvedores](for_devs.md)

---