  <a href="https://www.cypress.io">
    <picture>
      <img alt="Cypress Logo" src="https://docs.cypress.io/guides/overview/why-cypress">
    </picture>    
  </a>

# cypress-pdf-report

### Configurando o cypress-pdf-report
Instale o pacote do cypress-pdf-report via NPM:

```js
npm install cypress-pdf-report --save-dev
```
No seu arquivo de configuração do Cypress (cypress.config.js)

```json
{
  "reporter": "cypress-pdf-report",
  "reporterOptions": {
    "overwrite": false,
    "htmlFolder": "cypress/reports",
    "pdfFolder": "cypress/reports",
    "fileName": "cypress-report.pdf"
  }
}
```

Para gerar o relatório em PDF após a execução dos testes, basta executar o seguinte comando no terminal:

```js
cypress run --reporter cypress-pdf-reporter
```
Isso executará seus testes e, após a conclusão, gerará o relatório em PDF com base nos arquivos HTML gerados.

---
### scripts
Um exemplo de script NPM no seu arquivo package.json para executar o Cypress com o cypress-pdf-report. Adicione o seguinte código ao seu arquivo package.json:

```json
"scripts": {
  "test": "cypress run --reporter cypress-pdf-report",
  "cypress:open": "cypress open",
  "openPdf":"xdg-open cypress/reports/cypress-report.pdf"
},
```
###  Resumo 
Nesse exemplo irá configurar o cypress-pdf-report para gerar um relatório em PDF chamado "cypress-report.pdf" a partir dos arquivos HTML gerados pelo Cypress. 
O relatório será salvo na pasta "cypress/reports" e o parâmetro "overwrite" é definido como falso para evitar a substituição de relatórios anteriores.
