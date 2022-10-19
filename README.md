# Introdução ao Express

Neste exercício você usará a estrutura Express para implementar uma funcionalidade semelhante à implementada pelos servidores baseados no módulo HTTP no NodeJS. Ao final deste exercício, você será capaz de:

	- Implementar um servidor web simples usando a estrutura Express
	- Implementar um servidor web que veicule conteúdo estático

Um servidor simples usando o Express

	- Crie um repositório no GitHub chamado "nodejs-express"
	- Clone-o na raíz do sistema operacional do seu computador
	- Acesse-o com o comando: cd nodejs-express
	- Crie o arquivo package.json com o comando: npm init
	- Responda as perguntas com as respostas padrão
	- Crie uma subpasta com o comando: mkdir public
	- Crie dois arquivos na pasta public: index.html e sobre.html
	- Instale o Express com o comando: nom install express --save
	- Crie um arquivo chamado .gitignore contendo node_modules
	- Crie um arquivo chamado index.js com o seguinte conteúdo:

	const express = require('express'),
     http = require('http');

	const hostname = 'localhost';
	const port = 3000;

	const app = express();

	app.use((req, res, next) => {
	  console.log(req.headers);
	  res.statusCode = 200;
	  res.setHeader('Content-Type', 'text/html');
	  res.end('<html><body><h1>This is an Express Server</h1></body></html>');

	});

	const server = http.createServer(app);

	server.listen(port, hostname, () => {
	  console.log(`Server running at http://${hostname}:${port}/`);
	});



