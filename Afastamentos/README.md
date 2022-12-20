# Afastamentos

Os afastamentos são situações em que o colaborador estava ausente na jornada. Há afastamentos para o dia todo: férias, atestado médico, licença nojo, licença gozo, etc. Também há afastamentos para pequenos períodos durante a jornada diária de trabalho: justificativa de entrada ou justificativa de saída.

De um modo geral, há uma ou mais situações que motivam a ausência do colaborador em seu posto de trabalho.

Há variáveis/funções na regra LSP que retornam algumas informações de afastamentos.
* QtdAfs[ ] -> Entre os colchetes devemos colocar o código da situação da qual queremos obter informações.

No entanto, não temos uma situação em específico que queremos procurar. Na verdade, queremos encontrar todas as possíveis situações de afastamentos para os dias em processamento. Dessa forma, é mais intuitivo utilizar cursores para fazer a varredura na tabela de histórico.
