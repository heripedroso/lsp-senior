# Apuração/Cálculo

O algoritmo calcula os atrasos/saídas antecipadas levando em consideração se o horário é DIURNO, NOTURNO ou 24H. Para tal, utilizam-se as variáveis de estado ehHorarioNoturno e ehHorario24h.

## Variáveis e funções nativas

Alguns dos recursos de apuração do Sênior não foram utilizados, já que percebe-se que não estão no contexto da instituição. Além disso, parece calcular corretamente apenas para horários diurnos. Para os horários noturnos e de 24h os cálculos são diferentes.
```
@nHorasTrabalhadasNoDia = HorStg[1];@ 
@nHorasAtrasoNoDia = HorStg[103];  Sênior calcula errado. @
@nHorasSaidaAntecipadaNoDia = HorStg[101];  Sênior calcula errado. @  
@nHouveMarcacaoInvalida = HorStg[999];@ 
@nHorasFalta = HorStg[15];@ @ Sênior calcula as faltas em minutos. Não serve para o nosso caso. @   
```         

## Dia posterior (horário noturno e de 24 horas)

Os horários noturnos possuem marcações em 02 dias, sendo que no 1º dia está a entrada e no 2º dia a saída.
```
@ HorApg[1] -> primeira marcação @
@ HorApg[2] -> segunda marcação @

@ HorApg[1] ocorre em DatPro - hoje @
@ HorApg[2] ocorre em (DatPro +1) - amanhã @
``` 

Os horários de 24h necessitam marcar o 1º e o 2º dia, já que o Sênior parece não tratar esse tipo de horário de forma nativa.
