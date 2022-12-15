# Cálculos referente aos horários.

Há 03 tipos de horários em um hospital:
- Horário diurno.
- Horário noturno.
- Horário no regime de 24 horas.

## Problemática

Os cálculos nativos do sistemas (apuração de atrasos e saídas antecipadas) são úteis apenas para os horários diurnos. Já para os horários noturnos e de 24h, o sistema calcula de forma diferente, o que não é interessante para o contexto em que trabalho. Dessa forma, é melhor desconsiderar o cálculo nativo e utilizar um algoritmo mais simples para calcular os atrasos, saídas antecipadas e horas trabalhadas.

