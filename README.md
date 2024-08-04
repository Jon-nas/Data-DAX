# Projeto de modelagem e transformação de dados com DAX no Power BI.

Construção do projeto:

    1 - Coleta de Dados: Utilização da tabela Financial Sample para criar as tabelas dimensão e fato do modelo baseado em star schema;
    2 - Modelagem de Dados: Estruturar os dados em um modelo relacional, criando tabelas e definindo relacionamentos entre elas;
    3 - Transformação de Dados: Limpar e transformar os dados usando o Power Query para garantir que estejam prontos para análise;
    4 - Criação de Medidas e Colunas Calculadas: Utilizar DAX para criar medidas e colunas que ajudam a realizar cálculos complexos e análises avançadas.
   
O processo consiste na criação das tabelas com base na tabela original. A partir da cópia serão selecionadas as colunas que irão compor a visão das novas tabelas.  
Sendo assim, a partir da tabela principal - Financials_origem (modo oculto – backup) serão criadas as tabelas:
Esquema em estrela com o foco na análise dos dados de E-commerce:

    . D_Produtos (ID_produto, Produto, Média de Unidades Vendidas, Médias do valor de vendas, Mediana do valor de vendas, Valor máximo de Venda, Valor mínimo de Venda);
    . D_Produtos_Detalhes(ID_produtos, Discount Band, Sale Price, Units Sold, Manufactoring Price);
    . D_Descontos (ID_produto, Discount, Discount Band);
    . D_Detalhes (*);
    . D_Calendário – Criada por DAX com calendar();
    . F_Vendas (SK_ID , ID_Produto, Produto, Units Sold, Sales Price, Discount Band, Segment, Country, Sales, Profit, Date (campos)).


Ferramentas utilizadas:

    . Power BI
   
