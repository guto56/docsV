# Validação da ideia: validador/monitor de cadastro fiscal (NCM, CST, cClassTrib, IBS/CBS) para escritórios contábeis e PMEs — Reforma Tributária (data de referência: nov/2026)

> Limitação de método: nesta sessão o WebFetch foi bloqueado pela rede (gov.br, erpworks.com.br, contmatic.com.br não resolvem). Toda a evidência abaixo vem de **resumos e trechos do WebSearch**, não da leitura integral das páginas. Datas e números devem ser conferidos abrindo as URLs antes de decisões. Onde a fonte é blog de fornecedor (marketing), isso está indicado.

## 1. Status regulatório: rejeições de IBS/CBS estão em vigor? Marcos de 2026–2027

### Takeaway
A **rejeição por AUSÊNCIA** do grupo IBS/CBS na NF-e foi **suspensa** pelo Ato Técnico Conjunto CGIBS/RFB nº 1 (31/07–01/08/2026), sem data de retomada; a **obrigação legal** de preencher continua (Ato Conjunto RFB/CGIBS nº 4, em lotes até 01/01/2027, quando entra o Simples Nacional). Quando o grupo É preenchido, as **regras de consistência** (1024 cClassTrib x CST, 1023 código inexistente, 1025 modelo não permitido, 778 NCM inválida) são citadas por várias fontes como ativas. Erro "silencioso" (cClassTrib válido mas errado) não gera rejeição e vai para a apuração — esse é o risco econômico real a partir de 2027, quando a CBS passa a ser cobrada de fato.

