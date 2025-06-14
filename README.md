# Projeto 1: Construção de um Pipeline de Dados Simples para Análise de Logs de Servidor Web

Este projeto tem como objetivo construir um pipeline simples de análise de logs de servidores web, utilizando Python e bibliotecas como Pandas e Requests. O pipeline segue as etapas de **Extração**, **Transformação** e **Geolocalização** dos dados dos logs, facilitando a análise e visualização de informações relevantes sobre acessos e requisições ao servidor.

## Sumário

- [Descrição](#descrição)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Como Executar](#como-executar)
- [Principais Funcionalidades](#principais-funcionalidades)
- [Exemplo de Uso](#exemplo-de-uso)
- [Dependências](#dependências)
- [Licença](#licença)

---

## Descrição

O pipeline consiste em:

1. **Extração:** Leitura dos arquivos de log do servidor web.
2. **Transformação:** Estruturação dos dados extraídos em um DataFrame, separando informações como IP, data/hora, método HTTP, recurso, status, etc.
3. **Geolocalização:** Utilização de uma API pública para buscar informações de localização dos endereços IP presentes nos logs.

## Estrutura do Projeto

```
.
├── ArquivosLogs/
│   └── server_example.log
├── index.ipynb
└── README.md
```

- `ArquivosLogs/server_example.log`: Exemplo de arquivo de log de servidor web.
- `index.ipynb`: Notebook principal com todo o pipeline de análise.
- `README.md`: Este arquivo de documentação.

## Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/kingsonPaxe/Projecto1-Construcao-de-uma-pipline-para-analise-de-logs-de-servidores-web.git
   cd Projecto1-Construcao-de-uma-pipline-para-analise-de-logs-de-servidores-web
   ```

2. Instale as dependências necessárias:
   ```bash
   pip install pandas requests
   ```

3. Abra o notebook `index.ipynb` em um ambiente Jupyter (Jupyter Notebook, JupyterLab, Google Colab, etc.) e execute as células sequencialmente.

## Principais Funcionalidades

- **Leitura e extração de dados** de arquivos de logs do servidor.
- **Transformação dos dados** para uma estrutura tabular (DataFrame).
- **Separação automática** de campos relevantes: endereço IP, data/hora, método, recurso, protocolo, status HTTP, quantidade de bytes, etc.
- **Geolocalização de IPs** usando a API pública `ip-api.com`.
- **Análise exploratória dos dados** com Pandas.

## Exemplo de Uso

No notebook, você encontrará exemplos como:

- Leitura do log:
  ```python
  with open(r"ArquivosLogs/server_example.log") as file_log:
      log = file_log.readlines()
  ```

- Estruturação em DataFrame:
  ```python
  df = pd.DataFrame(data)
  ```

- Geolocalização dos IPs:
  ```python
  resposta = rqts.get(f"http://ip-api.com/json/{ip}")
  ```

## Dependências

- Python 3.7+
- pandas
- requests

Instale as dependências com:
```bash
pip install pandas requests
```

## Licença

Este projeto está sob a licença MIT. Consulte o arquivo LICENSE para mais detalhes.

---

Desenvolvido por [kingsonPaxe](https://github.com/kingsonPaxe).
