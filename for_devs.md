🖥️ For Developers
===
<br>

### Explicação do Código

O código é escrito em Django. Por isso, tem a seguinte estrutura:<br>
Pasta *__monitoring__* representa o App como um todo. Tudo da página (exceto arquivos estáticos) estão aqui.

![](/imgs/cod-pasta.jpg "Text to show on mouseover")

1. __migrations:__ Migrações dos modelos criados em ```models.py``` para o banco de dados. <br>
    ![](/imgs/migrations.jpg "Text to show on mouseover")<br>
    - ```0001_initial .py```**:** Migração dos modelos para o banco de dados. Caso houvessem mais migrações, os números iniciais do nome do arquivo seriam outros.
<br>

2. __templates:__ Arquivos ```HTML``` do App são guardados aqui.<br>
![](/imgs/templates.jpg "Text to show on mouseover")<br>
    - ```monitor.html```**:** Cada arquivo ```HTML``` para cada função da página.
<br>

3. __tests:__ Arquivos para fazer os testes do App.<br>
![](/imgs/tests.jpg "Text to show on mouseover")<br>
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


---

### [👋Início](README.md)

### [🔨Status do Equipamento](status_equipamento.md)

### [📊Gráfico Tree Map](grafico_treemap.md)

### [📅Tabela Grid](tabela_grid.md)

### [❗ Funcionalidades Extras](func_extras.md)

---
