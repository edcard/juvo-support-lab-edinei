# trilhas
# IT-2001 - Desembolso ao cliente

## Resumo

Cliente informa que assinou o contrato no dia anterior e ainda não recebeu o PIX.

## Análise

Ao consultar o sistema interno pelo CPF, foi identificado:

- Contrato: Assinado
- CCB: 90001001
- Crédito: Aprovado
- Banco validado: Sim
- Status do desembolso: Aguardando desembolso
- Motivo do bloqueio: ANTIFRAUD_HOLD

## Ação

Escalar para o time de Antifraude devido ao bloqueio ANTIFRAUD_HOLD.

## Resposta ao CX

Foi identificado que o contrato está aprovado e a conta bancária validada. O desembolso encontra-se retido por uma validação de Antifraude (ANTIFRAUD_HOLD). O caso foi encaminhado para a equipe responsável para análise e liberação do pagamento.

============================================================================================

# IT-2008 - Desembolso ao cliente

## Resumo

Cliente informa que assinou o contrato no dia anterior e ainda não recebeu o PIX.

## Análise

Ao consultar o sistema interno pelo CPF, foi verificado que:

- Contrato: recusado
- CCB: 90008001
- Crédito: Aprovado
- Banco validado: Sim
- Status do desembolso: cancelado
- Motivo recusa: RECUSA_CREDITO

## Troubleshooting

1. Localizar o cliente pelo CPF.
2. Confirmar a CCB informada.
3. Validar o status do contrato.
4. Consultar o status do desembolso.
6. Identificar o motivo da recusa do contrato.
7. Encaminhar para a equipe de crédito verificar.
8. Registrar todas as evidências no Jira.

## Ação

Encaminhar para a equipe de contratos/créditos verificar o que ocorreu.

## Resposta ao CX

Foi identificado que o contrato e o crédito foram recusados, enviado para a equipe  responsável para análise e liberação ou não do PIX.

========================================================================================

# IT-2011 - Desembolso ao cliente 902.888.888-08

## Resumo

Desembolso ao cliente

## Análise

Ao consultar o sistema interno pelo CPF e CCB, foi verificado que:

- Contrato: assinado
- CCB: 90008002
- Crédito: Aprovado
- Banco validado: Sim
- Status do desembolso: aguardando desembolso

## Causa
 Falha na integração/envio de Pix nessa nova proposta.

## Ação

Executar rotina de reprocessamento (Pagamento/Pix) para esse CCB 90008002

## Resposta ao CX

Não se trata do mesmo problema da CCB anterior. A CCB 90008001 (ticket IT-2008) foi recusada, porém a CCB 90008002 foi aprovado e estava pendente apenas do reprocessamento do Pix. 
Feito o reprocessamento do Pix, pedir para cliente validar o recebimento.
