# Convenções de nomenclatura para banco de dados

## Sobre

Estão são minhas anotações para convenções de nomenclatura. Serão notas incrementais, sob constante revisão ao longo dos cursos e desenvolvimentos em andamento.

## Geral

Nomes das tabelas e colunas devem estar **minúsculas** e as palavras devem ser separadas por **underscore**, seguindo o padrão [snake case](https://en.wikipedia.org/wiki/Snake_case). Todos os termos em inglês. Preferir nomes descritivos, evitando contrações.

## Tabelas

Nomes das tabelas no **plural**.

Ex:
- **Bom**: `users`, `posts`, `roles`, `room_categories`
- **Ruim**: `user`, `post`, `grupos`, `quarto_categoria`

## Colunas

Os nomes das colunas devem estar no **singular**.

Ex:
- **Bom**: `cpf`, `name`, `age`
- **Ruim**: `endereco`, `posts`, `idade`

## Foreign keys

Todas as foreign keys devem seguir o padrão `nome_da_tabela_no_singular_id`.

Por exemplo, caso a tabela `users` tenha um relacionameto com a tabela `roles`, o nome da coluna foreign key da tabela `users` deve ser `role_id`.

## Primary keys

A primary key de toda tabela deve ser uma coluna de inteiros com incremento automático, chamada `id`.

## Stored Procedures

Nomes das Stored Procedures com prefixo 'sp_' + nome tabela + ação.

Ex. 'sp_users_save', 'sp_orders_save'.

## Timestamps

Toda tabela deve definir duas colunas para colocar os timestamps: `created_at` e `updated_at`. A coluna `created_at` recebe automaticamente o timestamp do momento que o registro for criado. A coluna `updated_at` recebe automaticamente o timestamp do momento que o registro for alterado. 

## Referências

- https://gist.github.com/thiamsantos/654ec002f04c86d53611923a8b4c3a65
- http://guides.rubyonrails.org/active_record_basics.html#naming-conventions
- https://laravel.com/docs/5.5/eloquent#defining-models
- http://www.laravelbestpractices.com/#database_conventions
