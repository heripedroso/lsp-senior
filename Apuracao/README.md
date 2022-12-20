# Apuração/Cálculo

O algoritmo calcula os atrasos/saídas antecipadas levando em consideração se o horário é DIURNO, NOTURNO ou 24H. Para tal, utilizam-se as variáveis de estado ehHorarioNoturno e ehHorario24h.

## Variáveis e funções nativas

Alguns dos recursos de apuração do Sênior não foram utilizados, já que percebe-se que não estão no contexto da instituição. Além disso, parece calcular corretamente apenas para horários diurnos. Para os horários noturnos e de 24h os cálculos são diferentes e por isso não são aplicáveis.
```
@nHorasTrabalhadasNoDia = HorStg[1];@ 
@nHorasAtrasoNoDia = HorStg[103];  Sênior calcula errado. @
@nHorasSaidaAntecipadaNoDia = HorStg[101];  Sênior calcula errado. @  
@nHouveMarcacaoInvalida = HorStg[999];@ 
@nHorasFalta = HorStg[15];@ @ Sênior calcula as faltas em minutos. Não serve para o nosso caso. @   
```
