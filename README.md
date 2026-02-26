<div align="center">

<img src="https://cdn-icons-png.flaticon.com/512/2920/2920244.png" alt="CSV Analyzer Logo" width="110" />

# 📊 Leitor de Arquivo CSV — Análise de Vendas

**Uma aplicação de desktop em Java Swing para ler, processar e analisar**
**dados de vendas a partir de arquivos CSV.**

<br>

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Swing](https://img.shields.io/badge/Java%20Swing-GUI-007396?style=for-the-badge&logo=java&logoColor=white)
![Maven](https://img.shields.io/badge/Apache%20Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)
![CSV](https://img.shields.io/badge/CSV-Análise%20de%20Dados-217346?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completo-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

</div>

---

## 📚 Tabela de Conteúdos

> Navegue rapidamente pelas seções do projeto.

| # | Seção |
|:-:|:------|
| 1 | [📖 Sobre o Projeto](#-sobre-o-projeto) |
| 2 | [✨ Funcionalidades Principais](#-funcionalidades-principais) |
| 3 | [🛠️ Pilha de Tecnologias](#️-pilha-de-tecnologias) |
| 4 | [📋 Formato do CSV Esperado](#-formato-do-csv-esperado) |
| 5 | [📂 Estrutura do Projeto](#-estrutura-do-projeto) |
| 6 | [🚀 Como Compilar e Executar](#-como-compilar-e-executar) |
| 7 | [🤝 Como Contribuir](#-como-contribuir) |
| 8 | [👨‍💻 Autor](#-autor) |
| 9 | [📄 Licença](#-licença) |

---

## 📖 Sobre o Projeto

> **Leitor de CSV** é uma ferramenta de análise de dados de vendas desenvolvida em **Java** com interface gráfica criada com **Java Swing**.

A aplicação permite ao usuário carregar um arquivo `.csv` e, automaticamente, processa as informações para exibir análises relevantes sobre o desempenho das lojas: faturamento por unidade, produto mais vendido e visualização bruta dos dados. O projeto é gerenciado com **Apache Maven**.

---

## ✨ Funcionalidades Principais

| Ícone | Ação | Descrição |
|:-----:|:-----|:----------|
| 📂 | **Arquivo → Procurar...** | Abre um `JFileChooser` para localizar e selecionar o arquivo `.csv` desejado. |
| 📰 | **Arquivo → Abrir...** | Exibe o conteúdo bruto do CSV, calcula o faturamento total por loja e identifica o produto mais vendido. |
| 📈 | **Faturamento por Loja** | Calcula e exibe o faturamento total das primeiras quatro lojas encontradas no arquivo. |
| 🏆 | **Produto Mais Vendido** | Identifica e exibe o produto com maior quantidade total vendida. |
| 🧹 | **Botão LIMPAR** | Limpa todos os campos de texto e a área de visualização do CSV. |
| 🚪 | **Arquivo → Sair...** | Fecha a aplicação. |

---

## 🛠️ Pilha de Tecnologias

| Tecnologia | Função no Projeto |
|:-----------|:------------------|
| **Java 21+** | Linguagem principal — lógica de leitura, processamento e análise dos dados. |
| **Java Swing** | Construção da interface gráfica desktop (`JFrame`, `JFileChooser`, `JTextArea`). |
| **Apache Maven** | Gerenciamento do projeto, dependências e ciclo de build. |

---

## 📋 Formato do CSV Esperado

> Para que a leitura e os cálculos funcionem corretamente, o arquivo CSV deve seguir a estrutura abaixo.

| Propriedade | Valor Esperado |
|:------------|:---------------|
| **Delimitador** | Ponto e vírgula (`;`) |
| **Cabeçalho** | A **primeira linha** é ignorada automaticamente pelo programa. |
| **Encoding** | UTF-8 recomendado. |

### 📄 Exemplo de Arquivo CSV

```csv
loja;produto;quantidade;preco_unitario
Loja A;Produto X;10;25.00
Loja A;Produto Y;5;40.00
Loja B;Produto X;20;25.00
Loja B;Produto Z;8;15.00
Loja C;Produto Y;12;40.00
Loja D;Produto Z;3;15.00
```

---

## 📂 Estrutura do Projeto

```plaintext
AplicacaoLoja/
│
├── 📄 pom.xml                              # ⚙️  Configurações e dependências do Maven
│
└── 📁 src/
    └── 📁 main/
        └── 📁 java/
            └── 📁 aula02/
                └── 📁 aplicacaoloja/
                    ├── 📄 Painel.java      # 🖥️  Interface gráfica principal (JFrame) ← CORE
                    ├── 📄 Loja.java        # 🏛️  Modelo de dados — Loja
                    ├── 📄 Produto.java     # 🏛️  Modelo de dados — Produto
                    └── 📄 LeitorCSV.java   # 📂 Lógica de leitura e parsing do CSV
```

---

## 🚀 Como Compilar e Executar

### 📋 Pré-requisitos

| Requisito | Detalhe |
|:----------|:--------|
| **JDK** | Versão **21 ou superior** instalada e configurada no `PATH`. |
| **Apache Maven** | Instalado e configurado no `PATH`. |
| **Git** | Para clonar o repositório. |

---

### 💻 Opção 1 — Linha de Comando

**1. Clone o repositório e acesse a pasta do projeto:**

```bash
git clone https://github.com/VictorHJesusSantiago/AplicacaoLoja.git
cd AplicacaoLoja
```

**2. Compile o projeto com Maven:**

```bash
mvn compile
```

**3. Execute a classe principal:**

```bash
# Windows / Linux / macOS
java -cp "target/classes" aula02.aplicacaoloja.Painel
```

---

### 🖥️ Opção 2 — IDE (Recomendado)

```
1. Abra sua IDE preferida (IntelliJ IDEA, NetBeans ou Eclipse)
2. File → Open → Importe como "Projeto Maven existente"
3. Aguarde o Maven sincronizar as dependências
4. Localize: src/main/java/aula02/aplicacaoloja/Painel.java
5. Clique com o botão direito → "Run" (ou pressione Shift + F10)
```

---

### 🎯 Como Usar a Aplicação

| Passo | Ação |
|:-----:|:-----|
| 1️⃣ | Inicie a aplicação pelo método acima. |
| 2️⃣ | Clique em **Arquivo → Procurar...** e selecione seu arquivo `.csv`. |
| 3️⃣ | Clique em **Arquivo → Abrir...** para processar e visualizar os resultados. |
| 4️⃣ | Analise o **faturamento por loja** e o **produto mais vendido** nos campos exibidos. |
| 5️⃣ | Use o botão **LIMPAR** para resetar todos os campos e carregar um novo arquivo. |

---

## 🤝 Como Contribuir

> Contribuições são muito bem-vindas! Siga as etapas abaixo para colaborar de forma organizada.

| Passo | Ação | Comando |
|:-----:|:-----|:--------|
| 1️⃣ | **Fork** | Crie um fork do repositório para a sua conta. | — |
| 2️⃣ | **Branch** | Crie sua feature branch a partir da `main`. | `git checkout -b feature/NovaFeature` |
| 3️⃣ | **Commit** | Salve as alterações com mensagem clara e semântica. | `git commit -m 'feat: Adiciona NovaFeature'` |
| 4️⃣ | **Push** | Envie a branch para o repositório remoto. | `git push origin feature/NovaFeature` |
| 5️⃣ | **Pull Request** | Abra um PR detalhando as mudanças realizadas. | — |

<div align="center">

<br>

**Se este projeto foi útil para os seus estudos, deixe uma estrela ⭐️ no repositório!**

</div>

---

## 👨‍💻 Autor

<div align="center">

<br>

**Victor H. J. Santiago**

<br>

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/VictorHJesusSantiago)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/victor-henrique-de-jesus-santiago/)

</div>

---

## 📄 Licença

<div align="center">

Este projeto está distribuído sob a **Licença MIT**.
Consulte o arquivo [`LICENSE`](./LICENSE) no repositório para mais informações.

![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

</div>

---

<div align="center">

*Feito com 📊 e Java por **Victor H. J. Santiago***

</div>
