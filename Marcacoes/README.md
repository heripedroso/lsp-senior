# Marcações - pontos biométricos registrados.

O algoritmo utiliza 03 variáveis que serão responsáveis pelos cálculos de atrasos/saídas antecipadas/faltas.

```
nPrimeiraMarcacaoEntradaValida = 0;   
nUltimaMarcacaoSaidaValida = 0;
nMarcacaoCompensacao = 0;     
```

O algoritmo dá preferência para a primeira marcação que entra na tolerância da entrada. Se não houver marcação dentro da tolerância, a variável permanecerá zerada, indicando que não houve marcação válida. Dando preferência para a primeira marcação de entrada, marcações posteriores que configurem atraso serão desconsideradas.

Da mesma maneira, o algoritmo dá preferência para a última marcação de saída dentro da tolerância, de forma que possa desconsiderar marcações anteriores que configurem saída antecipada.

Para compensar algum atraso, as marcações até 30 minutos após a saída são configuradas como compensação. Após esse limite a compensação não acumula, permanecendo o máximo de 30 minutos.

## Falta calculada

O sistema sênior calcula a falta em horas, o que é completamente fora do contexto da instituição. Logo, optei por verificar se tanto a marcação de entrada e a marcação de saída estão ausentes (zeradas). Caso não hajam marcações de entrada e nem saída, essa condição configura uma FALTA.

## Marcações do 2º vínculo

Profissionais da saúde e do magistério são permitidos possuir mais de um vínculo. Dessa forma, há profissionais que possuem 02 jornadas em períodos distintos. O sistema Sênior apura somente o 1º vínculo. O problema encontra-se no 2º vínculo no qual não há registro de nenhuma marcação. Para contornar esta situação, utiliza-se uma função nativa que lê novamente os pontos registrados do 1º vínculo e comprada com as tolerâncias do horário do 2 º vinculo. Desta forma, todas as marcações do profissional são utilizadas no cálculo dos dois vínculos.
