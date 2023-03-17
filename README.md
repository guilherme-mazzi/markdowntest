👋 Bem vindo ao App de Status - Portal SEMEQ
===
*Utilização, acesso e funcionamento da tela de Status do Portal SEMEQ*
<br>

### Overview
Essa documentação tem como objetivo identificar o acesso a tela de Status, e como utilizar a funcionalidade de visualização das informações de equipamentos, sensores e plantas.

### Tecnologias utilizadas no desenvolvimento:

```shell
- Python 3.10 - [docs.python.org/pt-br/3.10/](https://docs.python.org/pt-br/3.10/)
- Django 4.1.3 - [docs.djangoproject.com/pt-br/4.1/](https://docs.djangoproject.com/pt-br/4.1/)
- PlotlyJS 2.18.2 - [/plotly.com/python/](https://plotly.com/python/)
- Pandas 1.5.1 - [pandas.pydata.org/docs/index.html](https://pandas.pydata.org/docs/index.html)
- Numpy 1.23.4 - [numpy.org/doc/1.23/](https://numpy.org/doc/1.23/)
- Git - [git-scm.com/doc](https://git-scm.com/doc)
- Docker 8.7.4 - <linkDoc>
- PostgreSQL 8.7.4 - <linkDoc>
- MongoDB 5.0.15 Enterprise - [www.mongodb.com/docs/v5.0/](https://www.mongodb.com/docs/v5.0/)
```
> **DICA:** Recomendado ler em Inglês


### [🚀Informações de Acesso](#entrar-com-login) 

### [🔨Funcionamento](status_equipamento.md)

### [🖥️Para Desenvolvedores](for_devs.md)
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

### [🔨Status do Equipamento](status_equipamento.md)

### [📊Gráfico Tree Map](grafico_treemap.md)

### [📅Tabela Grid](tabela_grid.md)

### [❗ Funcionalidades Extras](func_extras.md)

### [🖥️Para Desenvolvedores](for_devs.md)

---
