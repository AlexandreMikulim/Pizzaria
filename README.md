
# Apresentação do Projeto

Este projeto consiste em uma aplicação de interface para uma pizzaria e um sistema de cadastro de emails para clientes interessados em receber benefícios. Ele é composto por:

- **Backend em Python** (hospedado no Render).
- **Frontend responsivo**, hospedado em:
  - **AWS EC2**.
  - **AWS S3**.

A solução foi projetada para facilitar pedidos e criar um canal direto de comunicação com clientes por meio de benefícios exclusivos.

## Funcionalidades

### 1. Frontend Web

- Interface responsiva para interação com os clientes.
- Navegação amigável e design otimizado para diferentes dispositivos.
- Sistema de pedidos via WhatsApp integrado por meio do serviço **Categoriza**, que converte interações em links dinâmicos para facilitar o envio de pedidos diretamente para o WhatsApp.
- Hospedagem redundante:
  - **AWS EC2**: [http://13.59.24.60](http://13.59.24.60).
  - **AWS S3**: [https://fatfood.s3.us-east-2.amazonaws.com/teste/index.html](https://fatfood.s3.us-east-2.amazonaws.com/teste/index.html).

### 2. Backend (API)

- Desenvolvido em Python utilizando Flask.
- Endpoint para cadastro de emails de clientes interessados em benefícios.
- Hospedado no Render: [https://github.com/AlexandreMikulim/CadastroPizzaria.git](https://github.com/AlexandreMikulim/CadastroPizzaria.git).

### 3. Integração de Componentes

- Conexão entre frontend e backend para coleta de informações e atualização de dados.

## Orientação para Instalação de Dependências

O backend utiliza dependências listadas no arquivo `requirements.txt`. Para instalar as dependências:

1. Certifique-se de ter o Python 3.8+ instalado.
2. Crie um ambiente virtual (opcional, mas recomendado):

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # Linux/macOS
   venv\Scripts\activate  # Windows
   ```

3. Instale as dependências:

   ```bash
   pip install -r requirements.txt
   ```

## Passo a Passo para Rodar a Aplicação

### 1. Frontend (Site Web)

#### AWS EC2

- O frontend está hospedado em uma instância EC2 acessível em: [http://13.59.24.60](http://13.59.24.60).
- A configuração foi feita utilizando servidores web como Apache ou NGINX, com os arquivos do site copiados para o diretório raiz de publicação.

#### AWS S3

- Uma cópia estática do site também está em: [https://fatfood.s3.us-east-2.amazonaws.com/teste/index.html](https://fatfood.s3.us-east-2.amazonaws.com/teste/index.html).

### 2. Backend (API)

#### Hospedagem no Render

- O backend foi deployado no Render e pode ser encontrado em:
  - [https://github.com/AlexandreMikulim/CadastroPizzaria.git](https://github.com/AlexandreMikulim/CadastroPizzaria.git).
  - [https://github.com/AlexandreMikulim/Pizzaria.git](https://github.com/AlexandreMikulim/Pizzaria.git).

#### Passos Locais para Rodar o Backend

1. Acesse o diretório onde o arquivo `app.py` está localizado.
2. Certifique-se de que todas as dependências foram instaladas.
3. Execute o backend:

   ```bash
   python app.py
   ```

4. A API deve estar acessível em `http://localhost:5000` (por padrão).

## Notas Finais

- Certifique-se de que as regras de segurança nas plataformas AWS e Render permitem o tráfego HTTP e HTTPS.
- Teste a conexão entre o frontend e backend para garantir que está tudo funcionando corretamente.
