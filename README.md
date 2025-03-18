# 📊 Desafio DIO - Análise e Transformação de Dados
Este projeto faz parte do Desafio da DIO e tem como objetivo a análise e transformação de dados utilizando Power BI e MySQL. Durante o processo, foram aplicadas diversas técnicas para otimizar a estrutura dos dados, garantindo melhor organização e usabilidade.

## 🚀 Mudança de Plataforma
Inicialmente, o projeto seria implementado na Azure, porém, devido a problemas técnicos com a plataforma, optamos por utilizar um banco de dados MySQL. Essa mudança garantiu maior flexibilidade e continuidade no desenvolvimento, sem comprometer a integridade e a eficiência da solução.

## 🛠️ Modificações e Melhorias
🔹 Ajuste de Nomes
Algumas colunas tiveram seus nomes alterados para facilitar a compreensão.  
Exemplo: Mgr_ssn foi renomeado para Manager_ssn.  
🔹 Verificação de Cabeçalhos e Tipos de Dados  
Nenhuma modificação foi necessária nos cabeçalhos.  
Os valores monetários foram convertidos para decimal fixo para maior precisão.  
🔹 Tratamento de Valores Nulos  
Apenas um valor NULL foi identificado na coluna Super_ssn, correspondente ao gerente colaborador James Borg.  
Todos os departamentos possuem um identificador de gerente.  
## 🏗️ Transformações Aplicadas  
🔹 Separação de Colunas Complexas  
A coluna Address foi separada em quatro novas colunas:  
Number, Street, City, Postal_code.  
Antes da separação, foi necessário substituir o caractere "-" no nome composto da rua Fire-Oak.  
Após a substituição, a separação foi feita usando o recurso "Dividir coluna por delimitador".  
As colunas Fname e Lname foram combinadas em uma única coluna chamada Name.  
🔹 Criação da Tabela Company_employee_dpt  
Criada através do recurso "Mesclar consultas como novas".  
A tabela Employee foi utilizada como base, com o número do departamento como chave comum.
No final, foram mantidas apenas as colunas Departamento e Nome.  
## 🔄 Mesclagens e Junções  
🔹 Junção de Colaboradores e seus Respectivos Gerentes  
Foi criada uma nova coluna chamada superior_name na tabela Employee.  
O recurso Coluna Condicional do Power BI foi utilizado para atribuir o nome do gerente correspondente.  
🔹 Mescla de Nomes de Departamentos e Localização  
A mesclagem foi realizada utilizando o número do departamento como chave.  
Apenas a coluna Localização foi expandida.  
Criada uma nova coluna Departamento_Localização, combinando as colunas Nome do Departamento e Localização separadas por espaço.  
🔹 Explicação: Mesclar vs. Atribuir  
O recurso Mesclar foi utilizado porque queremos transformar duas colunas em uma única, sem a necessidade de criar colunas adicionais.  
O uso de Atribuir acrescentaria uma nova coluna ao invés de simplesmente combinar as já existentes.  
## 🚀 Conclusão
As transformações aplicadas aprimoram a estrutura dos dados, facilitando futuras análises e permitindo a criação de um modelo estrela em módulos futuros.  

## 🎯 Tecnologias Utilizadas:
✅ Power BI  
✅ Power Query  
✅ MySQL (substituindo a Azure devido a problemas técnicos)  
✅ SQL (opcional para junção de dados)  
