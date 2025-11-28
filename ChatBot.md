stateDiagram
  direction TB

  [*] --> S0
  S0 --> S1: saudação

  S1 --> S2: pedir esfirras
  S1 --> S5: pedir bebida

  S2 --> S3: escolher sabor
  S3 --> S3A: informar quantidade
  S3A --> S2: adicionar outro sabor
  S3A --> S4: seguir

  S4 --> S5: adicionar bebida
  S4 --> S7: sem bebida

  S5 --> S6: escolher bebida
  S6 --> S7: informar quantidade

  S7 --> S8: forma de pagamento
  S8 --> S9: confirmar pedido
  S8 --> S1: cancelar

  S9 --> [*]: encerrar
