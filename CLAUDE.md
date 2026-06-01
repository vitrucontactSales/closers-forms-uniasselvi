# Formulário Closers — Uniasselvi

## O que é este projeto

Sistema web de registro de matrículas para consultores de vendas da Uniasselvi, operado pela equipe **Closers**. Aplicação 100% estática (HTML/JS), usando **Supabase** como backend (banco PostgreSQL) e **GitHub Pages** como hospedagem.

---

## Arquivos do projeto

| Arquivo | Função |
|---|---|
| `index.html` | Formulário principal de registro de matrículas |
| `dashboard.html` | Painel analítico com KPIs, gráficos e tabela de registros |
| `relatorio.html` | Relatório individual por consultor |
| `CLAUDE.md` | Documentação do projeto |

---

## Backend — Supabase

**Projeto Supabase:** a configurar
**URL:** `SUPABASE_URL` (a preencher após criar projeto no Supabase)
**Anon Key:** `SUPABASE_ANON_KEY` (a preencher)

**Tabelas planejadas:**
- `matriculas` — registros de matrículas
- `colaboradores` — lista de consultores cadastrados

**Email de notificação:** `kleberson.azevedo@vitru.com.br`
**Serviço de email:** Resend (integrado via Supabase Edge Function)

---

## GitHub Pages

**Conta:** `vitrucontactSales`
**Repositório:** a criar (`closers-forms-uniasselvi` sugerido)
**Arquivos publicados:** `index.html`, `dashboard.html`, `relatorio.html`

---

## Identidade Visual — Uniasselvi

| Cor | Hex | Uso |
|---|---|---|
| Amarelo Uniasselvi | `#FFD400` | Destaques, CTAs, botões |
| Preto | `#000000` | Textos e elementos fortes |
| Branco | `#FFFFFF` | Fundo principal |
| Cinza Escuro | `#333333` | Textos secundários |
| Cinza Médio | `#666666` | Apoio visual |
| Cinza Claro | `#F5F5F5` | Cards e fundos suaves |

---

## Dados do formulário

**Tipos de matrícula:**
- Graduação
- Ed. Continuada

**Gestores:**
- Sandoval Eduardo Nazareth Souza
- Jhonatan Erik Ribeiro Dias
- Beatriz Ferrari Jordao

**Consultores:** a definir (lista chega amanhã)
**Polos:** a definir (lista chega amanhã)

**Campos obrigatórios (provisório — confirmar):**
1. Consultor(a)
2. Nº Candidato — deve começar com `2026`
3. Data do Pagamento
4. Link da Conversa
5. Tipo de Matrícula — Graduação / Ed. Continuada
6. Gestor(a)
7. Polo
8. Observações (opcional)

---

## Regras de negócio planejadas

- Número de candidato deve começar com `2026`
- Bloqueio de duplicatas via constraint único no Supabase
- Verificação de duplicata antes de salvar (front-end + banco)
- Acesso ao Dashboard protegido por senha
- Cadastro de colaboradores protegido por senha (só gestor)
- Email de notificação ao cadastrar novo colaborador

---

## Pendências para iniciar desenvolvimento

- [ ] Lista de consultores
- [ ] Lista de polos
- [ ] Criar projeto no Supabase e obter URL + Anon Key
- [ ] Criar repositório GitHub `closers-forms-uniasselvi`
- [ ] Confirmar campos do formulário
