# Afastamentos

Os afastamentos são situações em que o colaborador estava ausente na jornada. Há afastamentos para o dia todo: férias, atestado médico, licença nojo, licença gozo, etc. Também há afastamentos para pequenos períodos durante a jornada diária de trabalho: justificativa de entrada ou justificativa de saída.

De um modo geral, há uma ou mais situações que motivam a ausência do colaborador em seu posto de trabalho.

Há variáveis/funções na regra LSP que retornam algumas informações de afastamentos.
* QtdAfs[ ] -> Entre os colchetes devemos colocar o código da situação da qual queremos obter informações.

No entanto, não temos uma situação em específico que queremos procurar. Na verdade, queremos encontrar todas as possíveis situações de afastamentos para os dias em processamento. Dessa forma, é mais intuitivo utilizar cursores para fazer a varredura na tabela de histórico.


## Situações especiais

Há algumas situações que são tratadas de forma específica: justificativa de entrada, justificativa de saída, REP em manutenção e troca/repasse de plantões.

Estas situações especiais estão em mudanças esporadicamente, dependendo de normativas e suas interpretações.

## Variáveis de estado.

São variáveis booleanas que indicam sim ou não (0/1). Variáveis de estado determinam os caminhos do fluxo do algoritmo. Estas variáveis são utilizadas em outros trechos do código para a realização de cálculos do atraso ou da saída antecipada.

```
nManutencaoREP = 1;
nPlanFeitoParaOutroFuncion = 1;
nPlanFeitoPorOutroFuncion = 1;
nEntradaJustificada = 1; 
nSaidaJustificada = 1; 
nManutencaoNormal = 1;
```
