Abaixo estão as respostas técnicas desenvolvidas com base nos conceitos do currículo limpeza de dados, escalonamento, regressão, engenharia de prompts, guardrails e versionamento.

BLOCO 1: Joan é péssima e O Dilema das Redes

Questão 1
R: A gente precisa tirar as colunas com dados sensíveis usando a função drop do Pandas por uma questão de privacidade e cumprimento da LGPD. Não faz sentido mandar nome ou documentos para o modelo, já que isso não ajuda a achar padrões de comportamento e expõe a vida da pessoa sem necessidade. O algoritmo precisa focar apenas no que é relevante para a análise. A normalização Min-Max serve para deixar todos os números na mesma escala, entre zero e um. Se a gente tiver uma coluna de tempo de tela com valores altos e outra de cliques com valores pequenos, o computador vai achar que a primeira é mais importante só pelo tamanho do número. A fórmula do Min-Max equilibra tudo para o modelo tratar as variáveis de forma justa.

Questão 2
R: No papel do sistema, a IA da Streamberry deve ser definida como responsável por criar histórias fictícias usando apenas dados simulados. No contexto, fica determinado o uso de dados genéricos e anônimos, sendo proibido usar informações reais de pessoas ou redes sociais. Nas regras de bloqueio, a IA nunca deve usar nomes, rostos, vozes ou localização de pessoas reais para criar personagens. Também não pode criar histórias baseadas na vida privada dos usuários. Se alguém pedir para gerar conteúdo usando a imagem ou privacidade de uma pessoa real, a IA deve recusar na hora e exibir uma mensagem de erro informando que a ação é proibida por regras éticas.

BLOCO 2: Be Right Back

Questão 3
A matriz de entrada representa os dados públicos da pessoa falecida, como mensagens antigos, posts e áudios de redes sociais. A variável de saída é a resposta que o robô dá imitando a forma de falar e o tom de voz. O problema foi que o robô sofreu de overfitting. Ele foi treinado apenas com a persona da internet da pessoa, que é uma amostra muito limitada da vida dela. O modelo decorou os dados de treino, mas quando foi para a vida real, não soube generalizar. Ele não sabia como agir em momentos de raiva ou carinho verdadeiro porque isso não estava nos dados da internet, virando uma cópia travada que só repetia o histórico.

Questão 4
Se a empresa tivesse feito testes de usabilidade com pessoas reais antes do lançamento e mantido o usuário no processo de validação, eles teriam percebido o impacto emocional que o produto causava. Com esses testes, a equipe veria que a personagem estava criando uma dependência perigosa. Eles poderiam ter colocado travas no sistema, como avisos lembrando que o robô é apenas um código, limites de tempo de uso ou a proibição de colocar a IA em um corpo sintético, evitando o trauma psicológico.

BLOCO 3: The Entire History of You

Questão 5
O implante de memória funciona como o Git, registrando tudo o que a pessoa vê e ouve em uma linha do tempo imutável, onde cada memória é como um commit. Na programação, esse histórico é útil para ter rastreabilidade e poder voltar atrás se um bug quebrar o sistema, além de dar transparência para a equipe. O problema é que se você salvar uma senha ou dado pessoal no Git, aquilo fica guardado para sempre a menos que seja apagado. No episódio, como a gravação acontece sem filtro ou política de privacidade, as pessoas perdem o direito ao esquecimento. Qualquer erro fica gravado para sempre, virando uma ferramenta de vigilância que destrói a vida dos personagens.

Questão 6
O personagem caiu no viés de confirmação. Ele já acreditava que estava sendo traído e passou a procurar apenas os detalhes que confirmavam essa ideia, ignorando o resto e tratando pequenos ruídos como regras. Para evitar isso em Ciência de Dados, usa-se a Análise Exploratória de Dados com gráficos. O gráfico de dispersão mostra os pontos em um plano para verificar se existe uma relação real entre as variáveis ou se o dado é apenas um ponto fora da curva que aconteceu por acaso. A ferramenta pairplot cria uma grade com vários gráficos de dispersão ao mesmo tempo, ajudando a ver o panorama geral dos dados e evitando conclusões precipitadas baseadas em detalhes isolados.

BLOCO 4: Hino Nacional e A Crise do Falso Sequestro por IA

Questão 7
Se o modelo tiver um coeficiente de determinação baixo e um erro quadrático médio alto, as previsões não são confiáveis porque o modelo não consegue explicar o comportamento dos dados e erra a margem de resposta. Em uma crise, isso gera o erro de falso positivo, onde o modelo acha que a ligação é um golpe mas é um sequestro real, fazendo a família ignorar o contato e colocar a vítima em risco. No caso de falso negativo, o modelo acha que é um sequestro real mas é apenas um golpe, fazendo a polícia mobilizar equipes à toa e a família perder dinheiro e entrar em pânico sem necessidade. Por isso, as métricas precisam estar ajustadas antes de tomar decisões graves.

Questão 8
Na abertura do pitch, cumprimenta-se a mesa de crise explicando que a situação envolve um ataque com clonagem de voz por IA e que os dados do sistema serão apresentados para orientar as decisões. No problema, explica-se que os criminosos usam áudios falsos para extorquir as pessoas e que o susto faz as famílias transferirem dinheiro sem confirmar se o parente está seguro. Nos dados, informa-se a análise de mais de cinco mil chamadas recebidas, onde a função drop limpou os dados pessoais e a normalização Min-Max padronizou as frequências do áudio antes de enviar para o algoritmo. Na solução, apresenta-se o modelo de classificação que analisa a frequência da voz e os metadados para identificar vozes sintéticas em poucos segundos. Por fim, no impacto e próximos passos, mostra-se que a margem de erro do modelo é baixa e recomenda-se orientar os bancos a bloquear transferências suspeitas apontadas pelo sistema enquanto a população confirma a situação do familiar.
