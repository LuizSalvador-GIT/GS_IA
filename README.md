# Lia · ColetAr Boa Vereda

A Lia é uma assistente de descarte criada para a Global Solution 2026.2 da FIAP. Ela consulta uma base municipal simulada, cita os documentos usados na resposta e calcula o próximo horário de atendimento dos ecopontos.

1. Abra [o notebook](1_Notebook_GS2026_2.ipynb) no Google Colab.
2. Adicione o Secret `OPENROUTER_API_KEY` e habilite o acesso para o notebook.
3. Execute as células em ordem. Abra o link do Gradio exibido na seção 8.

A [base documental](2_base_documental) inclui o regulamento de descarte, o cadastro de ecopontos e o comunicado que alterou o atendimento. Para executar a avaliação RAGAS, preencha as respostas de referência na seção 7. A avaliação salva o progresso em `3_avaliacao_ragas.json`.

## Evidências

- [Resposta sobre descarte de óleo com fontes](evidencias/print_gradio_rag_oleo.png)
- [Cálculo local do próximo horário do CT02](evidencias/print_gradio_calculo_ct02.png)
- [Testes dos quatro guardrails](evidencias/print_secao_6_guardrails.png)

As capturas do Gradio registram os testes feitos antes da atualização visual da Lia.
