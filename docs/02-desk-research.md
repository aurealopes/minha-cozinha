# Minha Cozinha: Desk Research e Benchmarking

**Fontes:** duas pesquisas geradas por IA em nov/2026, a partir do mesmo prompt. Uma é do Perplexity ("Planejamento de refeições no Brasil") e a outra do Gemini ("Análise de Mercado: Soluções Digitais para Planejamento de Refeições e Sugestão de Receitas no Brasil").

**Confiabilidade:** o Perplexity separa evidência de hipótese e explica as limitações de cada dado, então ele é a referência para os **números**. O Gemini traz mais ideias e exemplos, mas apresenta dados globais como se fossem do Brasil e usa fontes mais fracas (Reddit, Play Store, blogs), então ele é a referência para **ideias**, com os números checados antes de usar.

---

## 1. Mercado

- **Não existe estimativa confiável do mercado de receitas e planejamento no Brasil.** Os números disponíveis são globais (meal planning: US$ 380 mi em 2025) ou de categorias vizinhas (apps de dieta e nutrição, bem-estar). *(Perplexity; o Gemini usa os números globais sem fazer essa ressalva)*
- **A audiência é grande:** o TudoGostoso teve ~10,75 mi de visitas em set/2026, segundo a Semrush. *(Perplexity)* O número de "33 mi de visitantes únicos" é institucional e não informa a metodologia.
- **Cozinhar em casa continua relevante, mas o motivo mudou.** Na pandemia, o motivo era segurança e hobby. Em 2025 e 2026, é **economia e rapidez**. *(ambos)*
  - Refeições com preparo de até 30 min cresceram 5,7 p.p. (Kantar 2025)
  - 40% pretendem cozinhar mais e pedir menos delivery em 2026 (Neogrid/Opinion Box). É intenção declarada, não comportamento comprovado.
  - A inflação de alimentos no domicílio subiu bem acima do IPCA geral desde 2020 (FGV IBRE, citado pelo Gemini)
- **Desperdício:** o PNUMA estima ~20 mi de toneladas por ano de desperdício alimentar no Brasil. *(Perplexity)*

## 2. Comportamento do usuário

**A jornada está fragmentada entre canais.** Não existe pesquisa que divida a participação de cada um na decisão. *(ambos)*

| Canal | Papel na jornada |
|---|---|
| TikTok, Reels, Shorts | Descoberta e inspiração (receita rápida, de uma panela só) |
| Google e portais (TudoGostoso, Panelinha) | Execução: medida exata, ponto, comentários da comunidade |
| IAs generativas | Conversa e adaptação ao que se tem em casa |
| WhatsApp de marcas | Foto da geladeira vira receita (Qualy, Perdigão) *(Gemini)* |

**Critérios de escolha** *(ambos, com base na PwC 2025 e na Kantar)*
- **Preço:** 63% colocam preço como prioridade nas compras, e 52% escolhem a opção mais barata
- **Tempo:** preparo de até 30 min em alta
- **Saúde:** 79% se preocupam com ultraprocessados, e 72% com pesticidas
- **Restrições:** uma demanda cada vez mais técnica (celíacos, alergias, dietas para GLP-1)

**Dores**
- 52% citam a falta de ideias como a principal barreira *(Gemini, fonte internacional)*
- 41% abandonam o planejamento porque organizar listas e compras dá trabalho demais *(Gemini, fonte internacional)*

**Uso de IA:** mais da metade dos brasileiros usa IA para planejar compras e refeições (PwC 2025). ⚠️ O indicador agrega vários tipos de IA e de atividade, então **não** significa "metade usa o ChatGPT pra decidir o jantar". *(o Perplexity faz essa ressalva; o Gemini, não)*

## 3. Concorrência

| Solução | Proposta | Modelo | Principais reclamações |
|---|---|---|---|
| **TudoGostoso** (BR) | 200 mil+ receitas, busca por ingrediente, comunidade | Publicidade e branded content | Excesso de anúncios; receitas sem moderação técnica; não separa receitas já feitas |
| **Panelinha** (BR) | Receitas testadas, técnica, educação alimentar | Livros, cursos, TV e parcerias | Sem app estruturado; não cruza sobras com o acervo |
| **SuperCook** (EUA) | Busca reversa pela despensa, entrada por voz | Freemium e anúncios | Cadastro manual cansativo; tradução ruim; pedido de exclusão permanente de alérgenos |
| **Samsung Food** (ex-Whisk) | Planejamento semanal, nutrição, importação de receitas | Freemium (Food+ US$ 6,99/mês) | Tradução ruim; quantidades da despensa; sem integração com o varejo BR |
| **Mealime** (Canadá) | Planejamento em até 30 min, lista de compras | Freemium | ⚠️ **Encerramento anunciado para 21/10/2026** *(Perplexity, com base na Play Store)*. O Gemini trata o app como ativo. |
| **ChatGPT / Gemini** | Conversa flexível, foto da geladeira, substituições | Assinatura genérica | "Alucinação culinária" (tempo, proporção, alérgeno); sem lista e sem despensa persistentes |
| **Assistentes de marca no WhatsApp** | Foto da geladeira vira receita, sem baixar app | Marketing de marca | Sem dados *(só no Gemini: "Jornada da Geladeira" da Qualy, "Leitura da Geladeira" da Perdigão)* |
| **Cookpad** | Importa receitas de Instagram, TikTok e sites | — | *(só no Perplexity)* |

**Leitura estratégica:** os portais nacionais têm audiência e confiança, mas inovam pouco. Os apps internacionais têm boa tecnologia, mas não são localizados para o Brasil. A IA genérica ocupou o espaço do meio, mas sem despensa persistente e sem garantia de segurança. *(ambos)*

