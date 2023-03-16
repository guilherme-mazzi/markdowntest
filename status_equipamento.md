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