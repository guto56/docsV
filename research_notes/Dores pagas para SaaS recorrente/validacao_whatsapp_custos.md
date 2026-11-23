# Validação: SaaS independente de monitoramento e auditoria de custos da API do WhatsApp Business (Cloud API) para PMEs e agências, Brasil/LatAm

> Data da pesquisa: 23/11/2026. Limitação importante: nesta sessão o WebFetch não alcançou developers.facebook.com, reclameaqui.com.br, respond.io, whapi.cloud nem crminer.com.br (erro de DNS no ambiente). Por isso, quase todos os achados vêm de **trechos de resultados de busca**, não da leitura completa das páginas. Valores e datas precisam ser conferidos na tabela oficial da Meta antes de entrar em pitch ou cálculo financeiro.
> Convenção: "Achados citados" = fato com URL; "Inferências" = minha análise e premissas, sem fonte direta.

## 1. Mudanças de preço da Meta em 2025–2026 e tarifas do Brasil

### Takeaway
Confirmado por várias fontes secundárias: a cobrança passou a ser **por mensagem de template entregue** em 01/07/2025. Em **01/10/2026** a Meta voltou a cobrar as mensagens de serviço (respostas livres dentro da janela de 24h), com franquia de 1.000 mensagens por número por mês. Também em 2026 houve migração para faturamento em BRL e cobrança por token do Business Agent. Com isso, o custo ficou mais granular e mais difícil de prever, o que é o gatilho de dor que a ideia precisa.

