# Projeto de enquetes em Real Time
-> Tecnologias utilizadas: 
 - Node.js
 - PostgreSQL
 - Prisma
 - WebScokets
 - Redis

Os protocolos que serão utilizados: Métodos HTTP e Protocolo WebSocket.

# Aula01:

> WebSocket: 
É uma forma de estabelecer uma comunicação bidirecional e em tempo real entre um navegador web(client) e um servidor web(server).


O WebSockets, ele não é uma requisição de via única, ela vai se manter aberta enquanto o usuário estiver vendo os dados da enquete.


> Redis:
O Redis é um banco de dados que ira armazenar a quantidade de votos na enquetes. É mais simples separar no Redis, pois é muito custoso para o PostgreSQL e ficar aumentando o seu processamento. No Redis iremos fazer um cache ou uma versão estática, pois o Redis é um banco de dados muito leve. Essa quantidade de votos será transmitida via websocket.

> Node.js: 
Ter a versão do Node mais atual e sempre verificar a sua versão.



> Comandos executados:
- npm init -y: Cria um arquivo package.json onde mostra os scripts para automatizar tarefas e mostra suas dependencias.

- npm install typescript @types/node -D: Serve para poder instalar o typescript e utilizar ele na aplicação e o types node é a integração do node com o typescript. O -D serve para adicionar ele como uma dependência do projeto.

- npx tsc --init: ele vai irá criar um arquivo chamado tsconfig.json. Esse arquivo serve para  indicar qual é a raiz do projeto e serve para especificar os arquivos raiz e as configurações de compilação necessárias para o projeto.

