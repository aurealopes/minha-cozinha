# Minha Cozinha | PRD do MVP

**Versão 0.2 · Proposta para validação · 5 de novembro de 2026**

Base: [01 · Problemas & Oportunidades](01-problemas-e-oportunidades.md) · [02 · Desk Research](02-desk-research.md)

## Resumo

O Minha Cozinha é um assistente de refeições com IA para quem cozinha no Brasil e precisa decidir o que fazer hoje com pouco esforço. A pessoa confirma o que tem em casa por foto, voz ou QR Code da NFC-e e recebe receitas que cabem no tempo, no orçamento e nas regras do seu perfil alimentar. A experiência é uma PWA mobile-first acessível por link, sem exigir instalação.

## Recorte do MVP do case

Este PRD descreve a visão do produto. Para o case, o MVP construído segue os recortes abaixo, que prevalecem sobre o restante do documento em caso de conflito.

| # | Decisão | Motivo |
|---|---|---|
| 1 | P0 restrito a captura por foto e voz, despensa aproximada, perfil com bloqueio de conflitos, busca, receita, histórico e login. O restante é P1. | Escopo construível; prioridade só funciona quando é seletiva. |
| 2 | NFC-e passa a P1, como prova de conceito. | O desk research tratou a NFC-e como hipótese: depende da cobertura por UF e das abreviações dos caixas. |
| 3 | O perfil cobre preferência, intolerância e alergia. Condição clínica fica fora do MVP, e o produto informa esse limite. | Exigiria revisão especializada, indisponível no case. |
| 4 | As receitas vêm de busca em sites especializados (modelo híbrido). A IA extrai e normaliza os ingredientes, as regras críticas validam e a receita é exibida com crédito e link para a fonte. Um catálogo pequeno e curado (50 a 100 receitas) funciona só como reserva. Redes sociais ficam fora do MVP. | Evita que a busca não retorne nada, sem reproduzir conteúdo de terceiros. Redes sociais não oferecem API de busca simples e o vídeo não vem estruturado. |
| 5 | Orçamento simplificado para "Sem compras" ou "Com compras", sem estimativa de preço. | Não há base de preços confiável. |
| 6 | Login obrigatório, por Google ou Apple, pedido depois da primeira sugestão e antes de salvar. O perfil de restrições é perguntado antes da primeira receita. | Despensa, perfil e histórico precisam de persistência. Cobrar o login antes de entregar valor aumenta o abandono. |
| 7 | A validação é um teste do protótipo com 3 a 5 pessoas, em vez de um piloto de 4 semanas. | Escala compatível com o case. |

## Problema e objetivos

**Pergunta central** — “O que consigo preparar hoje, com pouco esforço e sem comprar nada desnecessário?”

Quando decidir o que cozinhar exige lembrar o que sobrou, verificar os ingredientes de várias receitas e adaptar cada uma, pedir comida pronta vira a saída mais fácil. O MVP precisa encurtar essa decisão e tornar o aproveitamento de ingredientes parte do preparo.

### Objetivos para a pessoa usuária

- Encontrar rapidamente uma receita realizável com os ingredientes disponíveis e o tempo informado.
- Cozinhar com medidas claras, porções, etapas e substituições viáveis.
- Reaproveitar ingredientes que precisam ser usados primeiro e o restante de embalagens abertas.
- Configurar preferências e restrições uma vez e poder corrigir o perfil e a despensa a qualquer momento.

### Objetivos de negócio

- Converter sugestões em refeições efetivamente preparadas.
- Construir recorrência semanal em torno de cozinhar com o que já se tem.
- Manter a decisão do dia gratuita e validar interesse por planejamento semanal, lista de compras inteligente e personalização avançada na assinatura.
- Controlar o custo de IA por sessão e por preparo confirmado.

### Público, premissas e princípios

Público inicial proposto para o piloto: pessoas que cozinham em casa durante a semana, têm até 40 minutos e tomam decisões com base no tempo e no gasto adicional. Tratar como hipóteses a predominância de tempo e preço sobre variedade, a baixa disposição para manter uma despensa manual e a frequência semanal de uso.

**Viável agora > receita perfeita** · **Instrução clara > repertório grande** · **A IA sugere e explica, a pessoa decide**