## 4. Gaps e oportunidades

1. **Despensa que se mantém correta.** Reconhecer na entrada não resolve, o problema é manter o estoque atualizado. → **Inventário aproximado e fácil de corrigir** ("pouco", "suficiente pra uma refeição", "confirmar"), sem prometer controle perfeito. *(ambos; a solução é do Perplexity)*
2. **Aproveitamento de verdade.** "Gerar receita com cenoura" é diferente de "consumir a cenoura antes que estrague". → Priorizar o que precisa ser consumido e **planejar o resto da embalagem na próxima refeição**. *(ambos)*
3. **Restrições confiáveis.** Filtro de dieta todo mundo já tem. → Restrições persistentes por morador, separadas em **preferência, intolerância, alergia e condição clínica**. As críticas funcionam como **regra determinística**, não como instrução de texto para o modelo. *(Perplexity)*
4. **Da descoberta à execução.** → Histórico com os estados **quero fazer, planejado, feito e faria de novo**. O produto aprende com o que foi preparado, não com cliques. *(Perplexity)*
5. **Planejamento flexível.** Cardápio rígido de segunda a domingo quebra no primeiro imprevisto e leva ao abandono. → Plano que se adapta. *(Gemini)*
6. **Localização brasileira.** Medidas, ingredientes (feijão, mandioca) e substituições locais. *(ambos)*

## 5. Tecnologia de entrada

| Entrada | Situação |
|---|---|
| **Foto da geladeira** | Atrativa, mas imprecisa (luz, potes opacos, itens empilhados). **Exige que o usuário confirme.** Cobertura de classes não é o mesmo que precisão: a Samsung reconhece 37 tipos de alimento, mas isso não significa 37% de acerto. *(ambos)* |
| **NFC-e (QR Code do cupom)** | Específico do Brasil. Já é usado em apps de lista de compras (Anotadíssimo, Listaki, PoupaMercado). O desafio está nas abreviações dos caixas, e a compra registra aquisição, não consumo. O Gemini fala em "precisão absoluta"; o Perplexity diz que não há benchmark. → **Hipótese a testar, não algo resolvido.** |
| **Voz** | Útil com as mãos ocupadas. O SuperCook já oferece. O Gemini cita >95% de acerto, mas o Perplexity não encontrou benchmark para pt-BR. → Não usar esse número. |

**Recomendação:** combinar o comprovante com uma confirmação simples, o histórico de preparo e as correções do usuário. *(Perplexity)*

## 6. Desafios e riscos

- **Diferenciação:** "gerar receita com IA" sozinho é uma proposta frágil. As barreiras defensáveis são a **localização brasileira, a confiança editorial, o inventário de baixo esforço e a continuidade entre planejamento e preparo**. *(Perplexity)*
- **Retenção:** não há dado público de retenção de apps de receita brasileiros. O Gemini cita D1 de ~26%, D7 de ~13% e D30 de 3% a 3,7% para Food & Drink em geral. ⚠️ É só referência genérica. **Cadência:** o planejamento é semanal (fim de semana), e push diário irrita. *(Gemini)*
- **Monetização:** a publicidade sustenta o acesso grátis, mas é a principal reclamação. A propensão a assinar app de culinária é baixa no Brasil. O caso Mealime serve de alerta de continuidade. *(ambos)*
- **Custo de IA:** imagem, OCR, voz e geração por requisição. → Usar **busca estruturada** para receitas e **regras determinísticas** para restrições, e deixar a geração para adaptação, explicação e conversa. Medir o custo por refeição efetivamente preparada. *(Perplexity)*
- **Segurança alimentar:** a IA erra tempo e temperatura (risco de Salmonella) e ignora alérgenos. Requisitos: não inferir frescor por foto, não apresentar validade estimada como confirmada, confirmar ingredientes ambíguos antes de aplicar restrições e não garantir ausência de alérgeno. *(ambos)*
- **LGPD:** a foto da geladeira e o cupom de farmácia expõem dado de saúde (remédios, insulina, GLP-1). → Minimizar a coleta, permitir exclusão e deixar clara a finalidade. *(ambos)*

## 7. Implicações para o produto

O Perplexity sugere começar por uma tarefa estreita:

> **"O que consigo preparar hoje, com pouco esforço e sem comprar desnecessariamente?"**

| Prioridade | Experiência a testar | Métrica |
|---|---|---|
| Decisão imediata | Poucas sugestões compatíveis com ingredientes, tempo e equipamentos | Sugestão convertida em preparo |
| Despensa simplificada | Voz, foto ou NFC-e com confirmação rápida, sem inventário completo obrigatório | Tempo de cadastro e de correção |
| Aproveitamento | Priorizar itens que precisam ser consumidos | Uso efetivo desses itens |
| Histórico útil | Separar salvo, planejado, feito e aprovado | Uso em semanas consecutivas |
| Restrições confiáveis | Perfis persistentes com confirmação de itens incertos | Violações críticas |
| Localização | Medidas, ingredientes e substituições locais | Aceitação sem adaptação |

**Testes mais importantes antes de investir em reconhecimento automático:** a pessoa aceita corrigir a captura? O estoque continua correto o suficiente? A sugestão vira comida preparada?

## 8. O que muda no doc 01 (Problemas & Oportunidades)

- **Concorrência:** incluir os assistentes de marca no WhatsApp e o encerramento do Mealime
- **Como a IA pode ajudar:** incluir a NFC-e como entrada (hipótese) e o inventário aproximado
- **Pontos de atenção:** incluir LGPD (dados de saúde em fotos e cupons)
- **Premissa 3** (o usuário não mantém a despensa atualizada): **confirmada** pelas duas pesquisas
