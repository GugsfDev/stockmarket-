erDiagram
    PRODUTOS ||--o{ MOVIMENTACOES : possui

    PRODUTOS {
        int id_produto PK
        varchar nome
        varchar categoria
        int quantidade
        int estoque_minimo
        decimal preco
        datetime data_cadastro
    }

    MOVIMENTACOES {
        int id_movimentacao PK
        int id_produto FK
        enum tipo
        int quantidade
        datetime data
    }
