### **📊 Projeto de Análise de Dados:**

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

![produto](https://github.com/user-attachments/assets/143b7c66-ddfe-43e6-9c12-71de83cf8c1b)


	**Dados da Lojas:**

* **Loja (Tipo: Texto);**  
* **Cidade (Tipo: Texto);**  
* **Estado (Tipo: Texto);**

**Exemplos:**

![loja](https://github.com/user-attachments/assets/3389b9d1-2743-4991-9774-a01b2b28c65c)


	**Dados Vendedor:**

* **Vendedor 	(Tipo: Texto);**  
* **ID-Vendedor	(Tipo: Numerico);**  
* **Comissão	(Tipo: Numerico)**

**Exemplos:**

![vendedor](https://github.com/user-attachments/assets/c73cd410-2e4b-4049-840a-022e2ced9eaf)


	**Dados Venda:**

* **Data Venda (Tipo: Data);**  
* **ValorVenda (Tipo:Numerico);**  
* **Custo 	         (Tipo:Numerico)**

**Exemplos:**


![venda](https://github.com/user-attachments/assets/ebfb1ba1-44ad-4139-a6d9-e5388477fb94)

	

#### **3\. Preparação dos Dados (Data Preparation) 🛠️**

* **Limpeza e Transformação:** 

Os dados já vieram organizados e estruturados, não teve a necessidade de nenhuma limpeza.

**4\. Resultados Finais e Insights 💡**

**4.1 Nivel Inteligencia**

**Gráfico de Coluna**: Total de Vendas por Fabricantes

Neste gráfico, observamos a distribuição das vendas entre diferentes fabricantes. Destacam-se os seguintes pontos:

Lidera com impressionantes 93 mil reais em vendas na Brastemp. Essa performance robusta sugere uma demanda consistente por seus produtos. Para manter essa alta demanda e procura deve investir em::

* Inovação Contínua: Investir em novos modelos para atrair clientes.  
  * Marketing Direcionado: Segmentar campanhas para diferentes públicos   


 No extremo oposto temos a Electrolux registrando modestos 7 mil reais em vendas. Aqui estão algumas estratégias para impulsionar suas vendas:  
  * Feedback dos Clientes: Realizar pesquisas para entender as percepções dos clientes sobre a marca e seus produtos.  
  * Estratégias Promocionais: Oferecer descontos, bundles ou brindes para atrair mais o público.  
 

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
  


#### 

#### 

#### **5\. Conclusão 📎**
