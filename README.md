# Django MySQL Example

Este projeto é um exemplo de integração do Django com o banco de dados MySQL, seguindo o fluxo de criação de banco, configuração do settings.py e migração dos modelos.

## Pré-requisitos
- Python 3.x
- pipenv
- MySQL Server

## Instalação
1. Clone o repositório:
   ```sh
   git clone https://github.com/gct00/django-mysql.git
   cd django-mysql
   ```
2. Ative o ambiente virtual:
   ```sh
   pipenv shell
   ```
3. Instale as dependências:
   ```sh
   pipenv install
   ```

## Configuração do Banco de Dados
1. Crie o banco de dados e o usuário no MySQL:
   ```sql
   CREATE DATABASE reservations;
   CREATE USER 'admindjango'@'localhost' IDENTIFIED BY 'employee@123!';
   GRANT ALL ON *.* TO 'admindjango'@'localhost';
   FLUSH PRIVILEGES;
   ```
2. As configurações de acesso ao banco já estão em `myproject/settings.py`.

## Migrações
Execute:
```sh
python manage.py makemigrations
python manage.py migrate
```

## Rodando o servidor
```sh
python manage.py runserver
```

Acesse: http://127.0.0.1:8000/

## Observações
- O modelo principal está em `myapp/models.py`.
- O banco de dados utilizado é o MySQL.
- O usuário padrão do banco é `admindjango` com senha `employee@123!`.

---

Projeto para fins didáticos, baseado em exercícios da Coursera Full Stack. 