### Escopo comercial

| Gratuito no MVP | Assinatura, a validar após o piloto |
|---|---|
| Decisão de hoje, captura e correção da despensa, perfil alimentar com todas as regras críticas, receitas e histórico. O estado “Planejado” registra a intenção em uma receita avulsa. | Agenda com planejamento de vários dias, lista de compras calculada a partir do plano e do estoque confirmado, personalização avançada. Preço e cobrança ficam para uma etapa posterior. |

**Fora do escopo do MVP** — WhatsApp e outros canais de mensagem, dado o custo por mensagem. Notificações diárias, apps nativos, prescrição alimentar, acompanhamento clínico, regras para condições clínicas, busca em redes sociais e preços de supermercados.

## Referências competitivas

As categorias abaixo vieram do briefing. O piloto deve testar se a combinação de despensa aproximada, viabilidade imediata e restrições persistentes reduz o esforço em relação aos caminhos que as pessoas já usam.

| Referência | O que comparar em teste |
|---|---|
| ChatGPT e Gemini | Esforço para explicar os ingredientes e reaplicar as mesmas restrições em visitas diferentes. |
| TudoGostoso e Panelinha | Tempo para encontrar uma receita executável e adaptar o que falta. |
| SuperCook e Samsung Food | Esforço para cadastrar, confirmar e corrigir a despensa entre refeições. |
| Assistentes de marca citados no briefing, como Qualy e Perdigão | Facilidade de começar e concluir a decisão em comparação com o acesso por link da PWA. |

## Histórias de usuário

- Como alguém com pouco tempo, quero confirmar os ingredientes em poucos toques e receber opções dentro do tempo total que tenho.
- Como alguém que quer economizar, quero saber o que consigo fazer sem compras e entender o que falta antes de escolher.
- Como alguém com restrição alimentar, quero cadastrar a regra uma vez e vê-la respeitada nas receitas, substituições e respostas do assistente.
- Como alguém que abriu uma embalagem ou tem um item perto de vencer, quero aproveitar o restante na próxima refeição.
- Como alguém que cozinha com frequência, quero reencontrar o que salvei, planejei, fiz e faria de novo.

## Requisitos e critérios de aceite

