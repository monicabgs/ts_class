# Typescript studies

- Typescript passa a ser considerado uma linguagem de programação, a partir do momento em que o Deno (ambiente de execução) é lançado, sendo capaz de fazer a interpretaçã da linguagem;
- Antigamente o Typescript era um conjunto de funcionalidades que podiamos adicionar ao JavaScript tradicional, dando mais poder à linguagem;
- Acabou se tornando popular justamente por conseguir implementar algumas features que o JavaScript tinha dificuldade na entrega;
- Em 2016, o JavaScript teve uma grande "explosão" de funcionalidades, passando a suportar Arrow function, classes, etc;
- O principal motivo para a utilização do TypeScript, mesmo com a evolução do Javascript ocorre devido a sua tipagem, ou seja, acrescentamos os tipos dos dados juntamente com o código o que "força" o formato correto.

# Demo - Instalações iniciais:

- Instalando o Node e NPM:
sudo apt update
sudo apt install nodejs //Ambiente de execução Javascript
sudo apt install npm //Gerenciador de pacotes do nodejs

- Configurando projeto:
cd ~ 
mkdir typescript-demo
cd typescript-demo
mkdir backend
cd backend
yarn init -y //inicializando projeto
yarn add -D typescript //Adicionando o typescript como dependência

- No terminal do VsCode, criando servidor:
yarn add express
mkdir src
cd src
touch index.ts
yarn add @types/express -D //Adicionando a tipagem do módulo express

- Para rodar código é necessário converter de typescript para javascript para que o Node consiga entender:
yarn tsc src/index.ts

- Rodando o código com arquivo convertido para javascript:
node src/index.js

- Testar aplicação via endpoint:
http://127.0.0.1:3333/
Ctrl+C

- Interpretando default:
cd backend
yarn tsc --init
yarn tsc

- Diretório criado para enviar arquivos convertidos para javascript 
no arquivo tsconfig.json, inclui em "outDir": "./build" um direório build onde são enviados os arquivos transformados para javascript (arquivos que vamos rodar com o node). Esses arquivos não podem ficar na mesma pasta dos arquivos.ts

- Realizando a execução em tempo de desenvolvimento (de forma mais automatizável):
yarn add ts-node-dev -D
alterar arquivo de package.json e inserir "scripts"