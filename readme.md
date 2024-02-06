# Projeto de enquetes em Real Time
-> Tecnologias utilizadas: 
 - Node.js
 - PostgreSQL
 - Prisma
 - WebScokets
 - Redis

Os protocolos que serão utilizados: Métodos HTTP e Protocolo WebSocket.

# WebSocket: 
É uma forma de estabelecer uma comunicação bidirecional e em tempo real entre um navegador web(client) e um servidor web(server).


O WebSockets, ele não é uma requisição de via única, ela vai se manter aberta enquanto o usuário estiver vendo os dados da enquete.


# Redis:
O Redis é um banco de dados que ira armazenar a quantidade de votos na enquetes. É mais simples separar no Redis, pois é muito custoso para o PostgreSQL e ficar aumentando o seu processamento. No Redis iremos fazer um cache ou uma versão estática, pois o Redis é um banco de dados muito leve. Essa quantidade de votos será transmitida via websocket.