| ID | Prioridade e requisito | Critério de aceite |
|---|---|---|
| R01 | P0 · PWA mobile-first | Um link abre a experiência no navegador móvel sem instalação. A pessoa consegue navegar, corrigir itens e consultar a receita por controles acessíveis, com mensagens de erro textuais. |
| R02 | P0 · Captura assistida (foto e voz) · NFC-e em P1 | Foto, voz e, na P1, QR de NFC-e retornam uma lista revisável. A pessoa pode aceitar, renomear, remover ou acrescentar um item avulso antes de salvar. Captura negada, ambígua ou falha mantém o estoque anterior e oferece outro canal ou entrada pontual por texto. |
| R03 | P0 · Despensa aproximada | Cada item tem um estado “Pouco”, “Suficiente” ou “Confirmar”, com correção em linha. Itens em “Confirmar” e quantidades duvidosas para a porção exigem confirmação antes de contar para uma opção “Sem compras”. Reimportar o mesmo cupom não duplica itens. |
| R04 | P0 · Perfil persistente | O perfil guarda preferência, intolerância e alergia como categorias distintas e editáveis. Condição clínica fica fora do MVP e a interface informa esse limite. Preferências ordenam as sugestões. Restrições críticas confirmadas são aplicadas por regras determinísticas. Mudanças no perfil são aplicadas também ao reabrir receitas salvas. |
| R05 | P0 · Bloqueio de conflitos | A validação cobre ingredientes, derivados conhecidos, compostos, substituições, mudanças de porção que afetem regras e respostas do assistente. Conflito ou composição relevante desconhecida impede a exibição daquela opção como sugestão. Se nada passar, o fluxo informa a ausência de opções verificáveis e permite corrigir ingredientes ou ajustar apenas filtros flexíveis. |
| R06 | P0 · Busca por viabilidade | A pessoa ajusta tempo total, porções e “Sem compras” ou “Com compras”, com “Sem compras” como padrão. A busca consulta sites especializados, extrai os ingredientes de forma estruturada e aplica regras críticas, tempo e disponibilidade antes de ordenar por itens faltantes, aproveitamento e esforço. Cada receita exibe crédito e link para a fonte. Se a busca falhar ou nada passar pelas regras, usa o catálogo de reserva. Se houver item faltante, a opção fica em um grupo separado, mediante escolha da pessoa. |
| R07 | P0 · Receita clara e localizada | A ficha apresenta rendimento, tempo ativo e total (incluindo espera), medidas caseiras brasileiras e g/ml quando a equivalência estiver validada, etapas ordenadas e trocas locais com quantidades. Ingrediente obrigatório ausente aparece separado de item opcional. |
| R08 | P1 · Aproveitamento | Itens próximos do vencimento ganham prioridade quando a data foi informada ou confirmada pela pessoa e a receita passa pelos filtros. Itens marcados como vencidos ficam fora das sugestões. Após “Feito”, a pessoa confirma o que usou e se sobrou parte da embalagem. Essa sobra ganha prioridade na próxima busca compatível. |
| R09 | P0 · Histórico e retorno | A pessoa salva em “Quero fazer”, marca como “Planejado” ou registra “Feito” diretamente. “Faria de novo” é um marcador após o preparo e preserva o registro de “Feito”. A home de retorno permite retomar a despensa e encontrar receitas anteriores. |
| R10 | P1 · Privacidade e exclusão | A finalidade é exibida antes da captura e do preenchimento de restrições. A pessoa consegue corrigir e excluir dados de perfil e solicitar a exclusão da conta. Mídia e cupom bruto têm processamento transitório e descarte também em falhas. Eventos analíticos carregam somente identificadores e atributos operacionais permitidos. |
| R11 | P1 · Contingência de IA | A busca de receitas funciona com o catálogo de reserva quando a busca externa ou a geração falham ou excedem o orçamento. Explicações e adaptações geradas só aparecem depois de validadas. Sem validação, o produto usa uma explicação estruturada e, quando aplicável, a receita base já validada. |
| R13 | P0 · Login | Login social (Google ou Apple) obrigatório, pedido depois da primeira sugestão e antes de salvar despensa, perfil, receitas ou histórico. Dados informados antes do login são preservados na conta criada. |
| R12 | P1 · Conversa na receita | A pessoa pode perguntar sobre etapas e trocas dentro da ficha. Toda alteração de ingrediente segue as mesmas regras de R05. Respostas sobre diagnóstico ou prescrição são recusadas com uma orientação breve para revisar o perfil ou buscar apoio profissional. |

**Política de restrições proposta para o piloto.** Alergias e intolerâncias registradas como obrigatórias entram no bloqueio. Condições clínicas ficam fora do MVP. A interface explica a diferença entre preferência e exclusão obrigatória. O diagnóstico sozinho não gera regra alimentar. Quando a necessidade clínica não puder ser representada pelo conjunto de regras suportado, o produto informa o limite e não oferece recomendações apresentadas como adequadas à condição. Condições e regras suportadas exigem revisão especializada antes do piloto.

