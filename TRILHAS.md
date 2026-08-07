Ticket IT-2001 (Desembolso ao cliente - Antifraude)
1. Onde consulto primeiro

Sistema interno → contrato 90001001 / CPF → aba pagamentos e segurança.

2. O que busco

Status do contrato, Status do desembolso?, e se existe algum bloqueio de segurança ou pendência na proposta.

3. O que encontrei

CSV: contrato_status=assinado, credito_status=aprovado, banco_validado=sim, desembolso_status=aguardando_desembolso, bloqueio_motivo=ANTIFRAUD_HOLD.

4. Hipótese

Contrato e crédito estão aprovados, mas o Pix não foi enviado porque o sistema ativou uma trava preventiva do módulo de Antifraude (ANTIFRAUD_HOLD).

5. Retry/reprocesso

N/A - não cabe reprocessar enquanto houver trava de segurança ativa.

6. Correção manual

N/A - a liberação depende de análise da equipe especializada.

7. Escalação

Escalar ticket para o time de Antifraude/Risco solicitando a análise e liberação do bloqueio ANTIFRAUD_HOLD.

8. Comunicação

@agente.cx Contrato aprovado e banco validado. O desembolso está retido por uma trava preventiva de Antifraude (ANTIFRAUD_HOLD). Encaminhado ao time responsável para análise e liberação.

9. Status final

EM ANDAMENTO / ESCALADO

============================================================================================

Ticket IT-2008 (Desembolso ao cliente - CCB 90008001)
1. Onde consulto primeiro

Sistema interno → contrato 90008001 / CPF 902.888.888-08 → aba proposta/crédito.

2. O que busco

Status da CCB 90008001, Status do crédito?, e se Eexiste valor aprovado pendente de envio.

3. O que encontrei

CSV: contrato_status=recusado, credito_status=recusado, banco_validado=sim, desembolso_status=cancelado, recusa_motivo=RECUSA_CREDITO.

4. Hipótese

Solicitação de reprocessamento é indevida; a proposta foi recusada (RECUSA_CREDITO) e o desembolso foi cancelado.

5. Retry/reprocesso

N/A - não cabe reprocessamento de Pix para propostas recusadas.

6. Correção manual

N/A - não há valor a ser liberado.

7. Escalação

N/A - caso resolvido via consulta de dados; alinhar motivo com equipe de Crédito/Contratos se necessário.

8. Comunicação

@agente.cx07 A CCB 90008001 foi recusada pela equipe de crédito (RECUSA_CREDITO) e consta como cancelada. Não cabe reprocessamento de Pix. 

9. Status final
    
Cancelado/resolvido

========================================================================================

Ticket IT-2011 (Desembolso ao cliente - CCB 90008002)
1. Onde consulto primeiro

Sistema interno → contrato 90008002 / CPF 902.888.888-08 → aba pagamentos e integração Pix.

2. O que busco

Status da CCB 90008002. Se o status é diferente da CCB anterior e o status da transação Pix.

3. O que encontrei

CSV: contrato_status=assinado, credito_status=aprovado, banco_validado=sim, desembolso_status=aguardando_desembolso.

4. Hipótese

Não é o mesmo problema do IT-2008. A CCB 90008002 está aprovada e sofreu apenas uma falha temporária na integração de envio do Pix.

5. Retry/reprocesso

Executar rotina de reprocessamento (retry) do pagamento/Pix para a CCB 90008002.

6. Correção manual

N/A - reprocessamento via sistema resolve a pendência.

7. Escalação

N/A - ação operacional realizada diretamente pelo suporte.

8. Comunicação
@agente.cx07 Não é o mesmo caso da outra CCB. A CCB 90008002 foi aprovada e o Pix foi reprocessado com sucesso. 
Pedir para cliente validar o recebimento.

9. Status final

SOLUCIONADO

========================================================================================

IT-2003 - Pagamento do cliente - 902.333.333-03
1. Onde consulto primeiro
   
Sistema interno → contrato 90003001 / CPF 902.333.333-03 → aba staus das parcelas, numero_ parcela , valor, status pagamento.

2. O que busco
   
Status da Parcela, se continua em aberto ou não.

3. O que encontrei
   
CSV: installment_ref=parcela_5, installment_status=aberta, installment_amount_brl=380,00, 
status credito = quitado parcial, id pagamento =banco_pay_r2_d01;banco_pay_r2_d02, status pagamento =pago

4. Hipótese
   
Serviço ou job de liquidação não vinculou o pagamento à parcela 5. Além disso, houve pagamento em duplicidade pelo cliente para o mesmo vencimento.

5. Retry/reprocesso
    
Executar rotina/job de conciliação manual do Pix para dar baixa na parcela 5.

6. Correção manual
    
Solicitar ao time Financeiro/Tesouraria o estorno (devolução) do segundo Pix de R$ 380,00 para a conta de origem do cliente por ter sido pago em duplicidade.

7. Escalação
    
Escalar para o time Financeiro/Tesouraria com os dois comprovantes para operacionalizar a devolução do valor excedente (R$ 380,00).

8. Comunicação
    
@agente.cx03 Baixa da parcela 5 realizada com sucesso a partir do primeiro Pix. Como houve pagamento em duplicidade, o segundo valor de R$ 380,00 foi encaminhado ao 
Financeiro para estorno na conta do cliente. A parcela consta como quitada e as cobranças foram suspensas.

9. Status final
    
SOLUCIONADO
=========================================================================================
IT-2009 - Valor divergente de pagamento

1. Onde consulto primeiro
Sistema interno → contrato 90009001 / CPF 902.999.999-09 → aba staus das parcelas, numero_ parcela , valor, status pagamento.

2. O que busco
Status da Parcela, se continua em aberto ou não.

3. O que encontrei
CSV: installment_ref=parcela_3, installment_status=aberta, installment_amount_brl=403,06, 
status credito = quitado parcial, id pagamento =banco_pay_r2_i01, status pagamento =pago

4. Hipótese
Cliente efetuou o pagamento com um valor maior do que o devido na parcela, não vinculando 
o pagamento da parcela 3.

5. Retry/reprocesso
Executar rotina/job para dar baixa na parcela 3.

6. Correção manual
Solicitar ao time Financeiro/Tesouraria a devolução do valor pago a maior.
 
7. Escalação
Escalar para o time Financeiro/Tesouraria paraa devolução do valor excedente (R$ 46,94).

8. Comunicação
@agente.cx08 Baixa da parcela 3 realizada com sucesso. Como houve pagamento com um valor maior do que o devido, foi encaminhado ao financeiro para devolução do excedente para o cliente.

9. Status final
SOLUCIONADO


