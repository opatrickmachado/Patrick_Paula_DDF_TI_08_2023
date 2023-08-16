1. - ## **Case 5: Consulta SQL para Usuários Recentes**

     Para selecionar usuários que se cadastraram nos últimos 30 dias na tabela "users emails", a consulta seria:

     ```
     SELECT * FROM `users emails`
     WHERE DATE(`data_de_cadastro`) > CURDATE() - INTERVAL 30 DAY;
     ```

     **Explicação**:

     - `SELECT *`: Seleciona todos os campos da tabela.
     - `FROM 'users emails'`: Especifica a tabela de onde os dados serão retirados.
     - `WHERE`: Define a condição para filtrar os registros.
     - `DATE(data_de_cadastro)`: Converte o campo `data_de_cadastro` para um formato de data.
     - `CURDATE()`: Retorna a data atual.
     - `- INTERVAL 30 DAY`: Subtrai 30 dias da data atual.

     Assim, a consulta retornará todos os registros de usuários que se cadastraram nos últimos 30 dias.