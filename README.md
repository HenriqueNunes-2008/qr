#  Projeto QR

Um projeto para geração de QR Codes e registro de horas trabalhadas desenvolvido para a Fleximedical/Kure.

Este repositório contém ferramentas e scripts que permitem gerar QR Codes e registrar informações de horas trabalhadas, com persistência em nuvem, facilitando o uso de QR Codes em sistemas de controle e integração com outros módulos.

---

## 📌 Sobre

Este projeto possui funcionalidades para gerar, registrar e salvar QR Codes, ideal para aplicações como:
* Registro de dados com QR Code
* Integração com sistemas de leitura automática
* Automatização de processos por meio de QR Codes

Este repositório organiza os arquivos de forma simples, utilizando **Python (Flask)** e integração direta com banco de dados.

## 🛠️ Tecnologias e Infraestrutura

O projeto utiliza uma arquitetura moderna para garantir que os dados não sejam perdidos e que a aplicação esteja sempre online:

* **Linguagem:** Python 3.12+
* **Framework Web:** Flask
* **Banco de Dados:** Supabase (PostgreSQL) para armazenamento seguro dos registros.
* **Hospedagem:** Render para deploy contínuo.
* **Planilhas:** Integração com `openpyxl` para geração de relatórios Excel.

## 🧠 Funcionalidades

✔️ Geração dinâmica de QR Codes.
✔️ Registro automático de informações no **Supabase**.
✔️ Interface web amigável.
✔️ Exportação de dados para Excel.
✔️ Configuração via variáveis de ambiente (Segurança).

## 📁 Estrutura do Repositório

```text
qr/
├── .devcontainer/    # Configurações de desenvolvimento
├── Registro_qr/      # Código principal (app.py, templates, etc.)
├── .gitignore        # Arquivos ignorados pelo Git (como o .env)
├── requirements.txt  # Dependências Python atualizadas
└── README.md         # Documentação do projeto
🔐 Configuração de Segurança
Este projeto utiliza variáveis de ambiente para proteger credenciais sensíveis.

Crie um arquivo chamado .env na raiz do projeto.

Adicione suas chaves do Supabase:

Snippet de código
SUPABASE_URL=seu_link_do_projeto
SUPABASE_ANON_KEY=sua_chave_api_anonima
O arquivo .env nunca será enviado para o GitHub por estar listado no .gitignore.

🚀 Como Usar
1. Instalação
Clone o repositório e instale as dependências:

Bash
git clone [https://github.com/HenriqueNunes-2008/qr.git](https://github.com/HenriqueNunes-2008/qr.git)
cd qr
pip install -r requirements.txt
2. Execução Local
Certifique-se de que o seu .env está configurado e execute:

Bash
python Registro_qr/app.py
🌐 Deploy no Render
Ao realizar o deploy no Render, adicione as chaves SUPABASE_URL e SUPABASE_ANON_KEY na seção Environment Variables do painel de controle para que a aplicação funcione corretamente online.
