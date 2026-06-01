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

**Projeto Supabase:** `closers-uniasselvi`
**URL:** `https://wfequjtoutpqvfyjdrvo.supabase.co`
**Anon Key:** `sb_publishable_NYXnlMO9SZc4Sg3zxPCZtw_Uto0gecQ`

**Tabelas planejadas:**
- `matriculas` — registros de matrículas
- `colaboradores` — lista de consultores cadastrados

**Email de notificação:** `kleberson.azevedo@vitru.com.br`
**Serviço de email:** Resend (integrado via Supabase Edge Function)

---

## GitHub Pages

**Conta:** `vitrucontactSales`
**Repositório:** `vitrucontactSales/closers-forms-uniasselvi`
**URL pública:** `https://vitrucontactsales.github.io/closers-forms-uniasselvi/`
**Arquivos publicados:** `index.html`, `dashboard.html`, `Logo_Uniasselvi.png`

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

## Status do projeto

- [ ] Lista de consultores — aguardando coordenadora
- [ ] Lista de polos — aguardando coordenadora
- [x] Supabase configurado — tabelas `matriculas` e `colaboradores` criadas
- [x] Repositório GitHub criado — `vitrucontactSales/closers-forms-uniasselvi`
- [x] Formulário `index.html` — integrado com Supabase, tema dark, logo real
- [x] Identidade visual Uniasselvi aplicada
- [ ] Dashboard `dashboard.html` — criar após receber as listas
- [ ] Email de notificação — Supabase Edge Function + Resend
- [ ] Publicar no GitHub Pages
