# Cálculos de horários.

## Tipos

Há 03 tipos de horários em um hospital:
- Horário diurno.
- Horário noturno.
- Horário no regime de 24 horas.

## Problemática 01

Os cálculos nativos do sistemas (apuração de atrasos e saídas antecipadas) são úteis apenas para os horários diurnos. Já para os horários noturnos e de 24h (quando há a passagem de dias), o sistema calcula de forma diferente, o que não é interessante para o contexto em que trabalho. Dessa forma, optei por desconsiderar o cálculo nativo e utilizei um algoritmo simples para calcular os atrasos, saídas antecipadas e horas trabalhadas.

## Problemática 02

Para o cálculos de carga horária não encontrei função nativa com esse retorno, logo tive que utilizar cursor e fazer o cálculo da carga horária diária desconsiderando o horário de almoço quando houver.

## Problemática 03

É necessário saber se a batida está na 1ª metade ou na 2ª metade do horário. Para os horários diurnos utilizei (saída-entrada)/2 como hora que delimita a metade de uma carga horária cumprida. No entando, para os horários noturnos e de 24h, por conversão e conveniência, utilizei a virada do dia (00:00).

###### Exemplo 01: Se você tem o horário 07:00-13:00, todos os pontos registrados antes das 10:00 são marcações de entrada, enquanto as marcações posteriores às 10:00 são de saída.

###### Exemplo 02: Se você tem o horário noturno, todos os pontos registrados antes da meia-noite são consideradas marcações de entrada. Logo, todos os pontos registrados no dia seguinte são considerados marcações de saída.

## Linha do tempo

A partir da Entrada e suas tolerâncias, da Saída e suas tolerâncias e da Metade do período de trabalho, podemos calcular os valores necessários para a apuração dos atrasos e saídas antecipadas.

```
@ ---------------------------------------- Cálculo da carga horária diária  -------------------------------- @
@ ---------------------------------------- Recupera valores de tolerâncias  -------------------------------- @
@ ------------------------------------ De acordo com as configurações do horario  -------------------------- @
@                                                                                                            @ 
@                                                                                                            @ 
@                   Hora entrada                     METADE                    Hora saída                    @
@  Tempo > -----*---X----*-----------------------------||------------------*---X----*------ >                @
@               |         entrada tolerância DEPOIS                        |         saída tolerância DEPOIS @
@               entrada tolerância ANTES                                   saída tolerância ANTES            @
```
