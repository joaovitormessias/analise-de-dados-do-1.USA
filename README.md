# 📊 Análise de Dados do 1.USA

## 📌 Sobre os Dados
Em 2011, o serviço de encurtamento de URL [Bitly](https://bitly.com) firmou uma parceria com o site do governo dos Estados Unidos, [USA.gov](https://www.usa.gov), para fornecer um feed de dados anônimos coletados de usuários que encurtavam links com domínios .gov ou .mil.

No mesmo ano, um **live feed** e **snapshots de hora em hora** ficaram disponíveis como arquivos de texto para download. Para os snapshots, cada linha dos arquivos segue o formato JSON, um padrão comum para representação de dados na web.

---

## 🛠 Etapas do Projeto
Este projeto passa por diversas etapas essenciais, incluindo:

1. **Coleta de Dados** 📥 - Download e armazenamento dos arquivos JSON.
2. **Limpeza e Tratamento** 🧼 - Remoção de inconsistências e padronização dos dados.
3. **Exploração e Análise** 🔍 - Identificação de padrões e tendências.
4. **Visualização** 📊 - Geração de gráficos para melhor compreensão das informações extraídas.

---

## 🚀 Configuração do Ambiente
Para executar este projeto localmente, recomendamos o uso do **Anaconda**. Siga os passos abaixo para instalá-lo e ativá-lo:

### 🔹 Instalação do Anaconda
1. Baixe o instalador do Anaconda para seu sistema operacional [aqui](https://www.anaconda.com/products/distribution).
2. Siga as instruções de instalação conforme o sistema operacional escolhido.
3. Verifique a instalação abrindo um terminal e executando:
   ```sh
   conda --version
   ```

### 🔹 Criação e Ativação do Ambiente
1. Crie um novo ambiente chamado `analise_usa`:
   ```sh
   conda create -n analise_usa python=3.9
   ```
2. Ative o ambiente:
   - No Windows:
     ```sh
     conda activate analise_usa
     ```
   - No macOS/Linux:
     ```sh
     source activate analise_usa
     ```
3. Instale as dependências necessárias:
   ```sh
   conda install pandas matplotlib seaborn jupyter
   ```

### 🔹 Executando o Projeto
Para iniciar a análise de dados, execute o seguinte comando no terminal:
```sh
jupyter notebook
```
Isso abrirá o navegador, permitindo que você execute os notebooks do projeto.

---

## 📢 Contribuição
Sinta-se à vontade para contribuir com melhorias para este projeto! Basta abrir um **Pull Request** ou sugerir mudanças na aba de **Issues**.

---

## 📜 Licença

Este projeto está licenciado sob a **MIT License** - consulte o arquivo `LICENSE` para mais detalhes.
