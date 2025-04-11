# 🛍️ Alura Ecommerce com OpenAI

Este projeto simula um sistema de ecommerce com funcionalidades inteligentes integradas com a API da OpenAI. Ele utiliza Java e a biblioteca [openai-java](https://github.com/TheoKanning/openai-java) para processar linguagem natural em diferentes cenários como análise de sentimentos, categorização de produtos, perfis de clientes, contagem de tokens e geração de produtos.

---

## 🚀 Tecnologias Utilizadas

- Java 17+
- OpenAI API
- Biblioteca openai-java (TheoKanning)
- jtokkit (para contagem de tokens)
- Maven

---

## 📁 Estrutura do Projeto
src/main/java/br/com/alura/ecommerce/ ├── AnaliseDeSentimentos.java ├── CategorizadorDeProdutos.java ├── ContadorDeTokens.java ├── IdentificadorDePerfil.java └── TestaIntegracao.java

---

## ✨ Funcionalidades

### ✅ `AnaliseDeSentimentos.java`
Analisa avaliações de produtos usando IA e salva arquivos com:
- Resumo das avaliações
- Sentimento geral (POSITIVO, NEUTRO ou NEGATIVO)
- Pontos fortes e fracos

Requisitos:
- Arquivos `.txt` contendo avaliações no diretório `src/main/resources/avaliacoes`.

### ✅ `CategorizadorDeProdutos.java`
Interage com o usuário via terminal para categorizar produtos com base em categorias válidas fornecidas.

### ✅ `ContadorDeTokens.java`
Mostra a quantidade de tokens de um prompt e estima o custo da requisição com base na API da OpenAI.

### ✅ `IdentificadorDePerfil.java`
Lê um CSV com lista de compras de clientes e identifica o perfil de compra de cada cliente usando IA.

Requisitos:
- Arquivo CSV em `src/main/resources/compras/lista_de_compras_100_clientes.csv`.

### ✅ `TestaIntegracao.java`
Testa integração com OpenAI gerando nomes fictícios de produtos para ecommerce.

---

## 🛠️ Como Executar

### 1. Clonar o repositório

git clone (https://github.com/calebewerneckcouto/OpenaiApiKeyJava.git)
cd seurepositorio
2. Definir a variável de ambiente da API da OpenAI
No terminal:

Linux/macOS:
export OPENAI_API_KEY=sua-chave-da-api
Windows CMD:
set OPENAI_API_KEY=sua-chave-da-api
3. Compilar e rodar
Você pode executar via sua IDE favorita (IntelliJ, Eclipse, etc) ou via terminal com Maven:
mvn clean compile
mvn exec:java -Dexec.mainClass="br.com.alura.ecommerce.AnaliseDeSentimentos"
