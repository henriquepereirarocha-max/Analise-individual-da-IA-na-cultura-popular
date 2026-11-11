# Auditoria Técnica de IA e Ciência de Dados: Análise de Impacto Ético e Preditivo

## Contexto e Problema Investigado
Este projeto consiste em uma auditoria técnica e ética das tecnologias de Inteligência Artificial e análise de dados retratadas nas obras *Black Mirror* e no documentário *O Dilema das Redes*. O objetivo é avaliar os limites de privacidade, governança de dados, engenharia de prompts, métricas preditivas de regressão e falhas de generalização em cenários de alta complexidade social.

## Dados Analisados e Tratamento
- **Origem dos Dados:** Vetores comportamentais simulados (tempo de tela, histórico de interações) e registros de frequências de áudio/biometria.
- **Pré-processamento:** 
  - Remoção de colunas com dados sensíveis e PII através da função `df.drop(columns=[...])` da biblioteca Pandas.
  - Escalonamento de atributos contínuos via Normalização Min-Max (`fit_transform`), garantindo amplitude uniforme [0.0, 1.0].

## Solução Preditiva e Guardrails de Segurança
- **Ciência de Dados:** Implementação e avaliação de modelos preditivos com análise estrita do Coeficiente de Determinação ($R^2$) e do Erro Quadrático Médio ($RMSE$), prevenindo vieses e superajustes (*overfitting*).
- **Técnicas Integradas em IA:** Estruturação de Prompts do Sistema enriquecidos com *base_contexto* e *guardrails* rígidos para prevenção de violações de privacidade e uso indevido de imagem.

## Impacto Ético e Governança
- **Versionamento de Código:** Adoção do Git e GitHub como mecanismos auditáveis de histórico de modificações (*commits*), assegurando a rastreabilidade e a governança contínua do software.
- **Privacidade por Design:** Aplicação de diretrizes de anonimização restritivas antes da fase de treinamento dos modelos generativos e preditivos.

## Próximos Passos
1. Expandir a bateria de testes automatizados com novos cenários de borda (*edge cases*).
2. Refinar a margem de erro do modelo de classificação de voz sintética.
3. Incorporar testes contínuos de usabilidade com intervenção humana (*Human-in-the-Loop*).