### Achados citados
- A cobrança por mensagem vale desde 01/07/2025 ("effective July 1, 2025, it charges on a per-message basis"), segundo a documentação da Meta citada em busca — [Meta Pricing](https://developers.facebook.com/documentation/business-messaging/whatsapp/pricing); [Gulf News](https://gulfnews.com/technology/whatsapp-announces-pricing-update-to-charge-per-message-on-business-platform-1.500142961)
- Exemplo de cobrança: um template de marketing seguido de dois de utilidade gera 3 cobranças. Templates de utilidade enviados dentro da janela de serviço eram gratuitos até 30/09/2026 — [Gulf News](https://gulfnews.com/technology/whatsapp-announces-pricing-update-to-charge-per-message-on-business-platform-1.500142961)
- Mensagens de serviço foram gratuitas de cerca de nov/2024 até set/2026. Desde **01/10/2026** são cobradas pela tarifa de utilidade/autenticação do país, com franquia de **1.000 mensagens de serviço grátis por número por mês**. O pricing type de utility dentro da janela mudou de `free_customer_service` para `regular` — [Wati blog](https://www.wati.io/en/blog/whatsapp-service-message-pricing/); [Chakra](https://chakrahq.com/article/whatsapp-api-pricing-update-service-messages-october-2026); [EngageLab](https://www.engagelab.com/blog/whatsapp-pricing-2026-service-message-cost); [DEV.to](https://dev.to/abhijeet_singh_4577af3ef9/whatsapp-service-message-pricing-what-changes-october-1-2026-3ngl); [Zenvia](https://zenvia.com/en/new-whatsapp-business-pricing-rules-for-2026/); [Digisac](https://digisac.com.br/blog/preco-whatsapp-api-outubro-2026)
- A mudança de 01/10/2026 não se aplica a AI Providers. Governos e ONGs elegíveis têm política própria até 31/12/2027 — [Wati blog](https://www.wati.io/en/blog/whatsapp-service-message-pricing/) (trecho de busca, não verificado na Meta)
- Números hospedados em BSP: há relatos de que passam a depender de saldo pré-pago no WhatsApp, mas as fontes divergem sobre o bloqueio quando o saldo chega a zero — [respond.io](https://respond.io/blog/whatsapp-pricing-change-2026); divergência citada em [EngageLab](https://www.engagelab.com/blog/whatsapp-pricing-2026-service-message-cost)
- Desde 01/08/2026, as mensagens do Meta Business Agent são cobradas por token, a US$ 2,00 por 1 milhão de tokens — trecho de busca, fonte agregada ([Wati blog "two new fees"](https://www.wati.io/en/blog/whatsapp-business-api-pricing-changes-2026-what-meta-s-two-new-fees-actually-cost-you/))
- **Brasil**, segundo fontes secundárias: marketing por cerca de **R$ 0,32/msg** (US$ 0,0625) e utilidade, autenticação e serviço por cerca de **R$ 0,035/msg** (US$ 0,0068). Contas brasileiras elegíveis migraram para faturamento em BRL a partir de 01/07/2026, com prazo final em 30/06/2027. Uma fonte destoa e cita marketing a R$ 0,38 e utilidade a R$ 0,04 — [Message Central](https://www.messagecentral.com/blog/whatsapp-business-api-pricing-brazil); [Whautomate](https://whautomate.com/whatsapp-business-api-pricing-brazil); [Vectalk](https://vectalk.com.br/blog/en/whatsapp-api-pricing-brazil/); [CRMiner (out/2026)](https://www.crminer.com.br/en/blog/whatsapp-business-api-cobranca-outubro-2026); [FlowCall (nov/2026)](https://www.flowcall.co/blog/whatsapp-business-api-pricing)
- Um comparativo brasileiro cita R$ 0,3217 por mensagem de marketing — [Modo Fluxo](https://modofluxo.com.br/blog/preco-da-api-do-whatsapp-em-6-provedores-custo-real-de-1000-mensagens)
- Desde 09/04/2025, um template enviado como Utility que a Meta considere Marketing é **aprovado como Marketing** e cobrado como tal. Existe o webhook `template_category_update` e prazo de 60 dias para pedir revisão — [Meta – Template categorization](https://developers.facebook.com/documentation/business-messaging/whatsapp/templates/template-categorization); [Meta – webhook](https://developers.facebook.com/documentation/business-messaging/whatsapp/webhooks/reference/template_category_update/); [Wati – boas práticas de reclassificação](https://support.wati.io/en/articles/15932488-best-practices-to-reduce-whatsapp-utility-to-marketing-template-reclassification)
- A partir de 01/12/2025, o lookback das analytics de mensagens, conversas e preço caiu de 10 anos para 1 ano. O de templates continua em 90 dias — [Meta Analytics](https://developers.facebook.com/documentation/business-messaging/whatsapp/analytics)
- A Cloud API não retorna preço na resposta de envio. Quem quer controle por mensagem precisa estimar e depois reconciliar — [laravel-whatsapp-cost-control (README)](https://packagist.org/packages/dineshstack/laravel-whatsapp-cost-control)

### Inferências
- A mudança de 01/10/2026 é o melhor "momento de dor": empresas de atendimento com alto volume de respostas, que antes tinham custo zero nessas respostas, passam a pagar cerca de R$ 0,035 por mensagem acima de 1.000. Por exemplo, 100 mil respostas por mês dariam cerca de R$ 3,4 mil por número. A conta é ilustrativa e usa a tarifa secundária.
- Com a janela de 90 dias para templates e de 1 ano para preço, há espaço para um produto que **guarde o histórico** e reconcilie os dados.

### Lacunas
- Não consegui ler a tabela oficial de tarifas da Meta, com o CSV por país (o domínio estava bloqueado). As tarifas do Brasil são de fontes secundárias e divergem entre si.
- Não confirmei se houve nova revisão de tarifas do Brasil em out/2026. Uma fonte diz que Brasil e outros mercados não mudaram na última atualização.
- Os tiers de volume para utilidade/autenticação no Brasil (descontos por volume) não foram confirmados.

## 2. Os BSPs já oferecem breakdown por template, alertas de orçamento, alerta de reclassificação e custo por campanha?

### Takeaway
Parcialmente, sim, e de forma crescente. A própria Meta já mostra custo por template entregue, tem API de pricing analytics, webhook de reclassificação e, para a Marketing Messages API, teto de preço e orçamentos diários/vitalícios. SleekFlow tem limite de gasto mensal com alertas em 70/90/100%. Kommo mostra custo por template e custo por clique. A lacuna real é estreita: **visão consolidada e independente entre vários WABAs/BSPs, auditoria do markup do BSP versus a tarifa da Meta e alertas proativos de reclassificação ligados ao impacto em R$**, sobretudo para agências.

### Achados citados
- **Meta (nativo)**: o Template Insights mostra o custo por mensagem entregue. A Marketing Messages API tem "max price" por mensagem (beta) e `daily_budget`/`lifetime_budget` para limitar gasto de campanha. O campo `conversation_analytics`/pricing analytics da Business Management API traz custo por WABA — [Meta – MM pricing](https://developers.facebook.com/documentation/business-messaging/whatsapp/marketing-messages/pricing); [Meta – view metrics](https://developers.facebook.com/documentation/business-messaging/whatsapp/marketing-messages/view-metrics/); [Meta – BM API analytics](https://developers.secure.facebook.com/docs/whatsapp/business-management-api/analytics)
- **SleekFlow**: limite de gasto mensal de mensagens WhatsApp na página de Billing. O indicador muda em 70%, 90% e 100% e bloqueia envios ao atingir o limite. O artigo foi atualizado em out/2026 — [SleekFlow Help](https://help.sleekflow.io/en_US/setting-a-monthly-message-spend-limit-for-whatsapp)
- **Kommo**: analytics de WhatsApp com custo por template (total gasto, custo por mensagem entregue e custo por clique quando há botão URL) — [Kommo Support](https://www.kommo.com/support/messenger-apps/whatsapp-analytics)
- **Spur**: visão de custo total por país no período, na moeda de faturamento — [Spur Help](https://help.spurnow.com/en/articles/12595095-how-to-use-whatsapp-analytics-quick-links)
- **Wati**: tem guias de otimização de custo, calculadora de preço, campaign analytics e URL tracking. Não confirmei um relatório de custo por template. Cobra por wallet pré-paga, com tarifa por mensagem acima da tabela Meta segundo análise independente — [Wati Support](https://support.wati.io/en/articles/11660815-how-to-optimize-your-messaging-costs-with-the-new-message-based-pricing); [Wati calculadora](https://www.wati.io/whatsapp-business-api-pricing-calculator); [eesel.ai – Wati pricing](https://www.eesel.ai/blog/wati-pricing)
- **Digisac**: tem um simulador de custos de WhatsApp (pré-venda, não monitoramento) — [Digisac simulador](https://www.digisac.com.br/conteudos/simulador-de-custos-whatsapp)
- **respond.io**: calculadora de custo mensal (pré-venda) — [respond.io calculator](https://respond.io/whatsapp-pricing-calculator)
- **Chakra**: diz que analytics básicas de template são grátis e que dashboards avançados custam US$ 10–50/mês (afirmação de vendor, não verificada) — [Chakra Help](https://chakrahq.com/help/learning-centre/whatsapp-business-api/insights-reporting)
- **Mapa de preços dos BSPs (fontes secundárias, inconsistentes)**:
  - **Zenvia**: mensalidade a partir de cerca de R$ 600 mais tarifa por template de R$ 0,47–0,55, e R$ 0,069 por resposta de serviço. Há também um plano Starter com software a R$ 0 e pacote de canais a partir de R$ 100/mês — [Nação Digital](https://nacao.digital/blog/whatsapp-business-api/); [Modo Fluxo](https://modofluxo.com.br/blog/preco-da-api-do-whatsapp-em-6-provedores-custo-real-de-1000-mensagens)
  - **Blip**: sob cotação. Conversa excedente de cerca de R$ 1,40 no plano Plus (relato) — [Tenessi Hub](https://www.tenessihub.com.br/seo/take-blip-vs-zenvia/); [Modo Fluxo](https://modofluxo.com.br/blog/preco-da-api-do-whatsapp-em-6-provedores-custo-real-de-1000-mensagens)
  - **Wati**: cerca de US$ 29/usuário/mês (Growth anual) ou R$ 299/mês para IP brasileiro. Markup de cerca de 25% sobre a Meta segundo um comparativo — [Nação Digital](https://nacao.digital/blog/whatsapp-business-api/); [eesel.ai](https://www.eesel.ai/blog/wati-pricing)
  - **respond.io**: a partir de US$ 99/mês — [eesel/busca](https://www.eesel.ai/blog/wati-pricing) (trecho)
  - **Digisac**: a partir de R$ 99/mês, sem incluir o custo das mensagens da Meta — [Digisac blog](https://digisac.com.br/blog/quanto-custa-um-chatbot-para-whatsapp-e-como-calcular-o-retorno)
  - **AiSensy**: diz não cobrar markup pelo acesso à API — [AiSensy preços](https://aisensy.com/pt/planos-e-precos)
  - **Markups comparados** (tabela de um concorrente, 360dialog): de cerca de +2,4% (Gupshup) a cerca de +161,5% (Vonage) no mesmo volume — [360dialog blog](https://360dialog.com/blog/?p=1403)
- Um vendor (Whapi.Cloud) afirma que o markup dos BSPs adiciona 15–20% "invisível" sobre a tarifa Meta — [Whapi.Cloud](https://whapi.cloud/blog/whatsapp-bsp-pricing-hidden-costs-2026)

### Inferências
- Quem está na Cloud API direta (pagando a Meta) já tem dados nativos razoáveis. O valor incremental de um SaaS está em (a) multi-WABA e multi-cliente para agências, (b) alertas proativos e previsão, (c) reconciliação entre a fatura do BSP e a tabela Meta e (d) custo por campanha/conversão integrado ao CRM.
- Os BSPs têm incentivo **contra** a transparência do markup. Uma auditoria independente seria um diferencial, mas o acesso aos dados de quem está atrás de BSP é difícil: muitos BSPs não expõem a WABA ou o token ao cliente.
- O risco é a Meta e os BSPs maiores fecharem a lacuna. SleekFlow e Kommo já fizeram parte disso, e a Meta lançou orçamentos para a MM API.

### Lacunas
- Não verifiquei as páginas de features de Zenvia, Blip, Twilio, Gupshup, 360dialog, Z-API, ManyChat, Botconversa e Digisac quanto a breakdown e alertas: a busca não retornou páginas específicas e o fetch estava bloqueado.
- Z-API e Botconversa usam majoritariamente API não oficial ou modelo diferente. Não encontrei preços nem relevância para custo Meta.
- Não confirmei se algum BSP brasileiro alerta sobre reclassificação de template com impacto financeiro.

## 3. Ferramentas standalone de análise e otimização de custo do WhatsApp

### Takeaway
Praticamente inexistentes. O único achado direto é um pacote Laravel open source minúsculo (cerca de 4 stars, 6 installs) e templates de n8n/AWS. Nada no Product Hunt ou na Chrome Web Store foi encontrado. Isso indica um espaço vazio, mas também pode indicar demanda pequena ou que a dor é resolvida dentro do BSP.

### Achados citados
- **laravel-whatsapp-cost-control**: tracking de custo por mensagem, rate cards por país, caps de gasto (bloqueia marketing e nunca bloqueia transacional), alertas e audit log. Tem cerca de 4 stars no GitHub e 6 installs — [Packagist](https://packagist.org/packages/dineshstack/laravel-whatsapp-cost-control)
- Padrão AWS: integrar o AWS Budgets com alertas via WhatsApp (é FinOps de AWS, não custo de WhatsApp) — [AWS Blog](https://aws.amazon.com/blogs/messaging-and-targeting/establishing-finops-management-integrating-aws-budgets-with-whatsapp-using-aws-end-user-messaging)
- Existe um workflow n8n relacionado (conteúdo não verificado) — [n8n workflow 21896](https://n8n.io/workflows/21896)
- Calculadoras de pré-venda (respond.io, Wati, Digisac) não fazem monitoramento contínuo — [respond.io](https://respond.io/whatsapp-pricing-calculator); [Wati](https://www.wati.io/whatsapp-business-api-pricing-calculator); [Digisac](https://www.digisac.com.br/conteudos/simulador-de-custos-whatsapp)

### Inferências
- A ausência de concorrentes standalone tem duas leituras: oportunidade ou falta de demanda paga. O fato de o único player ser um pacote hobby sugere que devs resolvem in-house e PMEs não procuram ferramenta separada.

### Lacunas
- Não fiz busca direta no Product Hunt, na Chrome Web Store nem no GitHub search (sem acesso). Recomenda-se a checagem manual.

## 4. Reclamações em primeira pessoa sobre contas surpresa ou markup de BSP

### Takeaway
Há evidência, mas moderada. No Reclame Aqui, "cobrança indevida" é a principal categoria de reclamação da Zenvia (34,15%), e um cliente da Blip contesta uma fatura de cerca de R$ 31,5 mil de mensagens de marketing/utilidade, alegando taxa por mensagem do BSP. A maioria das reclamações da Zenvia, porém, é sobre cancelamento ou contrato, não sobre custo de mensagem. Não encontrei threads do Reddit. No Hacker News há comentários sobre marketing mais caro após jul/2025.

### Achados citados
- **Blip (Reclame Aqui)**: cliente contesta fatura de cerca de R$ 31.500 de mensagens de marketing e utilidade. Alega que a Blip cobra por mensagem "mesmo a Meta não cobrando mais" esse valor e adiciona tarifa a cada envio ativo — [Reclame Aqui – Blip](https://www.reclameaqui.com.br/take-blip/cobranca-abusiva-e-falta-de-retorno-da-blip-sobre-fatura-de-r-31500_QgPFNkXwvxrgRr5B/) (lido via trecho de busca)
- **Blip**: cobrança de serviço não contratado, com boletos vinculados ao CNPJ — [Reclame Aqui](https://www.reclameaqui.com.br/take-blip/cobranca-indevida-de-servico-nao-contratado-e-nao-utilizado-com-boletos-vencidos-vinculados-ao-cnpj_ssaJXw2hPTfEWfTl/)
- **Zenvia**: "cobrança indevida" é a maior categoria de reclamação (34,15%). A nota média é 8,9/10 nos últimos 6 meses — [Reclame Aqui – Zenvia](https://www.reclameaqui.com.br/empresa/zenvia/)
- **Zenvia**: ignora cancelamento, cobra indevidamente e ameaça protesto — [Reclame Aqui](https://www.reclameaqui.com.br/zenvia/zenvia-ignora-cancelamento-cobra-indevidamente-e-ameaca-protesto-e-cobranca-judicial_PkSx89KIiThW2Nd2/)
- **Zenvia**: não emite notas fiscais de recargas desde maio/2026 — [Reclame Aqui](https://www.reclameaqui.com.br/zenvia/zenvia-nao-emite-notas-fiscais-de-recargas-desde-maio-de-2026-apesar-das-tentativas-de-contato_tbUcGAt9i_CqEyzB/)
- **Huggy**: cobrança indevida sem ativação do WhatsApp Business — [Reclame Aqui](https://www.reclameaqui.com.br/huggy/cobranca-indevida-e-nao-ativacao-do-whatsapp-business_aXdvBkCz5_tejhZs/)
- **SendPulse Brasil**: dificuldade de estorno de créditos — [Reclame Aqui](https://www.reclameaqui.com.br/sendpulse-brasil/cobrancas-indevidas-e-dificuldades-no-estorno-de-creditos-de-chatbot__uyQtI1XAPsZcjCu/)
- **Hacker News**: discussão "what's free and where markup hides". Um comentário diz que a mudança de jul/2025 tornou o marketing "way pricier" — [HN](https://news.ycombinator.com/item?id=48504753)
- **Reclassificação** utility→marketing descrita como "a surpresa de fatura mais reportada", com anedota de conta de 80 mil msgs/mês cuja fatura triplicou em um ciclo (fonte vendor e anedótica) — [Whapi.Cloud](https://whapi.cloud/blog/whatsapp-bsp-pricing-hidden-costs-2026)
- Guia de "custos ocultos na primeira fatura" (DEV.to, conteúdo de autor/vendor) — [DEV.to](https://dev.to/dipbhi/whatsapp-business-api-pricing-hidden-costs-what-your-first-bill-wont-tell-you-23bl)
- Vários BSPs publicam artigos de suporte sobre "meu template utility virou marketing", o que indica volume de tickets: [MSG91](https://msg91.com/help/whatsapp/whatsapp-template-category-changed-from-utility-to-marketing--solution); [Graphy](https://graphy804657060717855613.freshdesk.com/support/solutions/articles/1060000150214-why-did-my-utility-template-automatically-got-changed-to-marketing-template-); [Exotel](https://support.exotel.com/support/solutions/articles/3000120232-how-do-i-raise-an-appeal-to-re-categorize-my-existing-whatsapp-templates-); [Qiscus](https://support.qiscus.com/hc/en-us/articles/1747210550039-How-to-Appeal-a-WhatsApp-Template-Category)

### Inferências
- Há mais de 3 links independentes, mas a dor documentada no Brasil é mais "**relação comercial / cobrança contestada com BSP**" do que "não sei quanto estou gastando". Isso sustenta o ângulo de **auditoria de fatura do BSP**, não o de dashboard.
- Os artigos de suporte sobre reclassificação são um sinal indireto forte de dor recorrente, mas o BSP já responde com conteúdo grátis.

### Lacunas
- Não encontrei threads do Reddit nem posts do LinkedIn em primeira pessoa (a busca não retornou nenhum).
- Não consegui ler os textos completos do Reclame Aqui (domínio bloqueado no fetch). Os detalhes vêm de resumos dos trechos.
- Não encontrei reclamações sobre Wati, Z-API ou Kommo.

## 5. Tamanho de mercado: usuários da API no Brasil, agências e revendedores BSP

### Takeaway
Não há número oficial confiável de empresas brasileiras na **API** (versus o app Business). Os números circulantes (cerca de 5 milhões de empresas BR no WhatsApp Business, 200 milhões no app no mundo, mais de 15 milhões na API no mundo) são de blogs e misturam app e API. O TAM do nicho "monitoramento de custo" precisa ser estimado bottom-up.

### Achados citados
- Mais de 5 milhões de empresas no Brasil usariam "alguma versão" do WhatsApp Business (blog/consultoria, sem separar a API) — [AiSensy PT](https://m.aisensy.com/blog/pt/whatsapp-para-empresas/); [Mind Group](https://mindconsulting.com.br/2026/04/whatsapp-business-api-pme-empresario-2026/)
- 200 milhões de empresas usam o app WhatsApp Business no mundo (cita a Meta Newsroom via blog) — [Nexamind](https://www.nexamind.com.br/blog/whatsapp-business-api-novidades-2026)
- Mais de 15 milhões de empresas na API no mundo, com fonte "dados de parceiros BSP" (não verificável) — [SocialHub](https://www.socialhub.pro/blog/50-estatisticas-whatsapp-business-2026/)
- Listas de BSPs no Brasil citam Zenvia, Blip, Twilio, Sinch, Infobip, 360dialog, Gupshup, YCloud e outros. São listas de vendors, sem contagem oficial — [YCloud](https://www.ycloud.com/pt/blog/top-whatsapp-business-api-solution-providers-brazil); [AiSensy – Top 20 BR](https://m.aisensy.com/blog/pt/top-provedores-whatsapp-business-api/)
- A Meta distingue Tech Providers, Tech Partners e Solution Partners — [WhatsApp Business – parceiros](https://whatsappbusiness.com/pt-br/partners/become-a-partner/)

### Inferências (premissas, sem fonte)
- Se 1–3% das cerca de 5 milhões de empresas usarem a API oficial, seriam de 50 mil a 150 mil contas WABA no Brasil. Destas, talvez 10–20% tenham gasto suficiente (acima de R$ 2 mil/mês) para justificar uma ferramenta de custo, ou seja, de 5 mil a 30 mil potenciais clientes. Essa conta é **uma premissa minha**.
- Agências e revendedores (white label sobre Z-API, Evolution e BSPs) provavelmente somam milhares no Brasil, mas não achei número.

### Lacunas
- Não há número oficial de WABAs no Brasil, nem de BSPs/Tech Providers BR, nem de agências revendedoras.
- Falta o volume de mensagens de marketing no Brasil e a receita da Meta com WhatsApp no Brasil.

## Mapa de concorrência e notas (síntese)

### Takeaway
**Veredito: dor real, mas estreita e em grande parte já endereçada por Meta e BSPs. Não vale como produto horizontal "dashboard de custo para PMEs". Pode valer como nicho: "auditoria de custo e reclassificação multi-cliente para agências e operações com 5 ou mais WABAs/BSPs", ou como feature/add-on de um produto maior (CRM/inbox). Nota geral: cerca de 4,5/10.**

### Achados citados (concorrência resumida)
| Player | Recurso de custo relevante | Preço (secundário) | Fonte |
|---|---|---|---|
| Meta (nativo) | Custo por template entregue, pricing analytics API, webhook de reclassificação, max price e budget na MM API | Grátis | [Meta MM pricing](https://developers.facebook.com/documentation/business-messaging/whatsapp/marketing-messages/pricing) |
| SleekFlow | Limite de gasto mensal + alertas 70/90/100% + bloqueio | n/d | [SleekFlow Help](https://help.sleekflow.io/en_US/setting-a-monthly-message-spend-limit-for-whatsapp) |
| Kommo | Custo por template, por entrega e por clique | n/d | [Kommo](https://www.kommo.com/support/messenger-apps/whatsapp-analytics) |
| Spur | Custo total por país e período | n/d | [Spur](https://help.spurnow.com/en/articles/12595095-how-to-use-whatsapp-analytics-quick-links) |
| Wati | Guia de otimização, calculadora, campaign analytics | ~US$ 29/usuário ou R$ 299/mês + markup ~25% | [eesel](https://www.eesel.ai/blog/wati-pricing); [Nação Digital](https://nacao.digital/blog/whatsapp-business-api/) |
| Zenvia | — (não verificado) | ≥R$ 600/mês + R$ 0,47–0,55/template | [Nação Digital](https://nacao.digital/blog/whatsapp-business-api/) |
| Blip | — (não verificado) | Sob cotação; excedente ~R$ 1,40/conversa | [Tenessi](https://www.tenessihub.com.br/seo/take-blip-vs-zenvia/) |
| Digisac | Simulador de custos (pré-venda) | A partir de R$ 99/mês | [Digisac](https://digisac.com.br/blog/quanto-custa-um-chatbot-para-whatsapp-e-como-calcular-o-retorno) |
| Chakra | Dashboards avançados (alegação) | US$ 10–50/mês | [Chakra](https://chakrahq.com/help/learning-centre/whatsapp-business-api/insights-reporting) |
| laravel-whatsapp-cost-control | Caps, alertas, ledger | Open source | [Packagist](https://packagist.org/packages/dineshstack/laravel-whatsapp-cost-control) |

### Inferências: scores (0–10, julgamento meu)
- **Recorrência da dor: 6.** A fatura é mensal e as regras mudam com frequência (jul/2025, abr/2025, out/2026, BRL em 2026). Mas, depois de configurado, o gasto tende a ser previsível.
- **Disposição a pagar: 4.** A PME brasileira já paga mensalidade de BSP e resiste a mais uma ferramenta. Agências pagam se puderem repassar o custo ou provar economia. Os gastos típicos de PME (R$ 500–5 mil/mês em mensagens) limitam o ticket.
- **Fit de assinatura: 6.** O monitoramento é contínuo por natureza, mas o valor se concentra em uma "auditoria única" (achou o markup, migrou de BSP, cancelou).
- **Baixa concorrência: 5.** Não há standalone, mas Meta, SleekFlow, Kommo e os próprios BSPs cobrem o básico, e a tendência é cobrir mais.
- **Tamanho de mercado: 4.** O nicho com gasto relevante tem talvez de 5 mil a 30 mil contas no Brasil (premissa). O LatAm amplia, mas cada país tem tarifas diferentes.
- **Retenção: 4.** Risco alto de churn após otimizar, e de commoditização pelo BSP ou pela Meta.
- **Buildability: 6.** A Cloud API direta é fácil: pricing analytics, webhooks e template analytics. Para clientes atrás de BSP (Blip, Zenvia), o acesso aos dados é difícil, e o MVP precisaria de upload ou parse de fatura (PDF/CSV) e da tabela Meta.
- **Ticket estimado (premissa):** de R$ 99 a R$ 299/mês para PME e de R$ 490 a R$ 1.500/mês para agência multi-cliente, ou um modelo de "auditoria" de R$ 500–2.000 pontual mais monitoramento.

### Inferências: recomendações
- Se seguir: validar com 10–15 agências e operações de atendimento afetadas pela cobrança de serviço desde 01/10/2026. A proposta seria "quanto você vai pagar a mais por respostas de atendimento e onde o BSP está cobrando acima da tabela Meta".
- Wedge mais forte: **auditoria de fatura de BSP versus tabela oficial** + **alerta de reclassificação de template com impacto em R$** + **relatório multi-WABA white label para agência**.
- Alternativa: embutir como feature em um produto maior (CRM/inbox) em vez de SaaS isolado.

### Lacunas
- Não houve entrevistas nem dados de disposição a pagar. Os scores são julgamento.
- Faltou verificar features e preços de Twilio, Gupshup, 360dialog, Z-API, ManyChat, Botconversa e Take Blip (analytics de custo) por falta de acesso aos sites.
- Recomenda-se reexecutar os fetches com os domínios liberados: developers.facebook.com, reclameaqui.com.br, respond.io, whapi.cloud e crminer.com.br.
