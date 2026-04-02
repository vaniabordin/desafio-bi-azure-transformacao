Desafio de Projeto: Processamento de Dados Simplificado com Power BI
📝 Descrição do Projeto
Este projeto consistiu na integração, extração e transformação de uma base de dados MySQL de um cenário de e-commerce e RH. O objetivo foi aplicar técnicas de limpeza e modelagem de dados para gerar insights sobre a estrutura organizacional da empresa.

🛠️ Tecnologias Utilizadas
Banco de Dados: MySQL (Hospedado no Clever Cloud)

Ferramenta de BI: Power BI Desktop

Linguagem de Consulta: SQL e Linguagem M (Power Query)

🚀 Adaptações de Infraestrutura
Diferente da proposta original que sugeria o uso do Azure, utilizei o Clever Cloud como provedor de banco de dados MySQL.

Motivação: Devido a limitações de acesso na conta de estudante (ausência de cartão de crédito para validação), o Clever Cloud foi a alternativa gratuita escolhida para manter a integridade do desafio.

Solução de Erros: O servidor apresentava limite de 5 conexões simultâneas (max_user_connections). Para solucionar, configurei o Power BI para desabilitar o carregamento paralelo de tabelas, garantindo a estabilidade da atualização dos dados.

Configuração realizada para contornar o limite de conexões simultâneas do servidor.

⚙️ Etapas de Transformação de Dados
Seguindo as diretrizes do desafio, realizei as seguintes ações no Power Query:

Cabeçalhos e Tipos: Ajuste de tipos de dados para colunas monetárias e numéricas.

Tratamento de Nulos: Análise de valores nulos em Super_ssn para identificação de gerentes.

Divisão de Colunas: Separação da coluna de endereço para melhor granularidade (Logradouro, Número).

Mesclagem de Consultas: * Junção de employee e departament para associar colaboradores aos seus respectivos departamentos.

Junção de nomes de departamentos e localizações para criar combinações únicas.

Criação de Colunas: Mesclagem de nomes e sobrenomes para criação da coluna Nome_Completo.

Agrupamento: Criação da tabela Colaboradores_por_Gerente para análise quantitativa de liderança.

Otimização de Modelo: Desabilitação da carga de tabelas auxiliares para o modelo de dados final, mantendo-as apenas no Power Query (identificadas pelo nome em itálico).

Visualização das consultas organizadas e otimizadas no Power Query.

💡 Por que usar 'Mesclar' e não 'Atribuir'?
Na diretriz 14, foi necessário explicar a escolha técnica. Utilize o Mesclar pois o objetivo era realizar um Join (extensão horizontal), trazendo colunas de uma tabela para outra com base em uma chave comum. O Atribuir (Append) seria usado apenas se fôssemos empilhar linhas (extensão vertical) de tabelas com a mesma estrutura.

📊 Visualização Final
O gráfico abaixo demonstra a distribuição de colaboradores por gerente, validando o tratamento de dados e a correta relação entre as entidades do banco.

👨‍💻 Desenvolvido por Vânia Bordin
