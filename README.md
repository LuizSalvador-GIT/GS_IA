# Lia

A Lia é uma assistente de descarte criada para a Global Solution 2026.2 da FIAP. Ela consulta uma base municipal simulada, cita os documentos usados na resposta e calcula o próximo horário de atendimento dos ecopontos.

1. Abra [o notebook](1_Notebook_GS2026_2.ipynb) no Google Colab.
2. Adicione o Secret `NVIDIA_API_KEY` e habilite o acesso para o notebook.
3. Execute as células em ordem. A seção 3 testa os modelos hospedados no NVIDIA NIM e seleciona o primeiro que responde em texto e aceita ferramentas. Abra o link do Gradio exibido na seção 8.

A [base documental](2_base_documental) inclui o regulamento de descarte, o cadastro de ecopontos e o comunicado que alterou o atendimento. Para repetir o RAGAS, preencha as respostas de referência na seção 7. A execução salva o progresso em `3_avaliacao_ragas_nvidia_auto.json`.

## Evidências

- [Resposta sobre descarte de óleo com fontes](evidencias/print_gradio_rag_oleo.png)
- [Cálculo local do próximo horário do CT02](evidencias/print_gradio_calculo_ct02.png)
- [Testes dos quatro guardrails](evidencias/print_secao_6_guardrails.png)

As capturas do Gradio registram os testes feitos antes da atualização visual da Lia.

## Demonstração e avaliação

[Vídeo de demonstração da Lia](https://youtu.be/SmxPXxjW8Cc)

A execução com `poolside/laguna-xs-2.1` no NVIDIA NIM avaliou oito perguntas, cada uma com quatro métricas válidas.

| Métrica | Média |
| --- | ---: |
| Fidelidade ao contexto | 0,969 |
| Relevância da resposta | 0,798 |
| Precisão do contexto | 0,625 |
| Cobertura do contexto | 1,000 |

O [JSON público do RAGAS](3_avaliacao_ragas.json) inclui as notas por pergunta e as médias. Na A2, o comunicado vigente apareceu em primeiro lugar, mas a resposta começou mencionando o horário antigo e só depois apresentou o vigente. A referência também trazia o horário antigo, o que limita a interpretação da nota.
