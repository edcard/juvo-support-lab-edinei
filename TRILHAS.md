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

## Troubleshooting

1. Localizar o cliente pelo CPF.
2. Confirmar a CCB informada.
3. Validar que o contrato está assinado.
4. Confirmar que a conta bancária foi validada.
5. Consultar o status do desembolso.
6. Identificar o motivo da retenção.
7. Verificar se existe análise pendente da equipe de Antifraude.
8. Caso não exista liberação automática prevista, escalar o caso para o time responsável pela Antifraude.
9. Registrar todas as evidências no Jira.

## Ação

Escalar para o time de Antifraude devido ao bloqueio ANTIFRAUD_HOLD.

## Resposta ao CX

Foi identificado que o contrato está aprovado e a conta bancária validada. O desembolso encontra-se retido por uma validação de Antifraude (ANTIFRAUD_HOLD). O caso foi encaminhado para a equipe responsável para análise e liberação do pagamento.
