### **📊 Projeto de Análise de Dados:**

#### **1\. Compreensão do Negócio (Business Understanding) 📈**

**Objetivo:**

Proporcionar uma visão detalhada das vendas de uma empresa fictícia, criando dashboards que permitam analisar dados e desenvolver estratégias mais eficazes. Essa análise beneficiará gestores, colaboradores e clientes.

**Alinhamento com as Metas de Negócio:** 

* **Gestores**: A análise detalhada dos colaboradores permitirá avaliar o desempenho em relação às metas estabelecidas. Compreender os valores alcançados por cada vendedor durante as vendas e se eles atingiram as metas é fundamental para tomar decisões informadas.  
    
* **Colaboradores**: Os vendedores poderão acompanhar seu próprio desempenho, identificando áreas de melhoria e oportunidades. Isso também incentivará a competição saudável entre os membros da equipe.  
    
* **Clientes**: Analisar quais produtos são mais vendidos, segmentando por categoria e região (estado, cidade), permitirá entender as preferências dos clientes e adaptar estratégias de marketing e estoque.

#### **2\. Compreensão dos Dados (Data Understanding) 🧐**

* **Fonte dos Dados:** Foi recebido um arquivo csv, com uma única planilha chamada “vendas”, ela foi carregada diretamente no Power BI.  
    
* **Grupos de Dados:**

**A fonte de dados segue uma estrutura que divide da seguinte forma:**

**Dados dos Produtos:**	

* **ID-Produto  (Tipo: Texto);**  
* **Produto       (Tipo: Texto);**  
* **Categoria    (Tipo: Texto);**  
* **Segmento   (Tipo: Texto);**  
* **Fabricante  (Tipo: Texto);**

**Exemplo:**

