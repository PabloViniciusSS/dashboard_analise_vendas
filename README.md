### **📊 Projeto para Análise de Dados:**

#### **1\. Compreensão do Negócio (Business Understanding) 📈**

**Objetivo:**

Proporcionar uma visão detalhada das vendas de uma empresa fictícia, criando dashboards que permitam analisar dados e desenvolver estratégias mais eficazes. Essa análise beneficiará gestores, colaboradores e clientes.

**Alinhamento com as Metas de Negócio:** 

* **Gestores**: A análise detalhada dos colaboradores permitirá avaliar o desempenho em relação às metas estabelecidas. Compreender os valores alcançados por cada vendedor durante as vendas e se eles atingiram as metas é fundamental para tomar decisões informadas.  
    
* **Colaboradores**: Os vendedores poderão acompanhar seu próprio desempenho, identificando áreas de melhoria e oportunidades. Isso também incentivará a competição saudável entre os membros da equipe.  
    
* **Clientes**: Analisar quais produtos são mais vendidos, segmentando por categoria e região (estado, cidade), permitirá entender as preferências dos clientes e adaptar estratégias de marketing e estoque.

#### **2\. Compreensão dos Dados (Data Understanding) 🧐**

* **Fonte dos Dados:** Foi recebido um arquivo csv, com uma única planilha chamada vendas, ela foi carregada diretamente no Power BI.  
    
* **Grupos de Dados:**

**A fonte de dados segue uma estrutura que divide da seguinte forma:**

**Dados dos Produtos:**	

* **ID-Produto  (Tipo: Texto);**  
* **Produto       (Tipo: Texto);**  
* **Categoria    (Tipo: Texto);**  
* **Segmento   (Tipo: Texto);**  
* **Fabricante  (Tipo: Texto);**

**Exemplo:**
	
