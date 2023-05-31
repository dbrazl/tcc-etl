# ETL COVID 19

Olá! Esse é o repositório das rotinas de ETL.
Por meio desses script, é possível a criação e população das tabelas de fato e dimensões de forma automatizada.

Rotinas:
- Extrair dados das tabelas .csv;
- Criar tabelas vazias de fatos e dimensões;
- Transformar e separar as colunas das tabelas base;
- Popular as tabelas de dimensões;
- Popular as tabelas de fatos.

# Como iniciar?

Basta clonar o repositório:

```bash
    git clone git@github.com:dbrazl/tcc-etl.git
```

Instalar as dependências:

```bash
    yarn
```

Criar uma pasta ```data``` com os arquivos ```.csv``` das tabelas do Brasil IO.

```bash
    mkdir data
```

```bash 
    cp ~/Downloads/caso_full.csv ~/PROJECT_PATH/tcc-etl/data/caso_full.csv
    cp ~/Downloads/caso.csv ~/PROJECT_PATH/tcc-etl/data/caso.csv
    cp ~/Downloads/obito_cartorio.csv ~/PROJECT_PATH/tcc-etl/data/obito_cartorio.csv
```

A onde o ```PROJECT_PATH``` é o caminho até ao repositório local.

E rodar o script de ```create``` ou o de ```update```. A diferença entre eles é que o de criar, exclui todo o banco de dados e cria as tabelas de fatos e dimensões novamente caso elas já existam. Se não existirem, apenas as criam. Enquanto o de inserir, insere os dados novos em ```data``` para a as atuais tabelas de fatos e dimensões sem perder os dados anteriores.
O script de inserir não verifica duplicidade dos dados. Verifique se as tabelas que estão em ```data``` não são tabelas antigas antes de executá-lo.

```bash
yarn run create
```

```bash
yarn run update
```

# Contribuidores

<a href="https://github.com/dbrazl" style="text-decoration: none; display:  color: black;">
  <img src="https://github.com/dbrazl.png" width="150px" height="150px" alt="Daniel Braz" />
</a>

[Daniel Braz](https://github.com/dbrazl)