![produto](https://github.com/user-attachments/assets/7a39ec9f-0766-4002-a9eb-642909d0176a)


**Dados da Lojas:**

* **Loja (Tipo: Texto);**  
* **Cidade (Tipo: Texto);**  
* **Estado (Tipo: Texto);**

**Exemplos:**

![loja](https://github.com/user-attachments/assets/850ec2b3-518d-4567-92a6-b15c7a67ad79)


**Dados Vendedor:**

* **Vendedor 	(Tipo: Texto);**  
* **ID-Vendedor	(Tipo: Numerico);**  
* **Comissão	(Tipo: Numerico)**

**Exemplos:**

![vendedor](https://github.com/user-attachments/assets/399e9ed0-761d-474f-af40-d6fbe7ab89a2)


**Dados Venda:**

* **Data Venda (Tipo: Data);**  
* **ValorVenda (Tipo:Numerico);**  
* **Custo      (Tipo:Numerico)**

**Exemplos:**


![venda](https://github.com/user-attachments/assets/7d737c86-d9d7-4502-8471-c633d0cb5684)

	

#### **3\. Preparação dos Dados (Data Preparation) 🛠️**

* **Limpeza e Transformação:** 

* Felizmente, os dados já chegaram organizados e estruturados, o que economizou tempo.  
      
* Foi realizado uma transformação nas colunas **ValorVenda** e **Custo**, convertendo os valores para o formato de moeda. Isso torna a análise mais coerente e legível.  
    **Exemplo:**  

   ![image](https://github.com/user-attachments/assets/e688f384-ea00-4fc4-af5b-abf1d3b14dbc)


  **3.1. Tabela Valor Comissão:**

  * Houve a criação de uma nova coluna chamada **Valor Comissão** para saber quanto os colaboradores receberam por cada venda, através da porcentagem da comissão e do valor do produto  
      
  * O cálculo utilizado foi:  
      
    * Valor Comissão=Vendas\[ValorVenda\]×(Vendas\[Comissão (Percentual) / 100\]​)  
      

**Exemplos**:  

 ![image](https://github.com/user-attachments/assets/316dbfe6-c8e4-4144-9401-79a2bc77cb84)


* Por exemplo, se uma venda tivesse um valor de R$ 1.000 e a comissão era de 5%, a comissão seria R$ 50\.


  **3.2 Valor Líquido:**

  * Também foi criado e calculado o **Valor Líquido** para entender o ganho real da empresa por cada venda, a tabela ganho o mesmo nome.  
      
  * A fórmula utilizada foi:  
      
    * Valor Líquido=Vendas\[ValorVenda\] − Vendas\[Custo\] − Vendas\[Valor Comissão\]  
      

  **Exemplos:**

![image](https://github.com/user-attachments/assets/60db799d-9fea-4c8c-97c7-f58402bc547a)

      		
  * Por exemplo, se uma venda tivesse um valor de R$ 1.000, custo de R$ 200 e comissão de R$ 50, o valor líquido seria R$ 750\.

### **4\. Funcionalidades do Power BI Utilizadas e Aplicações 🔧**

Para a transformação e os cálculos que foram mostrados anteriormente foi utilizado:

Power Query Editor: Utilizado para carregar e transformar os dados iniciais, e transformando algumas colunas para ajudar na análise dos dados. Por exemplo: a transformação das tabelas em Tipo Moeda.

Não foi necessário utilizar a modelagem de dados que está presente no Power BI, pois, só consta uma tabela.

Dax(Data Analysis Expressions): Foi utilizado para criar os cálculos das colunas “Valor Comissão” e “Valor Líquido”.

No Power BI foi utilizado para visualização dos dados os Cards, Gráfico de Cascata, Tabelas Matriz, Gráfico de Coluna, Pizza, Funil, Faixa e o Painel de Principais Influenciadores.

#### *5\. Resultados Finais e Insights 💡*

**5.1\. Desempenho Financeiro de Vendas**

![desempenho de vendas](https://github.com/user-attachments/assets/a1fd8274-acdc-409f-a070-87f232468200)


Nesta página, foram explorados três aspectos essenciais das vendas, bem como ferramentas visuais para uma compreensão mais clara.

5.1.1 **Cards:**

  **Valor Líquido das Vendas:**  
    * Vamos calcular o valor líquido das vendas, ou seja, o montante que efetivamente ficou com a empresa.  
    * Esse indicador é crucial para avaliar a saúde financeira da organização.  
       
  **Valor Bruto das Vendas:**  
    * Analisando o valor bruto obtido pelas vendas, antes de qualquer dedução.  
    * Esse número reflete o potencial de receita da empresa e sua capacidade de gerar negócios.

  **Total de Produtos Vendidos:  
    * Quantos produtos foram vendidos durante o período analisado?  
    * Essa métrica ajuda a entender a demanda e a eficácia das estratégias de vendas.  
       
  **Gráfico de Cascata**:  
    
   * O gráfico de cascata nos mostrará as flutuações nas vendas ao longo dos anos.  
   * Nota-se que em 2015, houve um pico significativo de vendas, atingindo 165 mil reais. Comparativamente, o ano de 2012 registrou o menor número de vendas, com 37 mil reais.  
      
      
  **Tabela Matriz**:  
    
   * Essa tabela apresenta informações detalhadas, incluindo segmento, categoria, fabricante, produto e os valores de venda, custo e valor líquido.       
   * Analisou os custos em relação aos valores de vendas para identificar oportunidades de otimização e maximização do retorno.  
    

Em resumo, esta página não apenas justifica o esforço de desenvolvimento, mas também oferece insights valiosos para a tomada de decisões estratégicas. Afinal, compreender os números é o primeiro passo para impulsionar o sucesso da empresa.

**5.2 Narrativa Inteligencia**

![narrativa inteligente](https://github.com/user-attachments/assets/cf6216f7-9fda-4ed0-b683-b3426b9d379e)

**Gráfico de Coluna**:   
Total de Vendas por Fabricantes: observa a distribuição das vendas entre diferentes fabricantes.   
Destacando os seguintes pontos:

A Brastemp lidera com impressionantes 93 mil reais em vendas. Essa performance robusta sugere uma demanda consistente por seus produtos. Para manter essa alta demanda e procura deve investir em:
* Inovação Contínua: Investir em adquirir novos produtos e modelos para atrair clientes e ter mais variedade da marca.
  
No extremo oposto, a Electrolux registra modestos 7 mil reais em vendas. Aqui estão algumas estratégias para impulsionar suas vendas:  
* Feedback dos Clientes: Realizar pesquisas para entender as percepções dos clientes sobre a marca e seus produtos e assim tentar entender o que faz ter baixo volume de vendas.  
* Estratégias Promocionais: Oferecer descontos ou brindes para atrair mais vendas para essa marca.  

**Gráfico de Pizza:** 

Total de Vendas por Segmento: Utilizando o gráfico de pizza, foi investigado a proporção de vendas em diferentes segmentos. Destacam-se os seguintes pontos:

Segmento Doméstico:

* Representa impressionantes 71,47% das vendas totais. Isso sugere uma forte demanda por produtos voltados para uso residencial. A preferência dos consumidores por produtos para uso doméstico é evidente, e investir nesse segmento pode ser estratégico.

Segmento Industrial:
    
* Apesar de modestos 3,49% das vendas, há oportunidades para crescimento.
* Para alavancar esse crescimento pode:  
* Identificar possíveis necessidades dos clientes.  
* Diversificar os produtos a partir das necessidades da indústria.
  
**Gráfico de Funil:** 

Total de Vendas por Categoria: Com vendas robustas de 193,32 mil reais, os eletrodomésticos são o destaque. No entanto, os eletroportáteis, com apenas 19,06 mil reais, têm espaço para crescimento. Aqui estão algumas estratégias para alavancar esse segmento:

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
    

**5.3 Principais Influenciadores de Vendas**

![principais influciadores](https://github.com/user-attachments/assets/e2307ec1-dd93-40ee-8fc7-b8d101fe29cb)


O painel de **Principais Influenciadores** no Power BI é uma ferramenta poderosa para entender os fatores que impactam o valor total de vendas. Vamos ver os detalhes:

1. Segmentos e Categorias:  
     
   * Aumento do Valor de Vendas:  
     * O segmento Corporativo é o principal influenciador para aumentar o valor total de vendas.  
     * Na categoria de produtos, os celulares também têm um impacto positivo significativo.  
   * Diminuição do Valor de Vendas:  
     * Quando se trata de diminuir o valor de vendas, o segmento doméstico é o fator crítico.  
     * Além disso, a categoria de eletroportáteis também contribui para essa diminuição.  
         
2. Estratégias e Ações:  
     
   * Corporativo:  
     * Investir mais no segmento corporativo é essencial. Isso pode envolver estratégias de marketing direcionadas e uma equipe de vendas focada nesse público.  
   * Celulares:  
     * Aumentar as vendas de celulares é uma oportunidade. Avalie campanhas específicas para essa categoria.  
   * Doméstico e Eletroportáteis:  
     * Monitore o segmento doméstico para evitar perdas no valor de vendas.  
     * Cuide dos produtos de eletroportáteis para otimizar o desempenho

**5.4 Faixas de Vendas Por Categoria e Pontos de Vendas**  

![faixas de vendas](https://github.com/user-attachments/assets/c89d89fd-f583-41f7-b2b4-2519f5e861d2)

	  
**Gráfico de Faixa:**
* O gráfico de faixas é uma ferramenta visual que nos permite comparar categorias (neste caso, lojas) com base em uma métrica (vendas).  
* Cada faixa representa uma loja, e sua cor indica como estão as vendas de determinado segmento..  
    
Identificando Tendências:

* Seguindo as faixas, podemos ver quais lojas estão se destacando e quais precisam de atenção.  
  * As lojas com vendas mais altas terão faixas mais largas.  
  * As lojas com vendas mais baixas terão faixas estreitas.  
    

Estratégias de Melhoria:

* Lojas com bom desempenho:  
  * Analise o que está funcionando bem nessas lojas.  
    * Compartilhe as melhores práticas com outras lojas.  
  * Lojas com desempenho inferior:  
    * Identifique os obstáculos (por exemplo, localização, estoque, equipe).  
    * Crie estratégias específicas para impulsionar as vendas nessas lojas.

**5.5 Performance de Vendedores por Regiões**

![perfomace vendedor](https://github.com/user-attachments/assets/cdc3d807-6e20-4ae6-ad54-313a81fc00d8)


Este relatório oferece insights valiosos sobre o desempenho dos vendedores em cada estado. Vamos detalhar:

1. Indicadores de Desempenho:  
   * O objetivo é fornecer aos gestores informações claras e concisas sobre como os vendedores estão se saindo.  
   * Os indicadores incluem métrica de vendas totais de cada um, por estado.  
1. Análise por Estado:  
   * Para cada estado, avaliamos:  
     * As vendas totais realizadas pelos vendedores.  
1. Estratégias Personalizadas:  
   * Com base nos dados, os gestores podem:  
     * Identificar os vendedores de alto desempenho e reconhecê-los.  
     * Oferecer treinamento específico para melhorar o desempenho dos vendedores com resultados abaixo da média.  
     * Criar estratégias personalizadas para cada estado, considerando suas particularidades.

#### 

#### **6\. Conclusão 📎**

Este projeto foi desenvolvido com o objetivo de aprimorar minhas habilidades em análise de indicadores de desempenho de equipes de vendas. Ao longo do projeto, adquiri uma compreensão aprofundada sobre a saúde financeira da loja e o desempenho das vendas, permitindo segmentar e entender como diferentes produtos, marcas e segmentos impactam a empresa. Identifiquei áreas que necessitam de maior atenção e manutenção para sustentar o sucesso.

Com minha expertise em análise de dados, consegui identificar lojas que estão abaixo da média de vendas e analisar os indicadores de desempenho dos vendedores. Esse projeto oferece uma ferramenta valiosa para gestores, proporcionando insights detalhados sobre o desempenho das lojas e de seus vendedores em relação às metas estabelecidas.

Os vendedores também se beneficiam desta análise, podendo identificar pontos de melhoria e entender seu desempenho em relação aos objetivos da empresa. A análise detalhada dos dados revela oportunidades para aumentar as vendas de determinados produtos, ajudando os vendedores a focarem seus esforços de maneira mais eficaz.

Além disso, o projeto destaca pontos estratégicos que a equipe de marketing pode utilizar para impulsionar as vendas da empresa, demonstrando a importância de uma abordagem integrada entre vendas e marketing.