![produto](https://github.com/user-attachments/assets/ef92e5ce-6deb-4b7b-a677-1c7430d44ac7)


**Dados da Lojas:**

* **Loja (Tipo: Texto);**  
* **Cidade (Tipo: Texto);**  
* **Estado (Tipo: Texto);**

**Exemplos:**

![loja](https://github.com/user-attachments/assets/c4b12359-6403-48ca-9aad-df2e50fe4fb7)


**Dados Vendedor:**

* **Vendedor 	(Tipo: Texto);**  
* **ID-Vendedor	(Tipo: Numerico);**  
* **Comissão	(Tipo: Numerico)**

**Exemplos:**

![vendedor](https://github.com/user-attachments/assets/678e1bd7-7f3d-445a-97a7-3641f1c2ec03)


**Dados Venda:**

* **Data Venda (Tipo: Data);**  
* **ValorVenda (Tipo:Numerico);**  
* **Custo 	         (Tipo:Numerico)**

**Exemplos:**

![venda](https://github.com/user-attachments/assets/a1ad3210-fadf-4302-ae86-9354eef46075)


#### **3\. Preparação dos Dados (Data Preparation) 🛠️**

* **Limpeza e Transformação:** 


A preparação dos dados é um passo crucial para obter insights significativos. Vamos aprofundar os detalhes:

1. **Limpeza e Transformação:**

   * Felizmente, os dados já chegaram organizados e estruturados, o que economizou tempo.  
       
   * Realizamos uma transformação nas tabelas **ValorVenda** e **Custo**, convertendo os valores para o formato de moeda. Isso torna a análise mais coerente e legível.  

     **Exemplo:**
     
    	 ![valorVenda_Custo](https://github.com/user-attachments/assets/a262ffd5-d7ad-413d-b427-f4b9c4134ff5)

     
1. **Tabela Valor Comissão:**

   * Criamos uma nova tabela chamada **Valor Comissão** para comparar os valores recebidos pelos colaboradores.  
   * O cálculo utilizado foi:  
       
     		* Valor Comissão=Vendas\[ValorVenda\]×(100Vendas\[Comissão (Percentual)\]​)

**Exemplos**:  

 	![Comissao](https://github.com/user-attachments/assets/c2c9e0f9-7fe1-4b43-87ac-91c34f2d503e)
  

* Por exemplo, se uma venda teve um valor de R$ 1.000 e a comissão era de 5%, a comissão seria R$ 50\.  
1. **Valor Líquido:**

   * Calculamos o **Valor Líquido** para entender o ganho real da empresa por cada venda.
     
   * A fórmula utilizada foi:  

     		 * Valor Líquido=Vendas\[ValorVenda\]−Vendas\[Custo\]−Vendas\[Valor Comissão\]

   **Exemplos:**  

	![Valor Liquido](https://github.com/user-attachments/assets/0e5126cd-61b2-4c2c-9a49-8d88a4251bbd)


   * Por exemplo, se uma venda teve um valor de R$ 1.000, custo de R$ 200 e comissão de R$ 50, o valor líquido seria R$ 750\.

**4\. Resultados Finais e Insights 💡**

**4.1 Desempenho Financeiro de Vendas**

Como analista de negócios, tenho a capacidade de compreender profundamente os dados e traduzi-los em insights estratégicos. Neste relatório, exploraremos três aspectos essenciais das vendas, bem como ferramentas visuais para uma compreensão mais clara.  
	
 **Cards:**
1. Valor Líquido das Vendas:  
   * Vamos calcular o valor líquido das vendas, ou seja, o montante que efetivamente ficou com a empresa após descontos, impostos e outras deduções.  
   * Esse indicador é crucial para avaliar a saúde financeira da organização.  
1. Valor Bruto das Vendas:  
   * Analisaremos o valor bruto obtido pelas vendas, antes de qualquer dedução.  
   * Esse número reflete o potencial de receita da empresa e sua capacidade de gerar negócios.  
1. Total de Produtos Vendidos:  
   * Quantos produtos foram vendidos durante o período analisado?  
   * Essa métrica nos ajuda a entender a demanda e a eficácia das estratégias de vendas.

* **Gráfico de Cascata:**  
  * O gráfico de cascata nos mostrará as flutuações nas vendas ao longo dos anos.  
  * Notaremos que em 2015, houve um pico significativo de vendas, atingindo 165 mil reais. Comparativamente, o ano de 2012 registrou o menor número de vendas, com 37 mil reais.  
* **Tabela Matriz:** 
  * Essa tabela apresentará informações detalhadas, incluindo segmento, categoria, fabricante, produto e os valores de venda, custo e valor líquido.  
  * Analisaremos os custos em relação aos valores de vendas para identificar oportunidades de otimização e maximização do retorno.

Em resumo, este relatório não apenas justifica o esforço de desenvolvimento, mas também oferece insights valiosos para a tomada de decisões estratégicas. Afinal, compreender os números é o primeiro passo para impulsionar o sucesso da empresa

**4.2 Nivel Inteligencia**

**Gráfico de Coluna**: Total de Vendas por Fabricantes  
Neste gráfico, observamos a distribuição das vendas entre diferentes fabricantes. Destacam-se os seguintes pontos:

Lidera com impressionantes 93 mil reais em vendas na Brastemp. Essa performance robusta sugere uma demanda consistente por seus produtos. Para manter essa alta demanda e procura deve investir em::

* Inovação Contínua: Investir em novos modelos para atrair clientes.  
  * Marketing Direcionado: Segmentar campanhas para diferentes públicos   
    .

  Electrolux: No extremo oposto, a Electrolux registra modestos 7 mil reais em vendas. Aqui estão algumas estratégias para impulsionar suas vendas:  
  * Feedback dos Clientes: Realizar pesquisas para entender as percepções dos clientes sobre a marca e seus produtos.  
  * Estratégias Promocionais: Oferecer descontos, bundles ou brindes para atrair mais o público.  
    .

**Gráfico de Pizza:** Total de Vendas por Segmento

Utilizando o gráfico de pizza, observamos a proporção de vendas em diferentes segmentos. Destacam-se os seguintes pontos:  
Segmento Doméstico:

* Representa impressionantes 71,47% das vendas totais. Isso sugere uma forte demanda por produtos voltados para uso residencial. A preferência dos consumidores por produtos para uso doméstico é evidente, e investir em inovações nesse segmento pode ser estratégico.

  Segmento Industrial:

  * Apesar de modestos 3,49% das vendas, há oportunidades para crescimento.  
  * Para alavancar esse crescimento pode:  
    * Diversificar os produtos a partir das necessidades do segmento industrial.  
    * Parcerias estratégicas com outras empresas do setor podem abrir novos canais de vendas e aumentar a visibilidade da marca.  
    * O marketing segmentado, direcionado especificamente ao público industrial, pode atrair mais negócios.

    

**Gráfico de Funil:** Total de Vendas por Categoria

Com vendas robustas de 193,32 mil reais, os eletrodomésticos são o destaque. No entanto, os eletroportáteis, com apenas 19,06 mil reais, têm espaço para crescimento. Aqui estão algumas estratégias para alavancar esse segmento:

Diversificação de Produtos:

* Introduza novos eletroportáteis ou amplie a variedade existente. Itens como liquidificadores, cafeteiras e aspiradores podem atrair diferentes públicos.

  Campanhas Promocionais:

  * Ofereça descontos específicos para eletroportáteis. Promoções sazonais ou bundles (combinações de produtos) podem estimular as vendas.

  Estratégias de Marketing:

  * Destaque os benefícios dos eletroportáteis, como portabilidade, economia de espaço e praticidade.  
  * Explore canais de marketing direcionados, como redes sociais e e-mail marketing.

  Pesquisa Profunda:

  * Identifique os eletroportáteis mais vendidos e investigue por que alguns não estão saindo bem.  
  * Avalie o feedback de clientes e considere ajustes nos produtos ou na comunicação.  
    

	**4.3 Principais Influenciadores de Vendas**

O painel de **Principais Influenciadores** no Power BI é uma ferramenta poderosa para entender os fatores que impactam o valor total de vendas. Vamos mergulhar nos detalhes:

1. Segmentos e Categorias:  
   * Aumento do Valor de Vendas:  
     * O segmento Corporativo é o principal influenciador para aumentar o valor total de vendas.  
     * Na categoria de produtos, os celulares também têm um impacto positivo significativo.  
   * Diminuição do Valor de Vendas:  
     * Quando se trata de diminuir o valor de vendas, o segmento Doméstico é o fator crítico.  
     * Além disso, a categoria de eletroportáteis também contribui para essa diminuição.  
1. Estratégias e Ações:  
   * Corporativo:  
     * Investir mais no segmento corporativo é essencial. Isso pode envolver estratégias de marketing direcionadas e uma equipe de vendas focada nesse público.  
   * Celulares:  
     * Aumentar as vendas de celulares é uma oportunidade. Avalie campanhas específicas para essa categoria.  
   * Doméstico e Eletroportáteis:  
     * Monitore o segmento doméstico para evitar perdas no valor de vendas.  
     * Cuide dos produtos de eletroportáteis para otimizar o desempenho

	**4.4 Faixas de Vendas Por Categoria e Pontos de Vendas**  
	  
	**Gráfico de Faixa:**

* O gráfico de faixas é uma ferramenta visual que nos permite comparar categorias (neste caso, lojas) com base em uma métrica (vendas).  
  * Cada faixa representa uma loja, e sua cor indica o desempenho de vendas.  
    

Identificando Tendências:

* Seguindo as faixas, podemos ver quais lojas estão se destacando e quais precisam de atenção.  
  * As lojas com vendas mais altas terão faixas mais largas e cores mais intensas.  
  * As lojas com vendas mais baixas terão faixas estreitas e cores mais suaves.  
    

Estratégias de Melhoria:

* Lojas com bom desempenho:  
  * Analise o que está funcionando bem nessas lojas.  
    * Compartilhe as melhores práticas com outras lojas.  
  * Lojas com desempenho inferior:  
    * Identifique os obstáculos (por exemplo, localização, estoque, equipe).  
    * Crie estratégias específicas para impulsionar as vendas nessas lojas.

	**4.5 Performance de Vendedores por Regiões**

Este relatório oferece insights valiosos sobre o desempenho dos vendedores em cada estado. Vamos detalhar:

1. Indicadores de Desempenho:  
   * O objetivo é fornecer aos gestores informações claras e concisas sobre como os vendedores estão se saindo.  
   * Os indicadores incluem métrica de vendas totais de cada um, por estado  
1. Análise por Estado:  
   * Para cada estado, avaliamos:  
     * As vendas totais realizadas pelos vendedores.  
1. Estratégias Personalizadas:  
   * Com base nos dados, os gestores podem:  
     * Identificar os vendedores de alto desempenho e reconhecê-los.  
     * Oferecer treinamento específico para melhorar o desempenho dos vendedores com resultados abaixo da média.  
     * Criar estratégias personalizadas para cada estado, considerando suas particularidades.

#### 

#### **5\. Conclusão 📎**
