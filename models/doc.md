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

### 🆕 Nova Tabela: appointments

| Campo | Tipo | Descrição |

|-------------|-----------|-----------------------------------------|

| id | bigint | Chave primária |

| user_id | bigint | Chave estrangeira para `users` |

| service_id | bigint | Chave estrangeira para `services` |

| date | date | Data do agendamento |

| time | time | Horário do agendamento |

| status | string | Status do agendamento (pending, done) |

| created_at | timestamp | Registro de criação |

| updated_at | timestamp | Registro de atualização |

> Observações:

> - FK (user_id) → users(id)

> - FK (service_id) → services(id)

---

## 🌐 Rotas/API

| Método | Rota | Descrição | Permissão |

|--------|-------------------------|---------------------------|------------|

| GET | /api/appointments | Lista agendamentos | admin/user |

| POST | /api/appointments | Cria novo agendamento | admin |

| PUT | /api/appointments/{id} | Atualiza agendamento | admin |

| DELETE | /api/appointments/{id} | Remove agendamento | admin |

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
