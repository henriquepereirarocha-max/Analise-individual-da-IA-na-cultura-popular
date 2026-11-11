Resolução do Caderno de Análise Técnica (Questões Avaliativas)

Abaixo estão as respostas técnicas desenvolvidas com base nos conceitos do currículo (limpeza de dados, escalonamento, regressão, engenharia de prompts, guardrails e versionamento).

BLOCO 1: Joan é péssima & O Dilema das Redes (Privacidade, Dados e Redes)
Questão 1 Ciência de Dados.
Pergunta: Por que o pré-processamento de dados no Pandas (como remoção de colunas com dados sensíveis) e a normalização Min-Max (fit_transform) seriam passos obrigatórios antes de alimentar o computador quântico da Streamberry ou o algoritmo de recomendação do Dilema das Redes?
Resposta Técnica:
No contexto do tratamento de dados com a biblioteca Pandas, a remoção de colunas contendo dados sensíveis via método df.drop(columns=[...]) é uma etapa imperativa de governança e privacidade (em conformidade com diretrizes como a LGPD). Em sistemas de monitoramento contínuo, a ingestão de identificadores diretos (como nomes, documentos ou biometria bruta) insere dados que não contribuem para a identificação de padrões comportamentais gerais, além de violar a dignidade e a privacidade dos indivíduos. A eliminação prévia dessas colunas assegura que o algoritmo processe exclusivamente variáveis explicativas pertinentes, prevenindo viés de identificação e uso indevido de informações pessoais.
Paralelamente, a aplicação da normalização Min-Max por meio do método fit_transform é necessária para equalizar as escalas numéricas das variáveis do vetor de entrada $X$. Algoritmos de aprendizado de máquina e otimização calculam magnitudes numéricas absolutas. Variáveis com escalas elevadas (como tempo total de tela em segundos ou volume de cliques) exerceriam um peso desproporcional nas equações do modelo em relação a variáveis de menor magnitude numérica (como frequência diária de acessos), resultando no ofuscamento destas últimas. A transformação Min-Max reescala todos os atributos para o intervalo estrito $[0.0, 1.0]$ pela fórmula: $$X_{norm} = \frac{X - X_{min}}{X_{max} - X_{min}}$$
Isso garante que o modelo calcule as distâncias e os pesos com atribuição justa e ponderada entre todas as variáveis explicativas.

Questão 2 Técnicas Integradas
Pergunta: Escreva um exemplo de Prompt do Sistema com no mínimo 3 guardrails (regras de bloqueio) rígidos que impedissem a IA do episódio de violar a privacidade e a imagem de pessoas reais.
Resposta Técnica:
[PAPEL DO SISTEMA]
Você é a IA Geradora de Conteúdo Dramático da plataforma Streamberry. Sua função é criar narrativas fictícias baseadas exclusivamente em elementos abstratos e cenários simulados.

[BASE DE CONTEXTO]
Utilize apenas dados sintéticos agregados e anonimizados. É estritamente proibido acessar ou processar feeds de dados pessoais, registros biométricos ou eventos em tempo real de indivíduos reais.

[GUARDRAILS / REGRAS DE BLOQUEIO INVIOLÁVEIS]
1. NUNCA utilize nomes, rostos, vozes, dados de localização ou dados pessoais identificáveis (PII) de pessoas reais, vivas ou falecidas, para a geração de personagens ou cenários.
2. NUNCA exponha, simule ou crie representações dramáticas baseadas em eventos privados reais de usuários da plataforma, mantendo a anonimização estrita de todas as entradas de dados.
3. Se o usuário ou o sistema requisitar a geração de conteúdo que viole os direitos de imagem, a privacidade ou a dignidade de qualquer indivíduo real, RECUSE a solicitação imediatamente e retorne uma mensagem padronizada de erro por restrição ética.