**Limites de segurança.** Uma foto identifica candidatos a ingredientes. Frescor e validade dependem de confirmação explícita da pessoa. Para produtos embalados, uma composição desconhecida ou um aviso relevante de “pode conter” impede o uso na sugestão diante da alergia correspondente. A ficha orienta a conferir rótulos e o risco de contato cruzado no preparo, sem prometer ausência de alérgenos. [Anvisa · Rotulagem de alimentos](https://www.gov.br/anvisa/pt-br/assuntos/alimentos/rotulagem)

## Experiência

1. **Abrir pelo celular.** A tela inicial apresenta “O que você tem em casa?” e os meios de entrada (foto e voz; NFC-e na P1). O login é pedido depois da primeira sugestão, antes de salvar. Permissões são solicitadas na ação correspondente. Antes da primeira recomendação, a pessoa responde se há restrições obrigatórias, registra as que se aplicam ou indica que não declarou nenhuma.
2. **Confirmar a captura.** Itens reconhecidos aparecem juntos para confirmação rápida. Identidades ambíguas pedem correção individual. O que veio do cupom é uma compra registrada e passa pela confirmação de presença em casa. Se a NFC-e estiver indisponível ou for de uma UF ainda sem suporte, oferecer foto, voz ou texto, preservando o que já foi confirmado.
3. **Escolher as condições de hoje.** A pessoa vê tempo, porções e gasto adicional ajustáveis. Proposta inicial de 40 minutos nos dias úteis e gasto adicional zero. A busca retorna até três opções elegíveis, com tempo total, esforço e motivo da indicação. Se não houver opções, a pessoa pode confirmar um item pendente, aumentar o tempo ou ver opções que exigem compras.
4. **Cozinhar.** A ficha agrupa ingredientes disponíveis e pendentes, oferece modo de leitura passo a passo e mostra apenas substituições validadas. Se a pessoa trocar uma quantidade ou ingrediente e a receita perder elegibilidade, a interface explica a alteração e permite voltar à última versão válida.
5. **Confirmar o preparo.** Ao marcar “Feito”, a pessoa confirma itens usados e sobras em uma revisão rápida. Pular a revisão deixa a disponibilidade dos itens afetados como “Confirmar”, sem baixar o estoque como fato. Na próxima visita, a home destaca uma sobra confirmada quando houver receita elegível.

**Exemplo de uso.** Na quarta-feira, uma pessoa tem meia embalagem de molho aberta e 25 minutos para fazer o jantar. Ela dita os itens, corrige a quantidade de arroz e confirma que quer evitar compras. A primeira opção explica que usa o molho e cabe no tempo. Após preparar a receita, a pessoa confirma o que sobrou. Na próxima vez, o Minha Cozinha usa essa informação para ordenar as opções, sem exigir que ela refaça o cadastro.

## Métricas e instrumentação

| Métrica | Como medir |
|---|---|
| Conversão de sugestão em preparo · principal | Sessões com pelo menos uma receita exibida e marcada “Feito” em até 7 dias ÷ sessões com sugestão exibida. Atribuir cada preparo à sessão da versão escolhida, sem duplicar eventos. É um indicador autorrelatado. |
| Tempo para cadastrar e corrigir despensa | Mediana e P90 do tempo entre início da captura e confirmação do lote, por canal, e entre abrir a edição e salvar uma correção. Acompanhar abandono separadamente. |
| Uso efetivo dos itens priorizados | Itens destacados como próximos do vencimento ou sobras e confirmados como usados ÷ itens destacados nas receitas priorizadas efetivamente preparadas. Exibir também a taxa de confirmação pós-preparo. |
| Retenção semanal | Entre pessoas cuja primeira sugestão foi exibida na semana 0, proporção que volta e recebe uma nova sugestão na semana 1. Acompanhar a mesma coorte até a semana 4. |
| Violações críticas | Meta de zero. Contar sugestões incompatíveis entregues em testes e incidentes confirmados em produção. Bloqueios preventivos entram em série separada. Um caso confirmado suspende o caminho afetado até correção e teste de regressão. |
| Custo de IA | Custo variável de captura e geração por sessão com resultado e por preparo confirmado. Separar visão, voz e geração para identificar o maior componente do custo. |

Eventos mínimos: captura iniciada, extração concluída ou falha por canal, lote confirmado, correção salva, busca iniciada, sugestões exibidas, nenhum resultado, receita selecionada, troca aplicada, estado atualizado, item priorizado usado, revisão de sobra concluída e bloqueio de segurança. Definir limites de custo e metas quantitativas de adoção após medir a linha de base no piloto. Validar interesse na assinatura separadamente, em teste de conceito.

## Considerações técnicas

- **Fontes de receitas e localização.** Fonte principal: busca em sites especializados de receitas, com extração estruturada dos ingredientes (aproveitar marcação estruturada de receita quando o site oferecer), normalização para ingredientes canônicos e exibição com crédito e link, sem reproduzir o conteúdo integral. Reserva: catálogo curado de 50 a 100 receitas com ingredientes canônicos, composição, porções, tempo, medidas locais e substituições revisadas. Mapear sinônimos regionais, como mandioca, aipim e macaxeira. Verificar os termos de uso dos sites consultados.
- **Ordem de processamento.** Normalizar entrada → buscar candidatos nos sites (ou no catálogo de reserva) → extrair e normalizar ingredientes → aplicar regras críticas → filtrar disponibilidade e tempo → ordenar → validar novamente antes de mostrar adaptações. O modelo recebe candidatos elegíveis e retorna uma adaptação estruturada. Um validador aplica as mesmas regras em qualquer rota, incluindo histórico e conversa.
- **Inventário e histórico.** Guardar ingrediente, estado, confirmação mais recente, validade opcional informada pela pessoa, sobra de embalagem e origem da entrada. Separar a receita versionada, o evento de preparo e as correções de estoque. Repetições de envio devem ser idempotentes e uma confirmação tardia não deve sobrescrever uma correção mais recente.
- **Integrações.** Isolar visão, transcrição e resolução da NFC-e em adaptadores. Validar cobertura por UF e variação de formato com cupons do piloto, aceitar somente destinos fiscais verificados, limitar redirecionamentos e descartar dados além dos itens necessários. Adotar cobertura explícita no piloto.
- **Compras.** “Sem compras” significa disponibilidade confirmada para os ingredientes obrigatórios e a porção selecionada. Com “Com compras”, mostrar apenas a lista de itens faltantes, sem estimativa de preço no MVP.
- **Privacidade.** Fotos, áudios e cupons podem trazer identificadores ou revelar informação de saúde. Remover campos sem utilidade, como CPF e dados de pagamento, e evitar enviar perfil clínico bruto para serviços de IA. Restringir o acesso e manter dados de saúde fora de logs e telemetria. Antes do piloto, validar base legal, fornecedores, retenção, exclusão e tratamento de backups. [Lei nº 13.709/2018 · LGPD](https://www.gov.br/mj/pt-br/assuntos/sua-protecao/sedigi/Lei13709.pdf)
- **Desempenho e custo.** Busca estruturada no caminho principal. Limitar tamanho dos arquivos, duração do áudio, tempo de espera e chamadas de geração. Definir tetos por operação após benchmark e preservar a busca quando a geração estiver indisponível. Medir latência e falhas por canal em aparelhos e redes representativos.

## Sequenciamento e validação

| Fase | Entrega | Critério de saída |
|---|---|---|
| 1 · Prova de viabilidade | Protótipo móvel, catálogo inicial, conjunto de regras críticas e ensaios com foto, voz e NFC-e. | Testar confirmação, tempo até a primeira receita e cobertura fiscal nas UFs selecionadas. Revisar o conjunto de regras com especialistas. |
| 2 · MVP fechado | PWA com perfil, captura, busca, receita, preparo, sobras, histórico e exclusão. | Passar por cenários de cadastro, fallback, privacidade e regressão de restrições, com zero violações críticas observadas na bateria de testes. |
| 3 · Teste do protótipo | Teste de usabilidade com 3 a 5 pessoas, validando as premissas assumidas como hipótese. | Decidir os próximos passos com base em conversão em preparo, tempo de captura e correção e zero violações críticas. |

**Equipe.** Case individual de Product Design, com construção apoiada por ferramentas de IA.

**Cenários de teste prioritários.** Cupom repetido ou inválido, foto ambígua, permissão de microfone negada, alergia com ingrediente derivado, produto embalado com composição desconhecida, tentativa de troca que viola regra crítica, receita antiga após mudança de perfil, tempo total acima do limite, estoque aproximado abaixo da porção, item vencido, exclusão de dados e indisponibilidade da geração.

## Decisões abertas

- Quais UFs e formatos de NFC-e entram no piloto? Qual taxa de leitura e tempo de confirmação justificam ampliar cobertura?
- Quais ingredientes e regras de alergia e intolerância podem ser suportados no MVP?
- Qual janela de “perto de vencer” faz sentido para a ordenação e pode ser compreendida sem inferir frescor?
- Quais sites de receitas consultar e quais termos de uso permitem exibir resumo com crédito e link?
- Qual taxa de preparo, retenção e custo justificaria ampliar o piloto e testar preço da assinatura?

*Criado com [ChatPRD](https://www.chatprd.ai/?utm_source=agent-plugin&utm_medium=doc).*
