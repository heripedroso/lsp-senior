# Marcações - pontos biométricos registrados.

O algoritmo utiliza 03 variáveis que serão responsáveis pelos cálculos de atrasos/saídas antecipadas/faltas.

```
nPrimeiraMarcacaoEntradaValida = 0;   
nUltimaMarcacaoSaidaValida = 0;
nMarcacaoCompensacao = 0;     
```

O algoritmo dá preferência para a primeira marcação que entra na tolerância da entrada. Se não houver marcação dentro da tolerância, a variáveis permanecerá zerada, indicando que não houve marcação válida. Dando preferência para a primeira marcação de entrada, marcações posteriores que configurem atraso serão desconsideradas.

Da mesma maneira, o algoritmo dá preferência para a última marcação de saída dentro da tolerância, de forma que possa desconsiderar marcações anteriores que configurem saída antecipada.

## Falta calculada

O sistema sênior calcula a falta em horas, o que é completamente fora do contexto da instituição. Logo, optei por verificar se tanto a marcação de entrada e a marcação de saída estão ausentes (zeradas). Caso não haja marcações de entrada e nem saída, isso configura uma FALTA.
