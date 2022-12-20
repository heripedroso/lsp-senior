# Apuração/Cálculo

O algoritmo calcula os atrasos/saídas antecipadas levando em consideração se o horário é DIURNO, NOTURNO ou 24H. Para tal, utilizam-se as variáveis de estado ehHorarioNoturno e ehHorario24h.

## Variáveis e funções nativas

Alguns dos recursos de apuração do Sênior não foram utilizados, já que percebe-se que não estão no contexto da instituição.

## Dia posterior (horário noturno e de 24 horas)

Os horários noturnos possuem marcações em 02 dias, sendo que no 1º dia está a entrada e no 2º dia a saída.
```
HorApg[1] ocorre em DatPro @ Hoje @
HorApg[2] ocorre em (DatPro +1) @ Amanhã @
``` 

