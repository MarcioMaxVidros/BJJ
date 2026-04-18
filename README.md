# Fratres BJJ — Sistema de Gestão
### Unidade Haydee

Sistema de gestão completo para a academia **Fratres Jiu-Jitsu**, unidade Haydee. Desenvolvido em HTML/CSS/JavaScript puro, sem dependências externas, com persistência local via `localStorage`.

---

## Acesso

O sistema roda diretamente no navegador, sem necessidade de servidor.

**Hospedagem via GitHub Pages:**
- Acesse: `https://[seu-usuario].github.io/[nome-do-repo]`

**Usuários:**
| Usuário | Perfil |
|---|---|
| Sthella Vilela | Gestora da Unidade |
| Cleisson Ribeiro | Black Belt Coach |

> ⚠️ As senhas padrão do repositório público são `fratres2026` para ambos os usuários.
> Para definir senhas personalizadas, edite a linha `const senhas={...}` no arquivo `index.html` e **não faça commit** dessa alteração.

---

## Funcionalidades

- **Dashboard** — visão geral com KPIs, últimos cadastros e alertas de estoque
- **Alunos** — ficha cadastral completa (dados pessoais, faixa, kimono, plano, contrato)
- **Kids** — módulo dedicado com cards visuais por faixa, checklist de técnicas e contato dos pais
- **Check-in** — registro de presença por sessão, com contagem de treinos por aluno
- **Graduações** — acompanhamento de progresso por treinos e promoção de faixa
- **Prospects** — pipeline de leads com avanço por etapa (Visita → Avaliação → Proposta → Convertido)
- **Lojinha** — cadastro de produtos, controle de estoque por tamanho e registro de vendas
- **Financeiro** — lançamentos manuais de entradas e saídas por sessão
- **Notificações** — agenda de mensagens (push/WhatsApp exigem backend)

---

## Persistência de dados

Todos os dados são salvos no `localStorage` do navegador — o que significa:

| ✅ Funciona | ⚠️ Limitação |
|---|---|
| Dados persistem entre sessões | Dados ficam apenas neste dispositivo/navegador |
| Funciona offline | Não sincroniza entre dois dispositivos ao mesmo tempo |
| Sem servidor necessário | Limpar o cache do navegador apaga os dados |

### Quando será necessário banco de dados

| Funcionalidade | Precisa de BD? |
|---|---|
| Fichas cadastrais e estoque | Não — funciona com localStorage |
| Check-in em múltiplos dispositivos | ✅ Sim |
| Mensalidades recorrentes automáticas | ✅ Sim |
| Push/WhatsApp automático | ✅ Sim |
| Integração Wellhub / TotalPass API | ✅ Sim |
| Acesso por múltiplas unidades | ✅ Sim |

**Stack recomendada para evolução:**
- **Banco de dados:** Supabase (PostgreSQL gerenciado, gratuito até 500 MB)
- **Autenticação:** Supabase Auth (já inclui)
- **Hospedagem:** Vercel ou Netlify

---

## Identidade Visual

Paleta de cores extraída do logo oficial Fratres BJJ:

| Cor | Hex | Uso |
|---|---|---|
| Charcoal | `#2C2C2C` | Fundo sidebar, anéis externos |
| Cinza médio | `#888888` | Segundo anel |
| Roxo/Violeta | `#7B5EA7` | Acento principal, botões, tabs |
| Azul aço | `#5B9BD5` | Acento secundário |
| Dourado | `#E5B300` | Stripes de graduação |

---

## Estrutura do projeto

```
fratres-bjj/
├── index.html     ← aplicação completa (single file)
└── README.md      ← este arquivo
```

---

## Desenvolvido com

Claude (Anthropic) — geração e iteração do código  
Fratres BJJ Unidade Haydee — requisitos e identidade visual

---

*Fratres BJJ · O Tatame nos Une, a Fraternidade nos Fortalece.*
