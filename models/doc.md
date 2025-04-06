  

# 🧾 Nome da Tela/Função

> _Exemplo: Cadastro de Agendamentos_

  

---

  

## 📌 Descrição Geral

Breve descrição da funcionalidade e seu propósito no sistema.

  

> Exemplo:

> Tela que permite o agendamento de serviços por parte do administrador, com vínculo a clientes e horários disponíveis.

  

---

  

## ⚙️ Regra de Negócio

  

- [ ] Quais campos são obrigatórios?

- [ ] Existem validações específicas?

- [ ] Algum processo automatizado (ex: envio de e-mail)?

- [ ] Regras de permissão (quem pode acessar/editar)?

  

> Exemplo:

> - Apenas administradores podem acessar essa tela.

> - Um cliente só pode ter um agendamento por dia.

> - O horário só pode ser agendado se estiver livre.

  

---

  

## 🗂️ Estrutura do Banco de Dados

  

### 🔁 Tabelas Envolvidas

  

```text

- users: usuários do sistema

- appointments: agendamentos

- services: serviços oferecidos

```

  

### 🆕 Novas Tabelas (DBML)

  

```dbml
Insira aqui o dbml
```
  
📎 [Visualizar no dbdiagram.io](https://dbdiagram.io/) *(link deve ser atualizado com seu próprio modelo)*
## 🌐 Rotas/API

#### 📥 `GET /endpoint`
- **Descrição**: Descrição da rota  
- **Permissão**: `permissões/middlewares da rota`

---

  

## 🖼️ Layout da Tela

  

### Wireframe / Mock

  

- [ ] Inserir imagem ou link do Figma

- [ ] Indicar campos e ações

  

### Componentes

  

- Campo de seleção de cliente

- Campo de seleção de serviço

- Picker de data e horário

- Botão “Agendar”

- Tabela com listagem de agendamentos

  

---

  

## ✅ Checklist de Implementação

  

- [ ] Criar migration da nova tabela

- [ ] Criar model/controller

- [ ] Criar rotas na API

- [ ] Criar tela e layout

- [ ] Validar regras de negócio

- [ ] Testes manuais

  

---

  

## 🗒️ Observações Adicionais

  

> Exemplo: O campo `status` será sempre “pending” ao criar, e atualizado manualmente depois do serviço concluído.