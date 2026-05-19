-- Seleciona o banco de dados
USE db_visual_rak;

-- Lista tabelas e colunas com filtros dinâmicos
SELECT 
    t.name AS Tabela,
    c.name AS Coluna
FROM sys.tables t
JOIN sys.columns c 
    ON t.object_id = c.object_id
WHERE 
    t.name LIKE '%ROD%'          -- filtro de tabela
    AND c.name LIKE '%COD%'      -- filtro de coluna
ORDER BY 
    t.name, c.name


