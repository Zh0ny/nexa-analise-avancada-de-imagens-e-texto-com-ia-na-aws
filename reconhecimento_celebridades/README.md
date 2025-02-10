Reconhecimento de Celebridades com AWS Rekognition

Este projeto utiliza o serviço AWS Rekognition para identificar celebridades em imagens e desenhar caixas delimitadoras ao redor de seus rostos.

📌 Tecnologias Utilizadas

Python 3.x

AWS Rekognition (via boto3)

Pillow (PIL) para manipulação de imagens

mypy_boto3_rekognition para tipagem estática com boto3

🚀 Como Funciona

O código carrega imagens de uma pasta images.

Usa a API do AWS Rekognition para detectar celebridades nas imagens.

Se forem encontradas celebridades com alta confiança (>90%), ele desenha caixas vermelhas ao redor de seus rostos e salva a imagem editada.

O resultado é salvo na mesma pasta com o sufixo -resultado.jpg.

📂 Estrutura do Projeto

/ ── images/
│   ├── bbc.jpg
│   ├── msn.jpg
│   ├── neymar-torcedores.jpg
│
├── recognize_celebrities.py
├── requirements.txt
├── README.md

🛠️ Como Configurar

1️⃣ Clonar o Repositório

git clone https://github.com/Zh0ny/nexa-analise-avancada-de-imagens-e-texto-com-ia-na-aws.git
cd seu-repositorio*
*Caminho do repositório na máquina.

4️⃣ Configurar Credenciais da AWS

Para utilizar o Rekognition, você precisa configurar suas credenciais AWS. Se ainda não tiver configurado:

aws configure

E insira suas credenciais de acesso.

5️⃣ Executar o Código

python recognize_celebrities.py
*Caso esteja usando o uv deve usar: uv run recognize_celebrities.py

*Não esqueça de instalar as dependências boto3, PIL, mypy_boto3_rekognition

As imagens processadas aparecerão na pasta images/ com o sufixo -resultado.jpg.

📷 Exemplo de Saída

Imagem original: neymar-torcedores.jpg

Imagem processada: neymar-torcedores-resultado.jpg (Com caixa delimitadora e nome da celebridade).

🔥 Aprendizados e Melhorias Futuras

✅ Integração com AWS Rekognition e manipulação de imagens com Pillow.
✅ Trabalhar com Bounding Boxes para marcação de rostos.
✅ Melhorar a tipagem estática com mypy_boto3_rekognition.

📌 Melhorias futuras:

Adicionar suporte para múltiplas imagens.

Criar uma interface gráfica para facilitar o uso.

Integrar com um banco de dados para armazenar os resultados, para uso posterior.

Implementar o código para vídeos, semelhante ao que é feito no filme do Homem de Ferro.

📢 Contribuições são bem-vindas! Caso tenha sugestões ou melhorias, fique à vontade para abrir um PR ou issue. 🚀

