# Atividade 4 - Cabeçalho compartilhado

Projeto de páginas do curso de Desenvolvimento de Software Multiplataforma (DSM), utilizando **Node.js + Express**.

Nesta atividade, o cabeçalho é mantido em um único arquivo (`server/partials/header.html`) e incluído pelo servidor em todas as páginas que possuem o marcador `<!-- shared-header -->`.

## Tecnologias
- Node.js
- Express
- HTML5
- CSS3
- ES Modules

## Estrutura do projeto
```text
app/
├── package.json
├── package-lock.json
├── .env
├── public/
│   ├── index.html
│   ├── assets/
│   │   ├── css/index.css
│   │   └── images/
│   └── pages/
│       ├── 1dsm.html
│       ├── 2dsm.html
│       ├── 3dsm.html
│       ├── 4dsm.html
│       ├── 5dsm.html
│       └── 6dsm.html
└── server/
    ├── main.js
    └── partials/
        └── header.html
```

## Como executar
1. Instale as dependências:
   ```bash
   npm install
   ```
2. Inicie o servidor:
   ```bash
   npm start
   ```
3. Acesse `http://localhost:3001` no navegador. A porta padrão está definida no arquivo `.env`.

## Como funciona o cabeçalho compartilhado
O arquivo `server/partials/header.html` contém os logos do DSM, da Fatec e do CPS, o título do curso e os links dos seis semestres. Nas páginas HTML, o comentário `<!-- shared-header -->` marca o local de inclusão. O mecanismo HTML configurado em `server/main.js` lê a página e o cabeçalho com `readFile()` e substitui o marcador antes de enviar o resultado ao navegador.
