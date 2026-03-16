# Task Portal

Portal de gerenciamento de tarefas e comunicação interna, desenvolvido com Bubble (no-code/low-code) como trabalho prático da disciplina de Fundamentos de No-Code e Low-Code — UniFECAF.

---

## Sobre o Projeto

O **Task Portal** é uma aplicação web funcional que permite que times colaborem, criem e atualizem tarefas com comentários e notificações. O objetivo foi validar um modelo de negócio real em 30 dias, sem código tradicional.

### Funcionalidades

- Cadastro e login de usuários com autenticação nativa do Bubble
- Criação e gerenciamento de times com membros
- Criação de tarefas com título, descrição, prioridade, prazo, time e responsável
- Atualização de status das tarefas (pending → in_progress → done)
- Comentários em tarefas com notificações automáticas
- Central de notificações com marcação de lidas
- Sidebar de navegação como Reusable Element reutilizado em todas as páginas
- Privacy Rules configuradas por tipo de dado para segurança

---

## Como Acessar e Testar

**Link da aplicação:** https://task-portal-19645.bubbleapps.io

**Conta de demonstração:**
- Email: `demo@taskportal.com`
- Senha: `Demo@2025`

**Fluxo sugerido para teste:**
1. Acesse o link acima
2. Faça login com a conta demo ou crie uma nova conta
3. Crie um time em "Times"
4. Crie uma tarefa em "+ Nova Tarefa" no dashboard
5. Abra a tarefa e adicione um comentário
6. Acesse "Notificações" para ver as notificações geradas

---

## Tecnologias Utilizadas

| Tecnologia | Uso |
|---|---|
| **Bubble** | Plataforma no-code principal — UI, banco de dados, workflows |
| **Bubble Data Types** | Banco de dados relacional (User, Team, Task, Comment, Notification) |
| **Bubble Workflows** | Lógica de negócio: cadastro, login, criação de tasks, comentários, notificações |
| **Bubble Privacy Rules** | Controle de acesso por tipo de dado e usuário |
| **Bubble Reusable Elements** | Sidebar de navegação reutilizada em todas as páginas autenticadas |

---

## Estrutura de Páginas

```
index          → Login e cadastro (Signup Popup)
dashboard      → Lista de tarefas do usuário + popup de criação
task-detail    → Detalhe da tarefa + comentários
teams          → Gerenciamento de times + popup de criação
notifications  → Central de notificações
```

### Dashboard

![Dashboard](images/page-dashboard.png)

### Detalhe da Tarefa

![Detalhe da Tarefa](images/page-task-detail.png)

### Central de Notificações

![Notificações](images/page-notifications.png)

### Sidebar (Reusable Element)

![Sidebar](images/reusable-sidebar.png)

---

## Modelagem de Dados

```
User          → name, avatar, role
Team          → name, description, created_by (User), members (list of Users)
Task          → title, description, status, priority, due_date,
                assigned_to (User), created_by (User), team (Team)
Comment       → content, author (User), task (Task)
Notification  → message, type, is_read, recipient (User), related_task (Task)
```

### Tipos de Dados

| Tipo | Imagem |
|---|---|
| User | ![User](images/data-type-user.png) |
| Team | ![Team](images/data-type-team.png) |
| Task | ![Task](images/data-type-task.png) |
| Comment | ![Comment](images/data-type-comment.png) |
| Notification | ![Notification](images/data-type-notification.png) |

---

## Privacy Rules

As regras de privacidade controlam o acesso aos dados por tipo e usuário autenticado.

| Tipo | Imagem |
|---|---|
| User | ![Privacy User](images/privacy-user.png) |
| Team | ![Privacy Team](images/privacy-team.png) |
| Task | ![Privacy Task](images/privacy-task.png) |
| Comment | ![Privacy Comment](images/privacy-comment.png) |
| Notification | ![Privacy Notification](images/privacy-notification.png) |

---

## Workflows

Principais fluxos de negócio implementados no Bubble.

### Autenticação

| Ação | Imagem |
|---|---|
| Login | ![Login](images/workflow-login.png) |
| Erro de Login | ![Erro de Login](images/workflow-login-error.png) |
| Cadastro | ![Cadastro](images/workflow-signup.png) |
| Logout | ![Logout](images/workflow-logout.png) |
| Página Protegida | ![Página Protegida](images/workflow-protected-page.png) |

### Tarefas e Times

| Ação | Imagem |
|---|---|
| Nova Tarefa | ![Nova Tarefa](images/workflow-new-task.png) |
| Novo Time | ![Novo Time](images/workflow-new-team.png) |
| Criar Comentário | ![Criar Comentário](images/workflow-create-comment.png) |
| Marcar Notificações como Lidas | ![Notificações Lidas](images/workflow-read-all-notifications.png) |

---

## Autor

**João Henrique Benatti Coimbra**
- GitHub: [github.com/joao-coimbra](https://github.com/joao-coimbra)
- LinkedIn: [linkedin.com/in/joao-henrique-benatti-coimbra](https://www.linkedin.com/in/joao-henrique-benatti-coimbra)

---

*Trabalho desenvolvido para a disciplina de Fundamentos de No-Code e Low-Code — UniFECAF, 2026.*
