# Extraindo Texto de Imagens com AWS Textract

## Visão Geral

Este projeto demonstra como utilizar o AWS Textract para extrair texto de imagens de forma programática utilizando Python. O código realiza a detecção de texto em uma imagem local e armazena o resultado em um arquivo JSON para posterior análise.

## Tecnologias Utilizadas

- Python 3.8+
- AWS Textract (via boto3)
- JSON para armazenamento de respostas
- mypy\_boto3\_textract para tipagem

## Como Funciona?

1. O script lê uma imagem contendo texto armazenada localmente na pasta `images`.
2. A imagem é enviada para o AWS Textract via a função `detect_file_text()`.
3. A resposta da API é salva em um arquivo `response.json`.
4. A função `get_lines()` lê esse JSON e retorna uma lista de linhas extraídas do texto da imagem.
5. Caso o JSON não exista, a função `detect_file_text()` é chamada automaticamente.

## Requisitos

- Conta AWS configurada com credenciais válidas.
- Biblioteca `boto3` instalada.
- IAM Role ou usuário com permissões para utilizar o AWS Textract.
- Python 3.8 ou superior.

## Instalação

1. Clone o repositório:

   ```sh
   git clone https://github.com/Zh0ny/nexa-analise-avancada-de-imagens-e-texto-com-ia-na-aws.git
   ```

2. Configure suas credenciais AWS (caso ainda não tenha feito):

   ```sh
   aws configure
   ```

\*Não esqueça de configurar o ambiente de trabalho, foi utilizado o anaconda com python 3.12.7, e instalar as bibliotecas como o boto3.

## Como Executar

Execute o script com o comando:

```sh
python main.py
```

O texto extraído da imagem será exibido no terminal e salvo em `response.json`.

## Prints e Exemplos

### Exemplo de Arquivo `response.json`

```json
{
    "Blocks": [
        {"BlockType": "LINE", "Text": "Lista de Material Escolar"},
        {"BlockType": "LINE", "Text": "- Cadernos"},
        {"BlockType": "LINE", "Text": "- Lápis"}
    ]
}
```

## Possíveis Melhorias e Insights

- Implementar suporte para processamento de múltiplas imagens automaticamente - Modo de processamento em lotes.
- Melhorar o tratamento de erros para lidar com diferentes exceções do AWS Textract.
- Criar uma interface gráfica simples para facilitar o uso do script por usuários não técnicos - talvez usar uma biblioteca de TUI (Terminal user interface).
- Armazenar os resultados extraídos em um banco de dados para consultas futuras.

