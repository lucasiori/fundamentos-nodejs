<p align="center">
  <img src="https://github.com/lucasiori/fundamentos-nodejs/blob/master/.github/gostack.png" alt="GoStack" width="250" />
</p>

<h1 align="center">Desafio: Fundamentos do Node.js</h1>
<p align="center">
  <a href="#sobre-desafio">Sobre</a> &nbsp;&nbsp;|&nbsp;&nbsp;
  <a href="#executando-aplicacao">Executando a aplicação</a> &nbsp;&nbsp;|&nbsp;&nbsp;
  <a href="#rotas-aplicacao">Rotas</a> &nbsp;&nbsp;
  
</p>

<h2 id="sobre-desafio">ℹ Sobre o desafio</h2>

<p>
  Nesse desafio, você deve criar uma aplicação para continuar treinando o que você aprendeu até agora no Node.js junto ao TypeScript, 
  utilizando o conceito de models, repositories e services!
</p>
<p>
  Essa será uma aplicação para armazenar transações financeiras de entrada e saída, que deve permitir o cadastro e a listagem dessas transações.
</p>

<br />

<h2 id="executando-aplicacao">✅ Executando a aplicação</h2>

<strong>Requisitos:</strong>
<ul>
  <li>Node.js</li>
  <li>Gerenciador de pacotes: NPM ou Yarn</li>
</ul>

<p>
  Primeiramente, clone o repositório na sua máquina local: <br />
  <code>git clone https://github.com/lucasiori/fundamentos-nodejs</code>
</p>

<p>
  Acesse a pasta do projeto, e no terminal execute o comando para instalar as dependências: <br />
  <ul>
    <li>
      <strong>se estiver utilizando NPM: </strong>
      <code>npm install</code>
    </li>
    <li>
      <strong>se estiver utilizando Yarn: </strong>
      <code>yarn</code>
    </li>
  </ul>
</p>

<p>
  Após instaladas as dependências, certifique-se de que a porta <strong>3333</strong> está disponível pois é a porta onde a aplicação será executada. <br />
  Para iniciar o serviço, execute o comando: <br />
  <ul>
    <li>
      <strong>se estiver utilizando NPM: </strong>
      <code>npm run dev:server</code>
    </li>
    <li>
      <strong>se estiver utilizando Yarn: </strong>
      <code>yarn dev:server</code>
    </li>
  </ul>
</p>

<br />

<h2 id="rotas-aplicacao">🔀 Rotas da aplicação</h2>

<h3>🔵 GET</h3>

<p>
  <strong>Rota:</strong> /transactions <br />
  <strong>Descrição:</strong> Retorna a lista de transações cadastradas e o balanço atual. <br />
  <pre>
    {
      transactions: [
        {
          title: "Salario",
          type: "income",
          value: "1800,00"
        },
        {
          title: "Horas Extras",
          type: "income",
          value: "600,00"
        },{
          title: "Faculdade",
          type: "outcome",
          value: "620,00"
        }
      ],
      balance: {
        income: "2400,00",
        outcome: "620,00",
        total: "1780,00"
      }
    }
  </pre>
</p>

<br />

<h3>🟢 POST</h3>

<p>
  <strong>Rota:</strong> /transactions <br />
  <strong>Descrição:</strong> Cadastra uma nova transação. <br />
  <strong>Corpo da Requisição: </strong> Objeto JSON contendo título, valor e tipo ("income" ou "outcome") da transação.
  <pre>
    {
      title: "Salário",
      type: "income",
      value: "1600,00"
    }
  </pre>
</p>
