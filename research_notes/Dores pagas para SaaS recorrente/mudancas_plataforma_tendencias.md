# Dores pagas criadas por mudanças recentes de plataforma/mercado e tendências de busca (pesquisa: nov/2026)

> Convenção: **[FATO]** = afirmação com URL. **[SUPOSIÇÃO]** = inferência minha, sem fonte direta. Notas pontuais (0–10) são julgamento do pesquisador, não dados.
> Limitação de coleta: buscas via motor de busca (EUA); fetch direto bloqueado para developers.facebook.com e support.wati.io nesta sessão (host não permitido na rede). Reddit raramente apareceu diretamente nos resultados; quando há citação de Reddit, ela veio via terceiros (indicado).

## 1. Quais ferramentas/APIs foram encerradas, degradadas ou reprecificadas em 2024–2026, deixando usuários órfãos?

### Takeaway
A mudança mais recente e com dor financeira recorrente é a cobrança da API do WhatsApp Business (por mensagem desde 01/07/2025 e **mensagens de serviço cobradas desde 01/10/2026**). Outras mudanças verificadas (Pocket, Instagram Basic Display, sites do Google Business Profile, X API, num=100 do Google, links externos na App Store) ou já têm substitutos fortes ou atingem públicos pequenos.

### Cited Findings
**WhatsApp Business Platform (Meta) — reprecificação em duas ondas**
- [FATO] Desde 01/07/2025 a Meta cobra por mensagem (template entregue), não mais por conversa de 24h — [Meta Developers: Pricing](https://developers.facebook.com/docs/whatsapp/pricing); [Twilio: aviso jul/2025](https://support.twilio.com/hc/en-us/articles/30304057900699-Notice-Changes-to-WhatsApp-s-Pricing-July-2025); [Zoho Community](https://help.zoho.com/portal/es/community/topic/whatsapp-pricing-changes-pay-per-message-starting-july-1-2025)
- [FATO] Twilio: quem envia vários templates de marketing/autenticação passa a pagar cada um separadamente — [Twilio changelog jun/2025](https://www.twilio.com/en-us/changelog/meta-is-updating-whatsapp-pricing-on-july-1--2025?afsrc=1)
- [FATO] A partir de 01/10/2026 a Meta passa a cobrar por mensagem **todas as mensagens de serviço** (respostas livres dentro da janela de 24h), gratuitas desde 01/11/2024; templates de utilidade dentro da janela voltam a ser cobrados — [ThisDay (ago/2026)](https://www.thisdaylive.com/2026/08/30/meta-to-charge-businesses-for-whatsapp-messages-from-october-1/); [Vonage: "Service Messages Become Billable on Oct 1 2026"](https://api.support.vonage.com/hc/en-us/articles/29982160922268-WhatsApp-Service-Messages-Become-Billable-on-Oct-1-2026-What-You-Need-to-Know); [Twilio: aviso out/2026](https://support.twilio.com/hc/en-us/articles/53100462475931-Notice-Changes-to-WhatsApp-s-Pricing-October-2026); [Meta: non-template messages](https://developers.facebook.com/documentation/business-messaging/whatsapp/pricing/non-template-messages/); [Omdia: "the WhatsApp free lunch is over"](https://omdia.tech.informa.com/om146764/the-whatsapp-free-lunch-is-over-and-meta-is-also-coming-for-the-ai-layer)
- [FATO] Meta Business Agent (IA) tem cobrança por tokens desde 01/08/2026; Meta pode revisar tarifas até trimestralmente; relato de que a Meta deixa de entregar mensagens de serviço de empresas sem forma de pagamento cadastrada — via resumo de busca sobre [Meta docs](https://developers.facebook.com/documentation/business-messaging/whatsapp/pricing/non-template-messages/) e [Zoho: Service Messages Will Be Charged Starting October 2026](https://help.zoho.com/portal/en/community/topic/whatsapp-business-platform-message-pricing-guide) (não consegui abrir a página da Meta para confirmar o texto literal).
- [FATO, conflito] Franquia gratuita: uma fonte fala em 1.000 respostas de serviço grátis/mês por número; outra diz que não há desconto por volume para serviço — fontes secundárias acima; **não resolvido**.
- [FATO] Brasil: marketing ≈ US$0,0718/msg, utilidade ≈ US$0,0078 (tabela vigente 01/01/2026) — [ManyChat Help](https://help.manychat.com/hc/en-us/articles/14281380243740); estimativa de R$130–180 por 1.000 msgs em mix médio — [MessageCentral (Brasil)](https://www.messagecentral.com/blog/whatsapp-business-api-pricing-in-brazil)
- [FATO] Template de confirmação de entrega categorizado erroneamente como marketing pode custar até 9x mais que como utilidade — resumo de guia de BSP ([SleekFlow](https://sleekflow.io/blog/whatsapp-business-price) / [Wati guide](https://www.wati.io/blog/whatsapp-api-pricing-guide)).
- [FATO] BSPs cobram taxa própria por cima da tarifa Meta ("custos escondidos") — [DEV: WhatsApp Business API Pricing Hidden Costs](https://dev.to/dipbhi/whatsapp-business-api-pricing-hidden-costs-what-your-first-bill-wont-tell-you-23bl)
- [FATO, via terceiro] Comentários de Reddit citados pela eesel: revendedor relata cliente com ~300k msgs de serviço/mês "sem palavras", já pagando ~US$1k/mês em templates; reclamação de aviso curto — [eesel: WhatsApp Business API pricing 2026](https://www.eesel.ai/blog/whatsapp-business-api-pricing) (não verificado no Reddit original).

**Google: remoção do parâmetro num=100 (set/2025) + AI Overviews**
- [FATO] Remoção do num=100 por volta de 10/09/2025; 87,7% de 319 propriedades perderam impressões no GSC; ferramentas de rank tracking passaram a precisar de ~10x mais requisições — [Search Engine Land: dados de impacto](https://searchengineland.com/google-num100-impact-data-462231); [SEJ](https://www.searchenginejournal.com/google-modifies-search-results-parameter-affecting-seo-tools/); [Practical Ecommerce: "Did Google just prevent rank tracking?"](https://www.practicalecommerce.com/did-google-just-prevent-rank-tracking); [BrightLocal](https://brightlocal.com/blog/google-updates-data-collection-a-rank-tracking-issues/)
- [FATO] AI Overviews: CTR por consulta cai 47,5% quando há AI Overview (Authoritas, enviado à CMA) — [Press Gazette](https://pressgazette.co.uk/platforms/google-search-clicks-traffic-2025-ai-overviews/); Pew: cliques caem de 15% para 8% — [NPR](https://www.npr.org/2025/07/31/nx-s1-5484118/google-ai-overview-online-publishers); [CJR "traffic apocalypse"](https://www.cjr.org/analysis/traffic-apocalypse-google-ai-overviews-killing-click-throughs-news-sites.php). Contraponto: Similarweb vê só −2,5% no tráfego orgânico do Google para top 40k sites nos EUA em 2025 (mesmo artigo da Press Gazette).

**Outras mudanças verificadas (provável descarte)**
- [FATO] Pocket encerrado em 08/07/2025 (export até 08/10/2025); Omnivore fechou ao ser adquirido pela ElevenLabs (fim de 2024) — [TechCrunch](https://techcrunch.com/2025/05/27/read-it-later-app-pocket-is-shutting-down-here-are-the-best-alternatives); [MacRumors forum](https://forums.macrumors.com/threads/omnivore-shutting-down.2441423); [wallabag](https://wallabag.org/news/20250524-pocket-shutdown/). Alternativas maduras: Instapaper, Readwise Reader, Matter, Raindrop, wallabag.
- [FATO] Instagram Basic Display API encerrada em 04/12/2024 — [Meta blog](https://developers.facebook.com/blog/post/2024/09/04/update-on-instagram-basic-display-api); [TechCrunch](https://techcrunch.com/2024/12/06/instagram-locks-out-developers-of-third-party-consumer-apps); feeds quebrados — [Bricks forum](https://forum.bricksbuilder.io/t/no-bug-instagram-feed-broken/28508). Já resolvido por Smash Balloon, Behold, WPZOOM, Spotlight — [Smash Balloon](https://smashballoon.com/instagram-is-shutting-down-basic-display-api-continue-displaying-instagram-feeds-on-your-site/); [Behold](https://behold.so/updates/basic-display-api-deprecated). Contas pessoais ficaram sem caminho oficial — [SpotlightWP](https://spotlightwp.com/instagram-basic-display-api-is-ending/).
- [FATO] Sites do Google Business Profile (business.site) desligados em mar/2024, redirecionamento até 10/06/2024; >21,7 milhões de sites criados — [Search Engine Land](https://searchengineland.com/google-business-profile-websites-are-now-redirected-to-google-maps-438154); [SE Roundtable](https://www.seroundtable.com/google-business-profiles-websites-now-shut-down-36999.html); [TechRadar](https://techradar.com/pro/google-is-shutting-down-websites-made-with-business-profiles). Mudança antiga (2024) e absorvida por construtores de site.
- [FATO] X API: Basic subiu de US$100 para US$200 (2024); pay-per-use em beta nov/2025, geral em 06/02/2026, teto de 3M leituras/mês; estimativa de US$575/mês para igualar o antigo Basic — [docs.x.com pricing](https://docs.x.com/x-api/getting-started/pricing); [TechCrunch](https://techcrunch.com/2025/10/21/x-is-testing-a-pay-per-use-pricing-model-for-its-api/?rand=324); [heise](https://heise.de/-11169806); [Open Terms Archive](https://opentermsarchive.org/en/memos/x-replaces-its-dollar200-entry-level-api-plan-with-a-pay-per-use-model/)
- [FATO] App Store EUA: decisão de 30/04/2025 permitiu links de pagamento externo sem comissão; em dez/2025 o 9º Circuito modificou a liminar permitindo a Apple cobrar alguma taxa ("reasonably necessary") — [TechCrunch](https://techcrunch.com/2025/05/02/apple-changes-us-app-store-rules-to-let-apps-redirect-users-to-their-own-websites-for-payments); [MacRumors dez/2025](https://www.macrumors.com/2025/12/11/apple-app-store-fees-external-payment-links/); [mjtsai](https://mjtsai.com/blog/2025/12/30/reasonably-necessary-external-purchase-fee/). Espaço já ocupado por Stripe, Paddle, RevenueCat, Adapty — [Paddle](https://www.paddle.com/blog/apple-vs-epic-app-store-changes); [Adapty](https://adapty.io/blog/new-us-ruling-on-external-ios-payments/).
- [FATO] Microsoft/Outlook passou a exigir SPF/DKIM/DMARC de remetentes >5.000 msgs/dia (a partir de 05/05/2025), com rejeição 550 5.7.515 — [Microsoft Tech Community](https://techcommunity.microsoft.com/blog/outlook/strengthening-email-security-outlook-new-requirements-for-high-volume-senders/4399730); [Microsoft Support NDR 550 5.7.515](https://support.microsoft.com/en-us/outlook/fix-ndr-error-550-5-7-515-in-outlook-com); [Red Sift](https://redsift.com/blog/microsoft-announces-new-email-requirements-for-bulk-senders)
- [FATO] European Accessibility Act aplicável desde 28/06/2025 a lojas que vendem a consumidores na UE, inclusive de fora da UE; overlays não garantem conformidade; isenção de microempresas é controversa — [Baymard](https://baymard.com/blog/european-accessibility-act-2025); [Bird & Bird](https://www.twobirds.com/en/insights/2025/a-guide-to-navigating-the-european-accessibility-act-for-online-retailers-service-providers-and-plat); [Practical Ecommerce](https://www.practicalecommerce.com/new-e-u-accessibility-act-impacts-global-merchants); [fudge.ai (Shopify)](https://www.fudge.ai/blog/european-accessibility-act-shopify/)

### Inferences
- [SUPOSIÇÃO] A mudança de out/2026 do WhatsApp transforma o atendimento (antes "grátis") em custo variável mensal para todo SMB que usa a API; como a tarifa varia por categoria, país e trimestre, há uma necessidade recorrente de monitorar e otimizar a fatura — e o Brasil é um dos maiores mercados de WhatsApp Business.
- [SUPOSIÇÃO] Pocket, Instagram Basic Display, GBP websites e App Store web checkout geram órfãos, mas a demanda já foi capturada por incumbentes bem avaliados → descartar.
- [SUPOSIÇÃO] X API: público órfão (indie devs/bots) é pequeno e de baixa disposição a pagar; descartar.

### Gaps
- Não verifiquei (por limite de tempo/chamadas): Skype (fim mai/2025), Zapier/Make reprecificação, Heroku, Mint, Glitch, Google Domains→Squarespace, Evernote, Reddit API, reversão de cookies do Chrome. Não devem ser citados sem nova verificação.
- Não consegui ler a página da Meta diretamente (host bloqueado); franquia grátis de 1.000 msgs de serviço é contraditória entre fontes.
- Não encontrei threads de Reddit originais sobre a conta do WhatsApp; só citações via eesel.

## 2. Novos hábitos (IA, custos de LLM, governança, criadores) e buscas crescentes com pouca oferta

### Takeaway
Os hábitos novos ligados a IA têm demanda clara, mas a oferta já explodiu: rastreamento de visibilidade em IA (GEO) está lotado e rastreamento de gasto de LLM está ficando lotado. Governança de "shadow AI" para pequenas empresas parece ter menos oferta (soluções são enterprise). As listas de tendências (Exploding Topics/Ahrefs) não revelaram termo SaaS claro com "pouca oferta".

### Cited Findings
**GEO / visibilidade em IA — lotado**
- [FATO] Roundups de 2026 listam 8–14+ ferramentas: Profound, Peec AI, Otterly.ai, AthenaHQ, Scrunch, Rankscale, Ahrefs Brand Radar, Semrush, SE Ranking etc. Preços: Otterly ~US$29/mês; Peec ~US$95–245/mês (€89 mín.); Profound enterprise US$499–2.000+/mês; Peec captou ~US$29M — [Rework: 12 plataformas AEO](https://resources.rework.com/tools/aeo-ai-visibility/best-aeo-tools-2026); [SE Ranking: alternativas ao Profound](https://seranking.com/blog/profound-alternatives/); [Superlines comparativo](https://www.superlines.io/articles/best-ai-visibility-tools); [getairefs: 14 AEO tools](https://getairefs.com/blog/best-aeo-tools/)

**Custo de API de LLM por cliente/feature — dor real, oferta crescente**
- [FATO] Relatos: usuário intensivo custou US$500 numa noite; conta Gemini saltou de centenas para US$6.000+ num mês sem detalhamento; API de uso da OpenAI só dá agregados, sem atribuição por cliente/feature — [DEV: per-customer LLM costs](https://dev.to/amedinat/how-i-track-per-customer-llm-costs-in-production-4l2l); [DEV: stop one customer blowing up budget](https://dev.to/amedinat/how-to-stop-one-customer-from-blowing-up-your-entire-llm-budget-4mac); [DEV: cost attribution per request](https://dev.to/sol_causely/llm-cost-attribution-per-request-how-to-track-openai-and-anthropic-spend-by-team-and-feature-1i8b); [Indie Hackers: 6 meses rastreando chamadas de IA](https://www.indiehackers.com/post/we-tracked-every-ai-api-call-for-6-months-90-of-alerts-fired-between-2-5-am-00419012ba)
- [FATO] Concorrentes citados: LiteLLM, Langfuse, Helicone, LLMeter (open source), StackSpend, Pingoni — mesmas fontes; [DEV: Pingoni](https://dev.to/silentishim/introducing-llm-cost-tracking-in-pingoni-see-your-openai-spend-per-user-in-5-minutes-43ch). Obs.: grande parte dos posts é de autores vendendo a própria ferramenta (viés).

**Shadow AI / governança de IA em empresas pequenas**
- [FATO] Cybernews (ago/2025, 1.000+ trabalhadores EUA): 59% usam IA não aprovada; 23% dos empregadores sem política formal — [SecurityWeek](https://www.securityweek.com/the-shadow-ai-surge-study-finds-50-of-workers-use-unapproved-ai-tools/); Harmonic: 45% dos prompts com dados via contas pessoais — mesmo conjunto de resultados; MIT NANDA: uso de ChatGPT/Claude pessoal mesmo sem licença — [Fortune](https://fortune.com/2025/08/19/shadow-ai-economy-mit-study-genai-divide-llm-chatbots/); quase metade já subiu dados sensíveis em chats de IA — [ClickOnDetroit (jan/2026)](https://www.clickondetroit.com/news/local/2026/01/12/shadow-ai-nearly-half-of-employees-say-theyve-uploaded-sensitive-data-into-ai-chats); custos de ferramentas não aprovadas — [Journal of Accountancy (nov/2025)](https://www.journalofaccountancy.com/news/2025/nov/lurking-in-the-shadows-the-costs-of-unapproved-ai-tools/)
- [FATO] Nenhum survey focado em SMB foi encontrado; PagerDuty 2026 cobre só empresas >US$500M — resultados da busca (lacuna).

**Tendências de busca**
- [FATO] Exploding Topics (software, atualizado 04/11/2026): ActiveCampaign +106%, Knowify +67%; versão de 17/10/2026: Waitlist Me +1.100%, VR Jobs +960%, Drata +733% — [Exploding Topics software topics](https://explodingtopics.com/software-topics); Ahrefs (out/2026): lemlist +180%, Dental Intelligence +150%, Manychat +120% em buscas de marca — [Ahrefs](https://ahrefs.com/blog/fastest-growing-companies-and-startups/)

### Inferences
- [SUPOSIÇÃO] Manychat (+120%) e o próprio aumento de custo do WhatsApp sugerem que automação de mensageria conversacional segue em alta — reforça o candidato WhatsApp.
- [SUPOSIÇÃO] Drata (+733%) indica demanda crescente por compliance automatizado; conversa com a dor de acessibilidade (EAA) e governança de IA.
- [SUPOSIÇÃO] GEO: não entrar como "mais um tracker". LLM cost: só como nicho vertical (ex.: agências que revendem IA), não horizontal.

### Gaps
- Não obtive dados de Google Trends/Glimpse diretamente (sem acesso à ferramenta); "buscas crescentes com pouca oferta" ficaram sem evidência quantitativa forte.
- Sem dados sobre hábitos de criadores/vídeo curto nesta rodada.

## 3. Candidatos de dor (4–6), concorrentes e notas

### Takeaway
Ranking final: (1) **Controle/auditoria de custo do WhatsApp API para PMEs e agências (foco Brasil/LatAm)** — melhor combinação de timing (out/2026), recorrência e baixa concorrência específica; (2) **Kit de conformidade EAA para pequenos e-commerces** — regulatório, recorrente, mas com concorrência de overlays e sem evidência de Reddit; (3) **Governança de IA "lite" para PMEs**; (4) **Relatórios de "por que meu tráfego caiu" para agências de SEO (pós AI Overviews + num=100)**; (5) **Custo de LLM por cliente** (rebaixado, lotado); GEO tracker e DMARC (descartados, lotados).

### Cited Findings (concorrentes por candidato)

**C1 — WhatsApp API: monitor de custo, alertas e auditoria de categoria de template**
- Persona: PME/e-commerce/clínica que usa WhatsApp API via BSP; agências que gerenciam vários números. Frequência: mensal (fatura) e diária (envios). Como lidam hoje: planilhas e dashboards do próprio BSP/WhatsApp Manager [SUPOSIÇÃO].
- Evidência (≥3): [Meta docs](https://developers.facebook.com/documentation/business-messaging/whatsapp/pricing/non-template-messages/); [Twilio out/2026](https://support.twilio.com/hc/en-us/articles/53100462475931-Notice-Changes-to-WhatsApp-s-Pricing-October-2026); [Vonage](https://api.support.vonage.com/hc/en-us/articles/29982160922268-WhatsApp-Service-Messages-Become-Billable-on-Oct-1-2026-What-You-Need-to-Know); [Omdia](https://omdia.tech.informa.com/om146764/the-whatsapp-free-lunch-is-over-and-meta-is-also-coming-for-the-ai-layer); [eesel (Reddit citado)](https://www.eesel.ai/blog/whatsapp-business-api-pricing); [DEV hidden costs](https://dev.to/dipbhi/whatsapp-business-api-pricing-hidden-costs-what-your-first-bill-wont-tell-you-23bl)
- Concorrentes: BSPs (Wati, SleekFlow, Zenvia, Twilio, Zoho, ManyChat) oferecem analytics dentro da própria plataforma — [Wati guide](https://www.wati.io/blog/whatsapp-api-pricing-guide); [SleekFlow](https://sleekflow.io/blog/whatsapp-business-price). A busca **não encontrou** produto independente dedicado a análise/otimização de custo multi-BSP (lacuna de oferta, mas também pode indicar que BSPs resolvem "bem o bastante") [SUPOSIÇÃO].
- Riscos [SUPOSIÇÃO]: dependência de API da Meta/BSP para dados de cobrança; BSPs podem copiar a feature; Meta muda regras trimestralmente (bom para recorrência, ruim para manutenção).

**C2 — Conformidade EAA (acessibilidade) contínua para pequenos e-commerces (Shopify/WooCommerce)**
- Evidência: [Baymard](https://baymard.com/blog/european-accessibility-act-2025); [Bird & Bird](https://www.twobirds.com/en/insights/2025/a-guide-to-navigating-the-european-accessibility-act-for-online-retailers-service-providers-and-plat); [Practical Ecommerce](https://www.practicalecommerce.com/new-e-u-accessibility-act-impacts-global-merchants); [fudge.ai](https://www.fudge.ai/blog/european-accessibility-act-shopify/); [Sharetribe (marketplaces)](https://www.sharetribe.com/academy/european-accessibility-act-for-online-marketplaces/)
- Concorrentes: Siteimprove, UsableNet, Accessibility.Works, accessiBe/UserWay (overlays, criticados como insuficientes), fudge.ai, Consentmo — [Siteimprove](https://www.siteimprove.com/blog/european-accessibility-act-e-commerce/); [accessibility.works](https://www.accessibility.works/blog/eaa-en301549-compliance-european-accessibility-act/); [Consentmo](https://www.consentmo.com/blog-posts/eaa-compliance-what-online-stores-must-do-before-june-2025). Preços não verificados nesta rodada.
- Fraqueza: nenhuma thread de Reddit encontrada; evidência majoritariamente de fornecedores (viés comercial). Multas citadas variam (€60k vs €100k) — fontes secundárias.

**C3 — Governança de IA "lite" para PMEs (política, inventário de ferramentas, treinamento, registro de uso)**
- Evidência: [SecurityWeek/Cybernews](https://www.securityweek.com/the-shadow-ai-surge-study-finds-50-of-workers-use-unapproved-ai-tools/); [Fortune/MIT](https://fortune.com/2025/08/19/shadow-ai-economy-mit-study-genai-divide-llm-chatbots/); [Journal of Accountancy](https://www.journalofaccountancy.com/news/2025/nov/lurking-in-the-shadows-the-costs-of-unapproved-ai-tools/); [TechRadar](https://www.techradar.com/pro/businesses-are-losing-control-of-ai-and-bosses-are-starting-to-despair); [ClickOnDetroit](https://www.clickondetroit.com/news/local/2026/01/12/shadow-ai-nearly-half-of-employees-say-theyve-uploaded-sensitive-data-into-ai-chats)
- Concorrentes: Harmonic, ManageEngine (enterprise), Drata/Vanta (compliance, tendência +733% Drata) — [ManageEngine PDF](https://download.manageengine.com/pdf/shadow-ai-surge-enterprises.pdf); [Exploding Topics](https://explodingtopics.com/software-topics). Oferta SMB específica não verificada (lacuna).
- Fraqueza: evidência é de surveys gerais, não de PMEs pedindo/pagando por solução.

**C4 — Relatórios explicativos de queda de tráfego para agências SEO (AI Overviews + num=100)**
- Evidência: [Search Engine Land num=100](https://searchengineland.com/google-num100-impact-data-462231); [Search Engine Land: "SEO reporting black box era"](https://searchengineland.com/seo-reporting-black-box-era-463461); [Press Gazette](https://pressgazette.co.uk/platforms/google-search-clicks-traffic-2025-ai-overviews/); [Practical Ecommerce](https://www.practicalecommerce.com/did-google-just-prevent-rank-tracking)
- Concorrentes: Semrush (Position Tracking com AI Overview), Ahrefs, BrightLocal, Botify, AgencyAnalytics, além dos trackers GEO — [Botify](https://www.botify.com/blog/googles-removes-num-100); [BrightLocal](https://brightlocal.com/blog/google-updates-data-collection-a-rank-tracking-issues/). Espaço denso → rebaixado.

**C5 — Atribuição de custo de LLM por cliente/feature (rebaixado)**
- Evidência: links da seção 2. Concorrentes: Helicone, Langfuse, LiteLLM, LLMeter, StackSpend, Pingoni (muitos, inclusive open source gratuito) → lotado.

**Descartados**: GEO tracker (≥12 concorrentes financiados); DMARC/entregabilidade (EasyDMARC, dmarcian, Valimail, Red Sift, PowerDMARC — [Valimail](https://www.valimail.com/?p=10655), [Red Sift](https://redsift.com/blog/microsoft-announces-new-email-requirements-for-bulk-senders)); Pocket/Omnivore; Instagram feed; GBP websites; X API; checkout web iOS.

### Notas (0–10) — [SUPOSIÇÃO: julgamento do pesquisador]

| Critério | C1 WhatsApp custo | C2 EAA e-commerce | C3 Governança IA PME | C4 Relatório SEO | C5 Custo LLM |
|---|---|---|---|---|---|
| Recorrência | 9 | 7 | 6 | 8 | 9 |
| Disposição a pagar | 7 | 7 | 5 | 6 | 6 |
| Fit assinatura | 9 | 8 | 7 | 8 | 8 |
| Baixa concorrência | 7 | 4 | 6 | 3 | 2 |
| Tamanho de mercado | 8 | 6 | 7 | 6 | 6 |
| Retenção/lock-in | 7 | 6 | 5 | 6 | 7 |
| Construível em semanas | 6 (depende de acesso a dados de cobrança via BSP/Meta) | 6 | 8 | 6 | 8 |
| Velocidade p/ 1º pagante | 7 | 5 | 5 | 6 | 6 |
| Ticket mensal possível | US$29–199 (PME) / US$300+ (agência) | US$29–149 | US$49–199 | US$49–299 | US$29–199 |

### Inferences
- [SUPOSIÇÃO] C1 é o candidato mais forte: mudança de 01/10/2026 é recentíssima (≈7 semanas), afeta toda empresa com atendimento via API, tem regras complexas (categoria × país × janela × trimestre) e o Brasil é mercado grande. Validar rapidamente com 10 entrevistas de agências/BSPs brasileiras.
- [SUPOSIÇÃO] C2 pode virar "auditoria contínua + relatório de conformidade" por loja; diferencial seria não ser overlay.

### Gaps
- Preços dos concorrentes de C2/C3 não verificados.
- Sem evidência direta (Reddit/HN) de PMEs reclamando da fatura do WhatsApp pós-out/2026 — tempo curto desde a mudança; buscar em grupos BR (Reddit r/brdev, fóruns de BSPs) numa próxima rodada.
- Não verifiquei se WhatsApp Manager/BSPs já oferecem alertas de orçamento por categoria — ponto crítico para C1.
