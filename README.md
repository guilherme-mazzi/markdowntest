👋 Bem vindo ao App de Status - Portal SEMEQ
===
*Utilização, acesso e funcionamento da tela de Status do Portal SEMEQ*
<br>

### Overview
Essa documentação tem como objetivo identificar o acesso a tela de Status, e como utilizar a funcionalidade de visualização das informações de equipamentos, sensores e plantas.

### Tecnologias utilizadas no desenvolvimento:

```shell
- Django 8.7.4 - <linkDoc>
```

### [🚀Informações de Acesso](#entrar-com-login) 

### [🔨Funcionamento](#como-funciona)

### [🖥️Para Desenvolvedores](#explicação-do-código)
<br>

---
🚀 Como acessar
===
*Informações de como acessar a tela de Status*
<br>

### Entrar com login
Acesse seu navegador e entre no link [portal-stream.semeq.com](https://portal-stream.semeq.com). Ao entrar no link, um login será necessário para acessar o menu do Portal, solicitando usuário e senha. Caso tenha esquecido sua senha, clique em "esqueceu a senha" abaixo do campo de senha e siga os passos.

> ⚠️: Não é possível criar uma conta a partir desta tela.

![Tela de login](/imgs/login.jpg "Tela de Login")

Após seu login, a tela abaixo será exibida:

![Tela de login](/imgs/menu-inicial.jpg "Tela de Login")

> __Dica__: Você pode escolher o tema do site caso sua preferência não esteja de acordo. Para isso, basta clicar em "Black" (preto) ou "White" (branco) no canto inferior direito.

### Como acessar a tela de Status
Com seu usuário autenticado, o seguinte menu será exibido. Para acessar a tela de Status, clique em análise, localizado no menu do centro da tela, ou no cabeçalho acima da tela, indicados por setas no exemplo abaixo:

![Tela de login](/imgs/menu-sublinhado.jpg "Tela de Login")
<br>

---
💡 Como apresentar as análises
===
*O que a tela apresenta e como exibir*
<br>

### Como apresentar os dados
Para apresentar os dados, primeiramente, precisará selecionar a corporação e a planta. Para isso, vá ao menu lateral na esquerda (caso o menu esteja encolhido, coloque o ponteiro do mouse na lateral, ou clique no ícone de três riscos no canto superior esquerdo), certifique-se que "Status" esteja em destaque, e selecione a corporação e a planta desejada.

![](/imgs/gifs/menu-lateral.gif "Text to show on mouseover")

Também, será necessário definir o serviço. Isso pode ser escolhido no canto superior direito da tela, onde uma seleção irá se apresentar para ser selecionado o serviço.

![](/imgs/gifs/dropdown.gif "Text to show on mouseover")

Caso tudo seja informado corretamente, será apresentada a seguinte tela:

![](/imgs/status-inteiro.jpg "Text to show on mouseover")

> __Dica__: Em caso de preferência, onde muita informação parece estar sendo apresentada ao mesmo tempo, pode-se alterar os níveis de Tree Map do gráfico, no menu lateral. Quanto menos níveis selecionados, menos seções são informadas no gráfico. Exemplo abaixo.
>
>![](/imgs/gifs/treemap-nivel.gif "Text to show on mouseover")

Gráfico da planta em 4 níveis:
![](/imgs/graf-4niveis.jpg "Text to show on mouseover")

Gráfico da planta em 3 níveis:
![](/imgs/graf-3niveis.jpg "Text to show on mouseover")

<br>

---

### [🔨Status do Equipamento](#status-do-equipamento)

### [📊Gráfico Tree Map](#gráfico-tree-map)

### [📅Tabela Grid](#tabela-grid)

---
🔨 Status do Equipamento
===
*Dados do estado dos equipamentos*
<br>

### Como funciona
Primeiro, os estados são diferentes baseados no serviço selecionado (telemetria, temperatura e vibração). Após escolher o serviço, os dados apresentados a esquerda da tela são as quantidades de equipamentos em cada estado, separados em alarme🔴, alerta🟡, normal🟢 e parado⚪. Também, o quantitativo de dispositivos com bateria baixa🟠 e sinal baixo🟣.

> ⚠️: No caso do serviço telemetria, bateria baixa🟠 e sinal baixo🟣 não serão apresentados, pois não existem essas informações para este serviço.

![](/imgs/status-qntd.jpg "Text to show on mouseover")

> **Alarme**🔴 (vermelho) - Quantidade de equipamentos em estado "alarme";
>**Alerta**🟡(amarelo) - Quantidade de equipamentos em estado "alerta";
>**Normal**🟢(verde) - Quantidade de equipamentos em estado "normal";
>**Parado**⚪(cinza) - Quantidade de equipamentos em estado "parado".

Para o equipamento ser definido como "parado", o sensor não deve emitir sinal nas últimas 24h.
O estado de bateria baixa🟠 é identificado quando o dispositivo está com menos de 40% de bateria. Para sinal baixo🟣, o dispositivo precisa ter um nível de sinal inferior a 10%.
<br>

---
📊 Gráfico Tree Map
===
*Agrupamento de equipamentos da planta e seus respectivos estados.*
<br>

### Como funciona
O gráfico é separado em um agrupamento de seções: **Planta** -> **Área** -> **Setor** -> **Máquina** -> **Equipamento**. A **planta** é o local onde os **equipamentos** estão situados ([selecionado anteriormente](#como-apresentar-os-dados)), fazendo parte de uma corporação. Nome da **planta** é definido pela localização. Tudo estará dentro desta seção, e é identificada no topo do gráfico em preto.

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

De dentro para fora, temos os **equipamentos**, cada cor representa o status do **equipamento** ([explicado acima](#como-funciona)). Para o conjunto que agrupa essas informações (no caso, a **máquina**), a cor é representada por uma média dos estados contidos na seção.

A coloração da **máquina** é representada por uma média dos status dos **equipamentos**. Se a maioria dos **equipamentos** estiverem em estado "alerta🔴", a coloração do bloco da **máquina** se transforma em um tom vermelho. Em caso de maioria em estado "normal🟢", a coloração é verde e, em caso de "parado⚪", a coloração é cinza.

![](/imgs/maquina-alerta.jpg "Máquina alerta, e seus equipamentos.") 
![](/imgs/maquina-normal.jpg "Máquina normal, e seus equipamentos.")
![](/imgs/maquina-parada.jpg "Máquina parada, e seus equipamentos.")

O mesmo se aplica para os outros blocos. O **setor** se colore baseado na média de estado das **máquinas** e a **área** se colore baseado na média de estado dos **setores**.

A partir desses dados, o analista pode decidir as prioridades de onde serão as próximas análises.


---
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


---
❗ Funcionalidades Extras
===
*Recursos extras do App de Status*
<br>

### Print Screen

Nos gráficos, um ícone de uma câmera fotográfica pode ser encontrado no canto superior direito. Clicando no ícone, uma print screen (captura de tela) será realizada do gráfico no estado atual.

![](/imgs/gifs/png-print.gif "Text to show on mouseover")

Após o clique no botão, uma imagem será baixada no seu navegador. Essa imagem é a print screen em questão.

![](/imgs/img-download.jpg "Text to show on mouseover")

### Zoom

Para o gráfico de estado, na esquerda da tela, um zoom pode ser feito para melhor compreensão, caso preferível. Esse zoom pode ser feito segurando o botão esquerdo do mouse e arrastando até que a área desejada seja coberta, conforme o exemplo a seguir:

![](/imgs/gifs/zoom-status.gif "Text to show on mouseover")

Para retornar ao estado padrão do gráfico, clique em um dos dois botões apresentados na imagem abaixo, localizados no canto superior do gráfico, próximo ao botão de print screen.

![](/imgs/scale.jpg "Text to show on mouseover")

### Exportar como Excel

No grid, pode ser utilizado uma funcionalidade encontrada no botão "Export" (localizado logo acima da tabela), que permite o usuário realizar o download do grid em formato de Excel.

![](/imgs/botao-export.jpg "Text to show on mouseover")

Após o clique do botão, um download de um arquivo será iniciado. Esse arquivo é a tabela em formato excel, podendo ser aberto pelo Excel.

![](/imgs/excel.jpg "Text to show on mouseover")

### Pesquisa

Uma caixa de pesquisa também é disponibilizada acima da tabela. Qualquer informação requerida será buscada na tabela.

![](/imgs/gifs/search-table.gif "Text to show on mouseover")


---
🖥️ For Developers
===
<br>

### Explicação do Código

O código é escrito em Django. Por isso, tem a seguinte estrutura:
Pasta *__monitoring__* representa o App como um todo. Tudo da página (exceto arquivos estáticos) estão aqui.

![](/imgs/cod-pasta.jpg "Text to show on mouseover")

1. __migrations:__ Migrações dos modelos criados em ```models.py``` para o banco de dados.

    ![](/imgs/migrations.jpg "Text to show on mouseover")
    - ```0001_initial .py```**:** Migração dos modelos para o banco de dados. Caso houvessem mais migrações, os números iniciais do nome do arquivo seriam outros.
<br>

2. __templates:__ Arquivos ```HTML``` do App são guardados aqui.

![](/imgs/templates.jpg "Text to show on mouseover")
    - ```monitor.html```**:** Cada arquivo ```HTML``` para cada função da página.
<br>

3. __tests:__ Arquivos para fazer os testes do App.

![](/imgs/tests.jpg "Text to show on mouseover")
    - ```test.py```**:** Arquivos que começam com "*__test__*" indicam um arquivo de teste em ```Python```.
<br>

4. ```__init__.py```**:** Arquivo para identificar a pasta como Módulo ```Django```. Não utilizado.

5. ```admin.py```**:** Define os modelos para exibir na url ```portal-stream.semeq.com/admin```.Nenhum sendo exibido.

6. ```apps.py```**:** Padrão ```Django```. Algumas configurações básicas do app. 

7. ```models.py```**:** Modelos de dados para serem enviados ao banco de dados ou usados de base no código.

8. ```urls.py```**:** Importando as ```views.py```, aqui define-se os caminhos para renderizar as *views*.

9. ```utils.py```**:** Toda a lógica se encontra aqui. Funções para as funcionalidades e suas consultas ao banco de dados. Código em ```Python```

10. ```views.py```**:** Define qual ```HTML``` renderiza e seu contexto (variáveis para se usar na página).
<br>


### GitHub

Caso deseje conferir os códigos do Portal afim de tirar dúvidas, acesse o GitHub do Portal - SEMEQ:

> https://github.com/semeqpd/portal_stream
>
> ⚠️: Necessário pedir a autorização para acessar os códigos no GitHub
