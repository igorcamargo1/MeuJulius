# MeuJulius

Uma API para sistema 

##EndPoints
-Despesas
    -cadastrar
    -apagar
    -listar todas
    -alterar
    -mostrar detalhes

-Contas
    -cadastrar
    -apagar
    -listar todas
    -alterar
    -mostrar detalhes

### Cadastrar Despesas

    `POST` /meujulius/api/despesa

    **Campos de Requisição**


    | campo      |   tipo  | obrigatório | descrição 
    |-------     |---------|-------------|----------
    |valor       | decimal |     sim     | o valor da despesa, deve ser maior que zero
    | data       | data    |    sim      | a data da despesa
    |conta_id    | int     |   sim       | o id de uma conta previamente cadastrada
    |categoria_id| int     |    sim      | o id de uma categoria previamente cadastrada
    |descricao   | texto   |    não      | um texto sobre a despesa

    **Exemplo por requisição**

    ```
    {
        valor: 100.00,
        data: '2023-02-27',
        conta_id: 1,
        categoria_id: 1,
        descricao:"cinema - homem aranha"
    }
    ```

    **Respostas**

    | código | descricao |
    | -      |-
    | 201 | despesa cadastrada com sucesso
    | 400 | campos inválidos
