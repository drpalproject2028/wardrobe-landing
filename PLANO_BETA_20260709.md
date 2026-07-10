# Wardrobe AI — Landing + Estratégia de Beta Testers (09/07/2026)

## Diagnóstico da landing actual

**Ficheiro**: `public/index.html` (+ `/en/index.html`). Última alteração 07/07 (limpeza de referências PALCORE/Beta/TestFlight/preços fantasma).

**O que está bom** (manter): design limpo, bilingue PT/EN, RGPD completo (privacidade/termos, consentimentos 18+/marketing/beta explícitos no form), 8 features bem escritas e diferenciadoras (classificação IA, marca detectada, outfits gerados, aprendizagem, inspiração em designers, mood do dia, partilha 9:16, privacidade Magic Link).

**O problema real**: a copy é 100% "lista de espera passiva" — *"Fica a saber quando estiver disponível... avisamos-te assim que estiver disponível na App Store"*. Não há nenhuma menção a TestFlight nem CTA de acção imediata. Isto está desalinhado com o objectivo actual: recrutar beta testers **agora**, antes de submeter à App Store.

**Dados reais**: 15 leads capturados (13 querem beta, só 2 partilham no IG), todos activos (zero unsubscribes), mas **nenhum lead novo desde 17/05** — quase 2 meses sem tráfego/conversão novos.

## Recomendação: MELHORAR, não refazer

O design e a estrutura servem bem o objectivo. Não há razão para reconstruir — é uma mudança de mensagem/CTA, não de arquitectura:

1. **Trocar a secção final** de "fica a saber quando estiver disponível" → "junta-te à beta" com CTA claro e acção imediata (link TestFlight público quando existir, ou "responde a este email" enquanto o link não existe).
2. **Adicionar um badge/secção "Beta em curso"** com contexto honesto (nº de lugares, o que esperar de uma beta — bugs, feedback pedido).
3. Limpar CSS morto (`.pricing*`, já sem conteúdo desde 07/07).
4. Manter o resto (features, RGPD, bilingue) inalterado.

## Estratégia de beta em camadas (decisão do Paulo: Apple Review só depois de ter várias pessoas a testar)

TestFlight não exige App Review completo para testers internos/externos limitados — só a "Beta App Review" (leve) para lá de ~100 externos. Isto permite testar sem decidir já "empresa vs pessoal":

| Camada | Quem | Quando | Acção |
|---|---|---|---|
| 1 — Círculo próximo | Pessoas de confiança directa (Nuno Ferreira, Misha, amigos próximos) | Já | Convite directo TestFlight (email/link), sem landing |
| 2 — 15 leads existentes | Os 13 que marcaram `consent_beta=true` na landing | Assim que build TestFlight estiver pronta | Email directo (não precisa de nova landing) |
| 3 — Skool PALCORE / AIGémeos | Comunidade já existente | Depois da camada 1-2 dar feedback estável | Post de reactivação do Skool (ver Caderno #07) + link TestFlight |
| 4 — Público (landing actualizada) | Quem encontrar a landing | Depois de validar com 3 camadas anteriores | Landing com CTA "junta-te à beta" + link TestFlight público |

**Decisão empresa vs pessoal**: adiar para depois da Camada 2-3 (feedback real de várias pessoas). Não bloqueia o arranque da Camada 1.

**Pendentes técnicos conhecidos que bloqueiam camadas 2+**: Magic Link bypass para testers + formulário TestFlight (ver memória `project_wardrobe_ai_launch`).

## Plano de posts de divulgação (calendário curto)

A produzir com o agente `palcore-social-strategist` quando a Camada 1 tiver feedback inicial (não antes — publicar antes de ter testers reais seria promessa vazia):

1. **Skool PALCORE**: post de "abertura de beta" ancorado no Caderno #07 (segundo cérebro / automatismos) — cross-promoção natural.
2. **LinkedIn pessoal**: post mais formal, "estou a testar uma app que construí" — tom de builder, não de marketing.
3. **Instagram/TikTok**: se fizer sentido dado o público (moda/outfits), 1 clip curto do fluxo real da app.

## Próximos passos concretos

1. Editar `public/index.html` + `/en/index.html`: secção final + CTA (Sonnet, mudança pequena e local).
2. Confirmar com o Paulo quando a build TestFlight está pronta para a Camada 1 arrancar.
3. Não tocar em `wardrobe-ai`/`wardrobe-install` (outros projectos Vercel) sem confirmar que não há sobreposição de domínio.
