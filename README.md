# Banco API Performance

## 🎯 Objetivo do Projeto
Este projeto tem como objetivo realizar **testes de performance e carga** na API REST do projeto [Banco API](https://github.com/juliodelimas/banco-api), utilizando a ferramenta **K6**.  
Os testes medem o desempenho e o comportamento da API sob diferentes níveis de estresse, avaliando métricas como tempo de resposta, throughput e taxa de erro.

---

## ⚙️ Stack Utilizada
- **Linguagem:** JavaScript  
- **Ferramenta de Teste de Performance:** [K6](https://k6.io/docs/)  
- **Gerenciamento de Dependências:** npm  
- **Ambiente de Desenvolvimento:** Node.js

---

## 🗂️ Estrutura de Diretórios
```
banco-api-performance/
│
├── config/                # Arquivos de configuração (como URLs e parâmetros)
│   └── config.local.json
│
├── fixtures/              # Dados de entrada utilizados nos testes
│   └── postLogin.json
│
├── helpers/               # Funções auxiliares usadas nos scripts de teste
│   └── autenticacao.js
│
├── tests/                 # Scripts principais de teste de performance
│   ├── login.test.js
│   └── transferencias.test.js
│
├── utils/                 # Variáveis e funções utilitárias
│   └── variaveis.js
│
├── .gitignore             # Arquivo que define itens ignorados pelo Git
├── html-report.html       # Relatório de resultados (gerado automaticamente)
└── README.md
```

---

## 🚀 Execução dos Testes

### 1️⃣ Instalação das Dependências
Certifique-se de ter o **Node.js** e o **npm** instalados. Em seguida, instale as dependências do projeto:

```bash
npm install
```

### 2️⃣ Executar Testes de Performance
Para executar os testes com o K6:

```bash
k6 run tests/login.test.js
```

ou

```bash
k6 run tests/transferencias.test.js
```

### 📊 Gerando Relatórios Web com o K6

O K6 permite visualizar relatórios de execução diretamente no navegador ou gerar arquivos HTML com gráficos e métricas detalhadas sobre o desempenho dos testes.

---

### 🔹 Acessando a Documentação Oficial
A documentação sobre essa funcionalidade está disponível em:  
➡️ [K6 Docs – Results Output: Web Dashboard](https://k6.io/docs/results-output/web-dashboard/)

---

### 🔹 Gerar Relatório Html

Para gerar um arquivo HTML com o relatório completo:

```bash
K6_WEB_DASHBOARD=true K6_WEB_DASHBOARD_EXPORT=html-report.html k6 run tests/login.test.js
```

🔸 Esse comando:
- Gera o relatório interativo;
- E exporta automaticamente para o arquivo **`html-report.html`**.

## 📚 Documentação das Dependências

- [K6 - Documentação Oficial](https://k6.io/docs/)
- [Node.js](https://nodejs.org/en/docs)
- [npm - Gerenciador de Pacotes](https://docs.npmjs.com/)
