# Lia · ColetAr Boa Vereda

A Lia é uma assistente de descarte criada para a Global Solution 2026.2 da FIAP. Ela consulta uma base municipal simulada, cita os documentos usados na resposta e calcula o próximo horário de atendimento dos ecopontos.

1. Abra [o notebook](1_Notebook_GS2026_2.ipynb) no Google Colab.
2. Adicione o Secret `OPENROUTER_API_KEY` e habilite o acesso para o notebook.
3. Execute as células em ordem. Abra o link do Gradio exibido na seção 8.

A [base documental](2_base_documental) inclui o regulamento de descarte, o cadastro de ecopontos e o comunicado que alterou o atendimento. Para executar a avaliação RAGAS, preencha as respostas de referência na seção 7. A avaliação salva o progresso em `3_avaliacao_ragas.json`.
