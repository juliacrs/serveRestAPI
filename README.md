# serveRestAPI
Criaçao de testes de API utilizando: postman, newman-html-extra e dados de massa por: csv e randomuser.me

# O que é
Este repositorio foi criado com a finalidade de ser executado na pipeline do GitHub.

# Tecnologias utilizadas
- Postman (versao web)
* Necessario ter o node instalado para executar a instalaçao do newman
  * newman-reporter-html@1.0.5
  * newman-reporter-htmlextra@1.23.1
  * newman@6.2.1

# Documentações
- Doc da API: [Consulte Swagger](https://serverest.dev/)
- Doc da API de geraçao de Massa: https://randomuser.me/

# Como instalar o ambiente
1. Instale o node em seu computador - https://nodejs.org/en/download
2. Realize a instação do newman (dependência) de forma global - https://www.npmjs.com/package/newman
```
    npm install -g newman
```
3. Realize a instalação da dependência dos relatórios [opcional]
  - https://www.npmjs.com/package/newman-reporter-html
  - https://www.npmjs.com/package/newman-reporter-htmlextra
```
   npm install -g newman-reporter-html
   npm install -g newman-reporter-html-extra
```

# Como rodar os testes
### Pelo Postman web ou desktop
- Importe a collection e o environment
- Execute os testes de forma manual ou automatizada 

### Pelo Newman
- Abra o console de preferencia
- Execute a seguinte linha de comando para rodar os testes
```
    newman run ServeRest.postman_collection.json -e ServeRest.postman_environment.json -r cli
```
- Execute os testes com relatorio
```
    newman run ServeRest.postman_collection.json -e ServeRest.postman_environment.json -r cli,htmlextra
```
### Report
Se voce optou por rodar os testes com o report htmlextra, então gerará um relatorio html dentro da pasta **newman** no local em que os arquivos collection e environment se encontram para que se possa verificar as validações dos resultados.

# Contato
Linkedin: https://www.linkedin.com/in/juliana-crs/

