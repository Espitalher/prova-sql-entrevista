# Teste de SQL Intermediário

## Instruções:

1. **Banco de Dados:**
    - Estrutura de banco de dados fornecida com base no PostgreSQL.

2. **Esquema do Banco de Dados:**
    - O banco de dados possui as seguintes tabelas:
        - `EMPRESA (id_empresa, razao_social, inativo)`
        - `PRODUTOS (id_produto, descricao, inativo)`
        - `CONFIG_PRECO_PRODUTO (id_config_preco_produto, id_vendedor, id_empresa, id_produto, preco_minimo, preco_maximo)`
        - `VENDEDORES (id_vendedor, nome, cargo, salario, data_admissao, inativo)`
        - `CLIENTES (id_cliente, razao_social, data_cadastro, id_vendedor, id_empresa, inativo)`
        - `PEDIDO (id_pedido, id_empresa, id_cliente, valor_total, data_emissao, situacao)`
        - `ITENS_PEDIDO (id_item_pedido, id_pedido, id_produto, preco_praticado, quantidade)`

3. **Tarefas:**
    - a. **Consultas Básicas:**
        - Escreva consultas SQL para obter as seguintes informações:
            - Lista de funcionários ordenando pelo salário decrescente.
            - Lista de pedidos de vendas ordenado por data de emissão.
            - Valor de faturamento por cliente.
            - Valor de faturamento por empresa.
            - Valor de faturamento por vendedor.
    - b. **Consultas de Junção:**
        - Escreva consultas SQL para obter as seguintes informações usando junções:
            - Unindo a listagem de produtos com a listagem de clientes, procure o último preço praticado nesse cliente com esse produto, formule o preço base do produto dentro da coluna chamada preco_base no seu select, conforme a seguinte regra:
                - O preço base do produto deve obedecer a configuração de preço da tabela CONFIG_PRECO_PRODUTO.
                - Caso as junções não retornem o último preço praticado, utilize o menor da configuração de preço do produto.
                - Nesta mesma consulta, os seguintes campos deverão estar contidos:
                    - Id do produto em questão;
                    - Descrição do produto;
                    - Id do cliente do pedido;
                    - Razão social do cliente;
                    - Id da empresa do pedido;
                    - Razão social da empresa;
                    - Id do vendedor do pedido;
                    - Nome do vendedor;
                    - Preço mínimo e máximo da configuração de preço;
                    - Preço base do produto conforme a regra.

**Observações:**
- Certifique-se de que suas consultas são eficientes e otimizadas.
- Utilize comentários para explicar suas consultas, se necessário.
