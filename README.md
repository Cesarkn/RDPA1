1. Carregamento e Preparação dos Dados:
		O dataset "Wine" (Vinhos) é carregado. Ele contém 178 amostras de vinhos, cada uma com 13 características químicas (como álcool, acidez, cor, etc.).
		Ponto Crítico: Os dados são padronizados usando StandardScaler. Isso é fundamental porque o PCA (próxima etapa) é muito sensível a diferenças de escala entre as variáveis. A padronização garante que todas as características tenham a mesma importância inicial.

2. Redução de Dimensionalidade com PCA:
		O PCA (Análise de Componentes Principais) é aplicado para reduzir as 13 características originais para apenas 2 "componentes principais".
		Esses dois componentes são novas variáveis que, juntas, capturam a maior parte da informação e da variação dos dados originais. O código mostra que esses 2 componentes conseguem explicar cerca de 55.41% da variância total, simplificando enormemente o problema.

3. Clusterização com K-Means:
		O algoritmo K-Means é aplicado sobre os dados já reduzidos pelo PCA (os 2 componentes principais).
		O objetivo do K-Means é agrupar os vinhos em 3 clusters distintos (o número 3 foi escolhido porque já se sabe que o dataset contém 3 classes de vinho). O algoritmo encontra os centros (centroides) de cada grupo e atribui cada vinho ao grupo mais próximo.

4. Visualização e Comparação:
	O código gera dois gráficos de dispersão lado a lado:

	Gráfico da Esquerda: Mostra os 3 clusters que o K-Means encontrou por conta própria, colorindo cada ponto (vinho) de acordo com o grupo atribuído. Os centroides de cada cluster são marcados com um "X" vermelho.
	Gráfico da Direita: Mostra os mesmos pontos, mas coloridos de acordo com a classe real (verdadeira) de cada vinho. Este gráfico serve como uma "resposta" para validar visualmente o quão bem o K-Means se saiu.
