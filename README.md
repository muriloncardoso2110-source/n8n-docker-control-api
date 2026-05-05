
# n8n-docker-control-api
=======
# 🐳 n8n Docker Control API

Este projeto transforma o n8n em uma API de gerenciamento para serviços Docker. Ele permite iniciar ou parar containers remotamente através de requisições HTTP seguras, executando comandos via SSH diretamente no servidor.

## 🚀 Funcionalidades
- **Interface via Webhook**: Aceita comandos de qualquer lugar do mundo.
- **Segurança Basic Auth**: Proteção por usuário e senha no ponto de entrada.
- **Execução via SSH**: Conecta de forma segura ao servidor para rodar comandos.
- **Verificação de Status**: O fluxo lê a resposta do terminal e confirma se a ação foi concluída com sucesso.



## 🛠️ Tecnologias Utilizadas
- **n8n**: Orquestração do fluxo.
- **Docker Compose**: Gerenciamento dos containers.
- **SSH**: Protocolo de comunicação segura com o servidor.
- **JSON**: Estrutura de dados para parâmetros de rota.

## 📋 Como Importar
1. Baixe o arquivo `workflow.json` deste repositório.
2. No seu n8n, clique em **Workflows** > **Import from File**.
3. Configure as credenciais de **HTTP Basic Auth** (para o Webhook) e **SSH Password** (para o seu servidor).

## 📡 Exemplo de Uso
Você pode disparar o comando via Terminal (cURL) ou integrá-lo a um botão no celular:

```bash
curl -X POST -u "usuario:senha" [https://seu-n8n.com/docker/start/meu-servico](https://seu-n8n.com/docker/start/meu-servico)

⚠️ Requisitos
Servidor Linux com Docker e Docker Compose instalados.

Usuário SSH com permissão para executar comandos docker.


---

### 4. Subindo os arquivos pelo site (Jeito Fácil)
Se você não quiser usar o terminal (Git), pode fazer tudo pelo navegador:
1.  No seu repositório no GitHub, clique em **Add file** > **Upload files**.
2.  Arraste o `workflow.json` e o seu `README.md` (se você editou fora).
3.  Clique em **Commit changes**.
>>>>>>> 81f1872 (feat: initial commit with n8n docker control workflow and documentation)
