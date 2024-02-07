# Projeto de enquetes em Real Time
-> Tecnologias utilizadas: 
 - Node.js
 - PostgreSQL
 - Prisma
 - WebScokets
 - Redis
 - Fastify
 - Docker

Os protocolos que serão utilizados: Métodos HTTP e Protocolo WebSocket.

# Aula01:

> WebSocket: 
É uma forma de estabelecer uma comunicação bidirecional e em tempo real entre um navegador web(client) e um servidor web(server).
O WebSockets, ele não é uma requisição de via única, ela vai se manter aberta enquanto o usuário estiver vendo os dados da enquete.


> Redis:
O Redis é um banco de dados que ira armazenar a quantidade de votos na enquetes. É mais simples separar no Redis, pois é muito custoso para o PostgreSQL e ficar aumentando o seu processamento. No Redis iremos fazer um cache ou uma versão estática, pois o Redis é um banco de dados muito leve. Essa quantidade de votos será transmitida via websocket.

> Node.js: 
Ter a versão do Node mais atual e sempre verificar a sua versão.

> Fastify:
Comando de instalação:
npm i fastify:

Framework para Node.js, onde deverá ser importado o fastify na aplicação.

> Docker:
Acessar o Get Docker na máquina, abrir o docker e rodar os seguintes comando "docker ps" - ele irá verificar se existe algum container rodando(não irá ter).

Será criado um arquivo no projeto docker-compose.yml, dentro dele irá conter quais serão os serviços que nossa aplicação irá precisar. Neste caso será o PostgreSQL e o Redis.


Executar o comando docker compose up -d, esse comando baixa as imagens e deixa elas rodando em background.

> Prisma:
O Prisma é uma biblioteca que trás uma interface para fazermos queries no banco de dados com uma linguagem mais clara. 

Comando de instalação:
npm install -D prisma

Comando para execução: 
npx prisma init

Ao executar o comando de inicialização, terá um arquivo .env que deverá conter as informações para conectar com o banco.

Dentro de uma pasta chamada "prisma", terá um arquivo chamado schema.prisma, esse será o arquivo que iremos para efetuar a criação e conteúdos de banco de dados.

Após efetuar a configuração dos arquivos e criação de uma tabela, no terminal iremos executar o comando npx migrate dev - que irá lhe perguntar o que você fez, nesse caso será "create polls", após isso ele cria um arquivo SQL com os comandos de configuração da tabela, e um arquivo de informações criadas. Para verificar o que foi criado é só digitar no terminal npx prisma studio

> Comandos executados:
- npm init -y: Cria um arquivo package.json onde mostra os scripts para automatizar tarefas e mostra suas dependencias.

- npm install typescript @types/node -D: Serve para poder instalar o typescript e utilizar ele na aplicação e o types node é a integração do node com o typescript. O -D serve para adicionar ele como uma dependência do projeto.

- npx tsc --init: ele vai irá criar um arquivo chamado tsconfig.json. Esse arquivo serve para  indicar qual é a raiz do projeto e serve para especificar os arquivos raiz e as configurações de compilação necessárias para o projeto. As configurações efetuadas foram verificadas no site https://github.com/microsoft/TypeScript/wiki/Node-Target-Mapping

-npm install tsx -D: ela converte o TypeScript para JavaScript para poder executar o código. Tudo isso de maneira atualizada.