### Cited Findings
- Receita Federal e CGIBS anunciaram em jul/2026 que "flexibilizarão a obrigatoriedade de informações em documentos fiscais" — [Receita Federal (gov.br)](https://www.gov.br/receitafederal/pt-br/assuntos/noticias/2026/julho/receita-federal-e-cgibs-flexibilizarao-obrigatoriedade-de-informacoes-em-documentos-fiscais); [Agência Gov](https://agenciagov.ebc.com.br/noticias/202608/receita-federal-e-cgibs-flexibilizarao-obrigatoriedade-de-informacoes-em-documentos-fiscais-1)
- O Ato Técnico Conjunto CGIBS/RFB nº 1 suspende a obrigatoriedade de preenchimento e a rejeição de NF-e, NFC-e, CT-e, NFCom sem campos de IBS/CBS; "caiu a rejeição, não a obrigação" — [ERPWorks](https://erpworks.com.br/conteudos/nfe-ibs-cbs-obrigatoriedade-agosto-2026-rejeicoes/); [IOB Notícias](https://noticias.iob.com.br/reforma-adiamento-rejeicao-notas-ibs-cbs/); [GRM Advogados](https://grm.com.br/receita-federal-suspende-rejeicao-de-documentos-fiscais-sem-informacoes-de-cbs-e-ibs/); [NS Tecnologia](https://blog.nstecnologia.com.br/suspensao-ibs-cbs/)
- Pela NT 2025.002-RTC v1.53, a rejeição por ausência do grupo em produção ficou como "implementação futura"; em homologação vale desde 01/07/2026 — [Nota Gateway](https://notagateway.com.br/blog/cclasstrib-nfe/)
- Antes da suspensão, o cronograma previa produção obrigatória em 03/08/2026 para regime normal (CRT 3) — [Sittax](https://sittax.com.br/artigo/cclasstrib-nf-reforma-tributaria/); [Exame](https://exame.com/economia/ibs-e-cbs-na-nota-fiscal-erro-podera-travar-faturamento-a-partir-de-3-de-agosto/)
- Cronograma em "ondas"/lotes do Ato Conjunto RFB/CGIBS nº 4 segue até 01/01/2027; Simples Nacional obrigado em 01/01/2027 para todos os DF-e — [Contmatic](https://simplifique.contmatic.com.br/blogs/obrigatoriedade-ibs-cbs-documentos-fiscais-4-ondas-2026); [Bluetax](https://bluetax.com.br/blog/receita-federal-cgibs-flexibilizarao-obrigatoriedade)
- Para NFS-e, período de tolerância até 31/12/2026 sem rejeição automática — [resumo de busca citando hopecont/ynpar](https://ynpar.com/nota-fiscal-ibs-cbs-rejeitada/) (não verificado na íntegra)
- Rejeição 1024: os 3 primeiros dígitos do cClassTrib devem ser iguais ao CST; senão a SEFAZ rejeita — [Planogestor](https://planogestor.com.br/blog/cst-ibs-cbs-tabela-quando-usar-cada-codigo); [TreeunFE ajuda](https://ajuda.treeunfe.com.br/hc/pt-BR/articles/1784295506-como-resolver-a-rejeicao-1024-classificacao-tributaria-do-ibs-e-da-cbs-incompativel-com-o-cst-informado)
- Outras: 1023 (cClassTrib inexistente), 1025 (não permitido no modelo), 1059 (finalidade x cClassTrib), 1115 (grupo ausente), 1050 (cClassTrib não informado), 778 (NCM inexistente, que costuma puxar 1024) — [Taxcel](https://taxcel.com.br/rejeicoes-ibs-cbs-xml-nfe); [Hopecont](https://hopecont.com/blog/rejeicao-nota-fiscal-ibs-cbs/); [TaxRadar](https://taxradar.app/blog/ncm/rejeicoes-nfe-ibs-cbs-como-resolver); [Escola Superior ESN](https://escolasuperioresn.com.br/rejeicao-nf-e-ibs-cbs-erros-como-corrigir/)
- Fórum DFS Pro com erro real "cClassTrib do IBS/CBS não permitido neste modelo de DF-e" — [DFS Pro fórum](https://www.dfspro.com.br/forum/documentos-fiscais-cst-cclasstrib-cadastro-4/cclasstrib-do-ibs-cbs-nao-permitido-neste-modelo-de-dfe-20439)
- cClassTrib válido mas incorreto para a operação não gera rejeição; o erro aparece na apuração/crédito do adquirente — [Jettax](https://www.jettax.com.br/blog/ncm-errada-o-risco-fiscal-que-continua-mesmo-quando-a-nota-e-autorizada/); [Systax](https://www.systax.com.br/artigos-e-novidades/cclasstrib-o-novo-cbenef-com-a-reforma-tributaria/)
- Mesma NCM pode ter tratamentos distintos (ex.: 9619.00.00 absorventes x fraldas) — parametrizar por produto, não só por NCM — [Jettax/resumo de busca](https://www.jettax.com.br/blog/ncm-errada-o-risco-fiscal-que-continua-mesmo-quando-a-nota-e-autorizada/)
- **Volatilidade da tabela**: fontes citam versões v1.51, v1.53, v1.60, v1.71 da IT/NT; IT 2025.002 v1.71 divulgada em 30/10/2026 ampliando classificações de doações/operações não onerosas — [Portal SPED Brasil fórum](https://portalspedbrasil.com.br/forum/it-2025-002-v1-71-atualiza-tabela-cclasstrib-e-amplia-utilizacao-de-classificacoes-ligadas-a-doacoes-e-operacoes-nao-onerosas/); versão de 01/10/2026 com 173 códigos em 18 CST — [resumo de busca, e-Auditoria/Dataas](https://www.e-auditoria.com.br/blog/cclasstrib/)
- **2027**: CBS cobrada de fato a partir de 01/01/2027 e extinção de PIS/Cofins; 2026 é ano-teste (CBS 0,9%, IBS 0,1%) — [Tax Group](https://www.taxgroup.com.br/intelligence/aliquota-ibs-cbs/); [InvestNews](https://investnews.com.br/guias/reforma-tributaria/)
- Alíquota de referência da CBS 2027 calculada pelo TCU em 11,3% (28/10/2026), pendente de fixação pelo Senado até 15/12 — [Tax Group](https://www.taxgroup.com.br/intelligence/aliquota-ibs-cbs/); [vhsys](https://blog.vhsys.com.br/cbs-2027-aliquota/) (dado vindo de resumo de busca; conferir)
- Simples Nacional: opção por recolher IBS/CBS no regime regular ("Simples híbrido") a partir de jan/2027, com prazo de opção até 30/10/2026 segundo uma fonte — [Facilite](https://www.facilite.co/aliquota-ibs-cbs-2027); outra fonte não cita prazo — [Sittax simulação](https://sittax.com.br/artigo/simulacao-da-reforma-tributaria/)
- Split payment: fontes divergem — início gradual/facultativo em 2027 vs. obrigatoriedade a partir de 2028 — [Thomson Reuters/Mastersaf blog](https://www.thomsonreuters.com.br/pt/tax-accounting/onesource-mastersaf/blog/split-payment-reforma-tributaria.html); [Tax Group guia](https://www.taxgroup.com.br/intelligence/reforma-tributaria-2026-guia-completo-sobre-o-que-muda-e-a-transicao/)

### Inferences
- A "dor de rejeição" em nov/2026 é **menor do que o marketing de agosto sugeria**: quem não preenche não é bloqueado. Mas quem preenche errado (1024/1023/1025) é bloqueado — e o ERP que gera o grupo automaticamente pode gerar combinações inválidas.
- A dor relevante migra de "nota rejeitada" para "**imposto/crédito errado**" a partir de jan/2027 (CBS real, Simples híbrido gerando crédito para clientes B2B). Isso é menos urgente-visível, porém de maior valor financeiro e recorrente até 2033 (IBS sobe gradualmente 2029–2033, cada ano muda alíquotas/regras).
- Tabela cClassTrib muda ~mensalmente (várias versões em 2026) → justifica "monitor de mudanças" recorrente.
- Risco regulatório: a suspensão sem data pode ser revertida a qualquer momento (pico de demanda) ou estendida (demanda morna).

### Gaps
- Não foi possível abrir o texto oficial do Ato Técnico Conjunto nº 1 nem a NT vigente para confirmar quais regras de consistência (1024 etc.) estão ativas em **produção** hoje vs. só homologação. Fontes secundárias divergem.
- Data de retorno da rejeição por ausência: não encontrada.
- Uma fonte (Reforma Aberta) alega que a Receita publicou em 16/11/2026 no GitHub (MIT) o código da calculadora oficial — não verificado; se verdadeiro, reduz barreira técnica para todos (inclusive concorrentes).

## 2. ERPs/emissores populares já validam cClassTrib/NCM?

### Takeaway
Os ERPs estão **adicionando campos** (cClassTrib no cadastro/natureza de operação, CST derivado automaticamente), mas a evidência encontrada é de **configuração manual ou em massa**, não de validação/sugestão inteligente por NCM. Não encontrei evidência pública de validação semântica (cClassTrib correto para o produto) em Bling, Omie, Tiny/Olist, Nibo, Questor, Domínio. Alguns nichos (Ganso Tax) dizem entregar classificação pré-preenchida.

### Cited Findings
- Conta Azul Pro: usuário escolhe o cClassTrib; o CST-IBS/CBS é gerado automaticamente no XML a partir dele (elimina 1024 por construção, mas não valida se o cClassTrib é o correto) — [Ajuda Conta Azul](https://ajuda.contaazul.com/hc/pt-br/articles/47089100961293-NF-e-qual-%C3%A9-a-diferen%C3%A7a-entre-CST-do-ICMS-e-CST-IBS-CBS); NFS-e pede NBS, indicador de operação e cClassTrib — [Ajuda Conta Azul NFS-e](https://ajuda.contaazul.com/hc/pt-br/articles/42702992541069-NFS-e-onde-consultar-e-como-preencher-o-IBS-e-CBS)
- Alterdata: base de conhecimento sobre importação das tags da NT 2025.002-RTC (cClassTrib) — [Alterdata ajuda](https://ajuda.alterdata.com.br/fiscalbase/reforma-tributaria-tags-importadas-nf-e-nota-tecnica-2025-002-rtc-297895942.html)
- IOB (ERP): artigo de ajuda "Cadastro de Produtos" para Reforma Tributária — [IOB Aprendo](https://aprendo.iob.com.br/ajudaonline/artigo.aspx?artigo=17557)
- Linear Sistemas: CST e cClassTrib preenchidos manualmente por produto ou em massa via planilha — [Linear Sistemas KB](https://atendimento.linearsistemas.com.br/kb/pt-br/article/597899/cadastro-de-produtos-configuracao-de-dados-do-cbs-e-ibs)
- Starsoft: prioridade de onde vem o cClassTrib: 1-TES, 2-Item de estoque, 3-NCM — [Starsoft suporte](https://suporte.starsoft.com.br/portal/pt/kb/articles/quais-procedimentos-de-configura%C3%A7%C3%A3o-devem-ser-realizados-no-sistema-para-adequa%C3%A7%C3%A3o-%C3%A0-reforma-tribut%C3%A1ria-para-2026-vers%C3%A3o-1)
- Ganso Tax: classificação (NCM, CEST, tributos) chega preenchida no cadastro do produto — [Ganso](https://ganso.com.br/classificacao-tributaria-de-produtos-automatizar-ncm-cest/) (marketing)
- Omie tem conteúdo sobre rejeição por NCM inválido (indica dor frequente na base) — [Omie blog](https://www.omie.com.br/blog/rejeicao-nota-fiscal-ncm-invalido/)
- Qive (ex-Arquivei) publica conteúdo sobre CST IBS/CBS e erros de classificação — [Qive blog CST](https://qive.com.br/blog/cst-no-ibs-e-cbs); [Qive erros](https://qive.com.br/blog/erros-tributarios-classificacao-incorreta-produtos)
- Workana: vaga para "configuração fiscal completa de Tiny ERP e Olist" (revisar NCM, tributação, inconsistências) — indica que o Tiny não resolve sozinho — [Workana](https://www.workana.com/pt/job/especialista-para-configuracao-fiscal-completa-de-tiny-erp-e-olist)
- Portal DFe "Conformidade Fácil" (oficial) permite consultar tabelas CST/cClassTrib de forma interativa — [resumo de busca, Webmania](https://ajuda.webmania.com.br/pt-BR/articles/12994146-codigo-de-classificacao-tributaria-cclasstrib)

### Inferences
- Os ERPs de PME tendem a resolver a **consistência sintática** (CST derivado do cClassTrib → 1024 some), deixando a **escolha correta** do cClassTrib ao usuário/contador. Esse é o gap que um validador poderia ocupar.
- Risco forte de **commoditização**: em 12–24 meses, Bling/Omie/Conta Azul provavelmente incorporarão sugestão de cClassTrib por NCM (tabela pública). Hipótese, não fato.

### Gaps
- Não encontrei páginas de recursos de Bling, Omie, Tiny/Olist, Nibo, Questor, Domínio (Thomson Reuters), SIEG, Qive descrevendo **validação automática de cClassTrib** em lote. Precisa verificação direta nas centrais de ajuda.

## 3. Concorrentes especializados e preços

### Takeaway
Mercado **já lotado** em nov/2026: incumbentes de inteligência fiscal (e-Auditoria, Systax, Sittax, Mastersaf/Thomson Reuters, Tax Group, Avalara, Sovos) + **dezenas de micro-SaaS e ferramentas gratuitas** surgidas em 2026 especificamente para cClassTrib por NCM e validação de XML (ClassTrib, TaxHub Fiscal, TribuMap, Reforma Aberta grátis, Contbit grátis, TaxRadar, Tributon API). Preços de entrada observados: grátis a R$ 197–497/mês.

### Cited Findings
| Player | Oferta relevante | Preço/público | Fonte |
|---|---|---|---|
| e-Auditoria | Plataforma de inteligência fiscal para escritórios: audita, corrige, classifica itens por NCM; complementar ao ERP | Preço não público; Black November 2026 com até 51% off | [Classificar itens](https://www.e-auditoria.com.br/solucoes/para-classificar-itens/); [Planos](https://www.e-auditoria.com.br/planos/); [Black Nov](https://www.e-auditoria.com.br/ofertas/lm-black-november-2026/) |
| Sittax (Sittax RT) | Simula Simples x híbrido x regular com XML/PGDAS da carteira; diz corrigir cClassTrib de cada nota e sinalizar divergências | Preço não público; foco escritórios | [Sittax](https://sittax.com.br/); [Sittax RT](https://sittax.com.br/sittax-rt/) |
| Systax | Conteúdo e base tributária (cClassTrib como "novo cBenef") | Enterprise, sob consulta | [Systax](https://www.systax.com.br/artigos-e-novidades/cclasstrib-o-novo-cbenef-com-a-reforma-tributaria/) |
| Thomson Reuters (Domínio / ONESOURCE Mastersaf) | Compliance fiscal enterprise, conteúdo sobre split payment | Enterprise | [TR blog](https://www.thomsonreuters.com.br/pt/tax-accounting/onesource-mastersaf/blog/split-payment-reforma-tributaria.html) |
| Tax Group | Inteligência tributária, conteúdo de alíquotas | Enterprise/médias | [Tax Group](https://www.taxgroup.com.br/intelligence/aliquota-ibs-cbs/) |
| TaxHub Fiscal | Sistema de classificação cClassTrib IBS/CBS | Grátis; Profissional R$ 197/mês; Expert R$ 497/mês | [TaxHub](https://taxhubfiscal.com.br/) |
| ClassTrib | Classifica produtos para a reforma | Profissional R$ 197 (até 40.000 consultas); promo R$ 59,90 (anúncios inconsistentes) | [ClassTrib](https://classtrib.com/novo/); [promo](https://classtrib.com/promocao/) |
| TribuMap | cClassTrib por NCM/NBS grátis; lote e validador de XML no trial 7 dias | Preço não exibido | [TribuMap](https://www.usetribumap.com.br/) |
| Reforma Aberta | Validador gratuito CBS/IBS/IS no navegador, valida XML | Grátis | [Reforma Aberta](https://reformaaberta.com.br/) |
| Contbit Verificador | Verifica cClassTrib no XML da NF-e grátis | Grátis | [Contbit](https://verificar.contbit.tax/) |
| Auditor Fiscal (indie) | Lê XML e mostra cClassTrib/CST | Grátis, 2 XMLs por envio | [jannio](https://jannio.pythonanywhere.com/) |
| Tributon | API (GitHub) cálculo CBS/IBS/IS e validação XSD; cobra por SKU certificado; cita escritórios cobrando ~R$ 500 por revisão de cadastro (alegação do próprio fornecedor) | Por SKU | [GitHub Tributon](https://github.com/juliopessan/Tributon) |
| TaxRadar | Tabela cClassTrib por NCM, conteúdo de rejeições | — | [TaxRadar](https://taxradar.app/blog/ncm/cclasstrib-como-mapear-ncm-regime-ibs-cbs) |
| Contabil Descomplica, Btax, Taxcel, eSimples Auditoria | Classificação fiscal / simulação / auditoria NCM | eSimples tem página de preços | [Contabil Descomplica](https://www.contabildescomplica.com.br/); [Btax](https://www.btax.com.br/); [Taxcel](https://taxcel.com.br/rejeicoes-ibs-cbs-xml-nfe); [eSimples preços](https://www.esimplesauditoria.com/precos) |

### Inferences
- A camada "consulta cClassTrib por NCM" + "validar XML" virou **commodity gratuita** em 2026. Diferenciação só seria possível em: (a) monitoramento contínuo multi-cliente para escritório (portfólio de CNPJs, alertas quando versão da tabela muda e afeta itens do cliente), (b) integração com captura automática de XML (SIEG/Qive/e-Auditoria já têm), (c) responsabilidade técnica/curadoria.
- Incumbentes com distribuição em escritórios (e-Auditoria, Sittax, SIEG, Qive) já miram exatamente o mesmo ICP.

### Gaps
- Preços de e-Auditoria, Sittax, Systax, Avalara Brasil, Sovos, SIEG, Qive não encontrados (sob consulta). Fiscal.io e Cosmos/Bluesoft não foram pesquisados por limite de chamadas.

## 4. Evidência em primeira pessoa da dor

### Takeaway
Evidência **fraca a moderada**: encontrei fóruns técnicos com dúvidas reais (DFS Pro, ProjetoACBr, Portal SPED Brasil, TabNews) e vagas no Workana para configuração fiscal de ERP, mas **nenhuma reclamação no Reclame Aqui** nem thread do fórum Portal Contábeis especificamente sobre cClassTrib nas buscas feitas. A maior parte do conteúdo é marketing de fornecedor/escritório ("revise seu cadastro").

### Cited Findings
- DFS Pro fórum: usuário com erro "cClassTrib do IBS/CBS não permitido neste modelo de DF-e" — [DFS Pro](https://www.dfspro.com.br/forum/documentos-fiscais-cst-cclasstrib-cadastro-4/cclasstrib-do-ibs-cbs-nao-permitido-neste-modelo-de-dfe-20439)
- ProjetoACBr fórum: desenvolvedor pergunta qual cClassTrib usar em retorno/cobrança de industrialização; resposta: ajustar sistema e aguardar contador — [ProjetoACBr](https://www.projetoacbr.com.br/forum/topic/86383-cclasstrib-para-as-diversas-opera%C3%A7%C3%B5es/)
- Portal SPED Brasil fórum: discussão da IT 2025.002 v1.71 (30/10/2026) — [Portal SPED Brasil](https://portalspedbrasil.com.br/forum/it-2025-002-v1-71-atualiza-tabela-cclasstrib-e-amplia-utilizacao-de-classificacoes-ligadas-a-doacoes-e-operacoes-nao-onerosas/)
- TabNews: dev pedindo ajuda de contador para questão fiscal — [TabNews](https://www.tabnews.com.br/Andreldev/tem-algum-contador-por-ai-ou-so-ve-como-consegue-me-ajudar-com-issod) (relação exata com cClassTrib não verificada)
- Workana: "Especialista para configuração fiscal completa de Tiny ERP e Olist" (revisar NCM, tributação, inconsistências) — [Workana](https://www.workana.com/pt/job/especialista-para-configuracao-fiscal-completa-de-tiny-erp-e-olist); "Atualizador tributário" (ICMS, PIS, COFINS, CEST por produto) — [Workana](https://www.workana.com/job/atualizador-tributario)
- CRC-CE fez evento/material "Classificação tributária na era de IBS e CBS" (26/02/2026) — demanda de capacitação entre contadores — [CRC-CE PDF](https://www.crc-ce.org.br/crcnovo/files/CTEIBSCBS26022026.pdf)
- Notícia replicada em sites de escritórios: "empresas devem revisar NCM e cClassTrib para evitar rejeição" — [contadores.cnt.br](https://contadores.cnt.br/projetos/54/noticias/tecnicas/2026/06/29/reforma-tributaria-empresas-devem-revisar-ncm-e-cclasstrib-para-evitar-rejeicao-de-notas-fiscais.html); [Meira Fernandes](https://www.meirafernandes.com.br/noticias/reforma-tributaria-empresas-devem-revisar-ncm-e-cclasstrib-para-evitar-rejeicao-de-notas-fiscais/)
- eSimples Auditoria posiciona "revisão de NCM e ICMS-ST" como serviço que escritórios vendem aos clientes — [eSimples](https://www.esimplesauditoria.com/revisao-de-ncm-e-icms-st)

### Inferences
- Há uma **dor real de configuração**, mas concentrada em picos (jul–ago/2026; provavelmente dez/2026–jan/2027 com o Simples). A suspensão da rejeição esvaziou a urgência visível.
- "Revisão de cadastro" parece ser vendida como **projeto pontual** (consultoria/escritório), não como assinatura — sinal contra recorrência.

### Gaps
- Sem posts de LinkedIn/YouTube/Reclame Aqui verificados. Recomenda-se busca manual nesses canais e entrevistas com 10–15 contadores antes de construir.

## 5. Tamanho de mercado

### Takeaway
~90–102 mil organizações contábeis e ~490–530 mil profissionais; NF-e na casa de bilhões/ano (426 milhões de NF-e só no início de 2026 segundo a Receita). Mercado grande, mas o segmento pagante (escritórios com clientes de comércio/indústria) é uma fração.

### Cited Findings
- CFC: 97.836 organizações contábeis e 529.505 profissionais (data não clara) — [CFC](https://cfc.org.br/?p=76649)
- Benchmark Escola Exchange (21/09/2026): 101.880 organizações contábeis; +40% 2020–2025 — [Âmbito Jurídico](https://ambitojuridico.com.br/?p=9024386); [Roberto Dias Duarte](https://www.robertodiasduarte.com.br/relatorio-executivo-evolucao-das-organizacoes-contabeis-no-brasil-1995-2024/)
- "Mais de 100 mil escritórios, 79% sem área comercial estruturada" — [Site Contábil](https://sitecontabil.com.br/noticias_empresariais/ler/brasil-soma-mais-de-100-mil-escritorios-contabeis--mas-79--ainda-nao-tem-area-comercial-estruturada)
- 490 mil profissionais — [Contábeis](https://www.contabeis.com.br/noticias/16964/contabilidade-no-brasil-possui-490-mil-profissionais/)
- 2020: mais de 3 bilhões de NF-e, R$ 17,51 tri — [Jornal Contábil](https://www.jornalcontabil.com.br/noticia/41761/mais-de-r-17-trilhoes-de-notas-fiscais-foram-emitidas-em-2020)
- Início de 2026: 1 bilhão de notas/eventos, sendo 426 milhões de NF-e — [ReformaTributaria.com](https://www.reformatributaria.com/governo/brasil-emitiu-1-bilhao-de-notas-fiscais-desde-1o-de-janeiro-diz-receita/)

### Inferences
- Se 10–20% dos escritórios atendem carteira relevante de comércio/indústria emissora de NF-e de produto e 1–3% adotam uma ferramenta nova nicho, SAM realista ≈ 1–6 mil escritórios. A R$ 150–300/mês → ~R$ 2–20 mi ARR teórico (premissa, não fato).

### Gaps
- Número de CNPJs emissores de NF-e modelo 55 em 2025: não encontrado.

## 6. Score e veredito (análise do pesquisador — premissas, não fatos)

### Takeaway
**Veredito: NÃO como produto standalone de "validador de cClassTrib/NCM". Pivô possível: monitor multi-cliente para escritórios focado em "erro silencioso" (crédito/apuração CBS 2027) + alertas de versão da tabela, vendido como canal/add-on.** A dor é real e se estende até 2033, mas o recorte "validar XML antes da rejeição" foi (1) esvaziado pela suspensão da rejeição em ago/2026, (2) comoditizado por ferramentas grátis e pela correção nativa nos ERPs (CST derivado do cClassTrib), (3) disputado por incumbentes com distribuição em escritórios (e-Auditoria, Sittax, SIEG, Qive).

### Cited Findings
- Ferramentas gratuitas existentes: [Reforma Aberta](https://reformaaberta.com.br/); [Contbit](https://verificar.contbit.tax/); [TribuMap](https://www.usetribumap.com.br/)
- Faixa de preço de pagos: R$ 197–497/mês — [TaxHub](https://taxhubfiscal.com.br/); [ClassTrib](https://classtrib.com/novo/)
- Tabela muda com frequência (v1.71 em 30/10/2026) — [Portal SPED Brasil](https://portalspedbrasil.com.br/forum/it-2025-002-v1-71-atualiza-tabela-cclasstrib-e-amplia-utilizacao-de-classificacoes-ligadas-a-doacoes-e-operacoes-nao-onerosas/)

### Inferences
| Critério | Nota 0–10 | Justificativa |
|---|---|---|
| Recorrência | 6 | Tabela muda ~mensalmente e transição dura até 2033, mas o cadastro, uma vez saneado, muda pouco por cliente |
| Disposição a pagar | 4 | Concorrência grátis; dor visível (rejeição) suspensa; revisão vendida como projeto pontual |
| Encaixe em assinatura | 5 | Monitor multi-CNPJ encaixa; validador avulso não |
| Baixa concorrência | 2 | 10+ players em 2026, incluindo incumbentes e gratuitos |
| Tamanho de mercado | 7 | ~100 mil escritórios, bilhões de NF-e |
| Retenção | 4 | Risco de churn após saneamento e quando ERPs incorporarem a função |
| Buildability | 8 | Tabelas públicas, XSD público, possível código oficial aberto; MVP em semanas |
| **Média** | **~5,1** | |

- Ticket estimado: R$ 99–299/mês por escritório (por faixa de CNPJs) ou R$ 0,50–5 por SKU revisado; PME direta R$ 49–99/mês (baixa disposição). Premissa baseada nos preços dos concorrentes acima.
- Gatilhos que melhorariam a tese: retomada da rejeição por ausência com data definida; evidência de autuações/glosa de crédito por cClassTrib errado em 2027; entrevistas mostrando que e-Auditoria/Sittax são caros demais para escritórios pequenos.

### Gaps
- Sem entrevistas com clientes; sem dados de churn/conversão dos concorrentes; sem confirmação oficial do status das regras de consistência em produção.
