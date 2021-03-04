# Dashboard-Financeiro

Essa é apenas uma dashboard de visualização de dados contendo algumas medidas calculadas
This is a data visualization on Power BI with some measures.



## Explicando os Painéis / Explaining the Panels

Primeiro e segundo painel temos uma etiqueta a qual nos informa o total de entradas e saídas.

In the first and second panels, we have a card with the total inflows and outflows of cash.

Entradas/Inflow
```
Faturamento = 
CALCULATE(SUM(Movimentacoes[Valor da Movimentação]),Movimentacoes[Tipo]="Recebimento")
```
Saída/Outflow
```
Custos = 
CALCULATE(SUM(Movimentacoes[Valor da Movimentação]),Movimentacoes[Tipo]="Pagamento")
```
\
No terceiro e quarto painel temos um grafico de cascata, que nos informa o lucro mensal e no quarto temos um gráfico de rosca informando a margem de lucro.

In the third and fourth panels, we have a cascade graph that shows the total profits and the donut chart shows the profit margin

Lucro/Profits
```
Lucro = SUM(Movimentacoes[Valor da Movimentação])
```

Margem/Margin
```
Margem = [Lucro]/[Faturamento]
```

```
% Custos = 1-[Margem]
```
\
No último painel temos a localização de onde ocoreram as movimentações de dinheiro
In the last panel, we have the location of the places.


![This is a alt text.](https://github.com/msoaresrocha/Dashboard--Financeiro/blob/main/Dashboard%20Financeiro/Foto%20Dashboard%20Financeiro.jpg)
