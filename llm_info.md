# Uso de Ferramenta LLM no Auxílio da Tarefa

Arquivo que descreve o uso de uma ferramenta de LLM para auxílio na execução da tarefa.

A ferramenta de LLM usada para auxiliar no desenvolvimento da atividade foi o **ChatGPT 4.0**.

## Construção do Arquivo CSV

Para construção do arquivo CSV, foi pedido para que o modelo de linguagem listasse 50 comidas típicas do Brasil, utilizando um prompt simples:

> "Pode listar 50 receitas de comidas típicas do Brasil?"

Com a lista de 50 receitas, foram buscadas imagens para auxiliar no reconhecimento dos ingredientes com um segundo prompt, também simples:

> "Pode descrever os ingredientes desse prato?"

Com os ingredientes listados, mais um prompt foi elaborado para criação do arquivo CSV:

> "Agora gostaria que me ajudasse na elaboração de um arquivo csv com os dados das 50 comidas. Preciso de 3 colunas (nome_receita, ingredientes e tipos_ingredientes), a coluna de ingredientes deve incluir os principais ingredientes e a coluna de tipos deve classificar os ingredientes em proteína, carboidrato, vegetal, fruta, laticínio, gordura, condimento e outro."

## Criação do Código para Geração do Grafo

Após isso, um prompt mais refinado foi utilizado na criação do código que iria criar o grafo e extrair as informações desejadas:

> "Tenho um arquivo .csv com 50 comidas típicas do Brasil, organizadas em 3 colunas (nome_receita, ingredientes e tipos_ingredientes). Preciso processar esses dados da seguinte forma: Gere um código em Python que lê as informações do arquivo .csv e cria um grafo da seguinte forma: Os nós serão os ingredientes, as arestas serão a ligação entre ingredientes que aparecem na mesma receita e o atributo dos nós será o tipo de ingrediente. O código também deve calcular o coeficiente de assortatividade por tipo usando networkx.attribute_assortativity_coefficient(G, "tipo") e criar uma visualização do grafo com layout adequado e coloração por tipo (nxviz), o formato do grafo pode ser o CircosPlot. No grafo também gostaria de uma legenda para cada tipo de nó, com cores que correspondem às cores do grafo plotado. Posicione a legenda de forma que ela não fique na frente do grafo. Também devem ser impressas informações importantes, como os ingredientes mais comuns, quantidade de ingredientes de cada tipo e a assortatividade."

O código criado ainda apresentava alguns pequenos erros, que foram corrigidos posteriormente, durante as execuções.
