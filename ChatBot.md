%% Diagrama de Estados – Chatbot Esfirras J&A

stateDiagram
  direction TB

  [*] --> S0

  S0 --> S1: "saudação recebida\n(oi/olá/bom dia)"

  S1 --> S2: "quero pedir esfirras"
  S1 --> S5: "quero bebida"
  S1 --> S1: "entrada inválida"

  S2 --> S3: "sabor válido"
  S2 --> S2: "sabor inválido"

  S3 --> S3A: "quantidade válida"
  S3 --> S3: "quantidade inválida"

  S3A --> S2: "sim\n(outro sabor)"
  S3A --> S4: "não\n(sem mais sabores)"
  S3A --> S3A: "resposta inválida"

  S4 --> S5: "sim\n(desejo bebida)"
  S4 --> S7: "não\n(ir para pagamento)"
  S4 --> S4: "resposta inválida"

  S5 --> S6: "bebida válida"
  S5 --> S5: "bebida inválida"

  S6 --> S7: "quantidade válida"
  S6 --> S6: "quantidade inválida"

  S7 --> S8: "pagamento válido"
  S7 --> S7: "pagamento inválido"

  S8 --> S9: "confirmar pedido"
  S8 --> S1: "cancelar pedido"
  S8 --> S8: "resposta inválida"

  S9 --> [*]: "sim\n(encerrar)"
  S9 --> S9: "outra resposta"

  %% Labels descritivos dos estados
  S2: ESCOLHER_SABOR
  S3: ESCOLHER_QUANTIDADE
  S3A: ADICIONAR_OUTRO_SABOR
  S4: DESEJA_BEBIDA
  S5: ESCOLHER_BEBIDA
  S6: QUANTIDADE_BEBIDA
  S7: PAGAMENTO
  S8: CONFIRMAR
  S9: FINALIZADO
