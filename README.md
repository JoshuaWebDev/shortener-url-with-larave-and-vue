# Shortener URL with Laravel and Vue.js

Desafio proposto como critério para ingressar na equipe da [Clínica Experts](http://clinicaexperts.com.br/)

## Descrição

O desafio consiste em desenvolver uma aplicação para encurtar links, semelhante ao conhecido [bit.ly](https://bit.ly/). Deverá existir uma interface inicial, onde o usuário irá inserir um link e como retorno terá uma URL curta.

## Requisitos

- O projeto deve ser desenvolvido com frontend em **Vue**, backend em **Laravel** e armazenar os dados em um banco de dados relacional (**MySql/MariaDB**);
- Utilizar o conceito de **API REST** com retornos em formato JSON;
- Criar telas para **cadastro, alteração, exclusão e listagem** dos links;
- Deve existir uma tela com a listagem de todos os links encurtados e também suas métricas de acesso, permitindo uma busca textual e uma ordenação por todos os campos da tabela;
- A tela de criação deverá enviar a **url do link (obrigatório)** e um **identificador (opcional)**. Lembre-se que **o identificador deve ser único**, pois será utilizado como slug para o novo link. Quando não informado, **deverá ser gerada uma string aleatória de 6 a 8 caracteres, incluindo letras e números**;
- Ao acessar um link encurtado, o sistema deve redirecionar o usuário para a página original e **gerar um registro do acesso**, salvando alguns dados da requisição, como o **IP**, o **User-Agent**, e incrementar um **contador de acessos** do link encurtado;
- Criar uma cron que irá zerar o número de acessos de todos os link no primeiro dia de cada mês;
