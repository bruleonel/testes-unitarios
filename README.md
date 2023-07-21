# anotações Importantes

Foi dados os comandos
- npm init -y <Para inicializar o projeto criando o arquivo package.json>
- npm install --save-dev eslint@8.16.0 --save-exact <Ferramenta de análise estática para o desenvolvimento>
- npx eslint --init <Configurações iniciais>

Será apresentado as seguintes opções:

You can also run this command directly using 'npm init @eslint/config'.
? How would you like to use ESLint? ...
  To check syntax only *Checa somente a sintaxe*
  To check syntax and find problems *Checa a sintaxe e problemas*
> To check syntax, find problems, and enforce code style *Checa a sintaxe, problemas e forca um padra de código*

- npx eslint index.js <Para executar o eslint>

ERRO: 
![Alt text](image.png)

SOLUÇÃO:
No arquivo .eslint.json

"""js

{
    "env": {
        "es2021": true,
        "node": true
    },
    "extends": "airbnb-base",
    "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module"
    },
    "rules": {
        "linebreak-style": 0
    }
}
""""

Alguns dos tipos de testes que podemos implementar, como: os estáticos, unitários, de integração e E2E. Sendo:

**Testes estáticos** - voltados para analisar o código sem necessariamente executá-lo, verificando se algumas boas práticas e formatação padronizada foram adotadas na implementação;

**Testes unitários** - são utilizados para verificar o comportamento das menores unidades de código da aplicação;

**Testes de integração** - são as fases do teste de software em que módulos são combinados e testados como um conjunto;

**Teste E2E (End-to-End)** - é um método de teste utilizado para testar um fluxo da aplicação desde o começo até o fim.


Para facilitar o uso do linter, utilizamos uma extensão para fazer a marcação de forma mais cômoda no VSCode.

Para “chamar” o Eslint no VSC e organizar seu código automaticamente, utilize o atalho ctrl + shift + P (Windows/Linux) ou cmd + shift + P (MacOs), digite Eslint e escolha a opção "Fix all auto-fixable problems" ou posicione o cursor piscante sobre alguma das linhas sublinhadas vermelhas e utilize o atalho ctrl + . para abrir o menu do Eslint e escolher “Fix all auto-fixable problems” se estiver disponível.
