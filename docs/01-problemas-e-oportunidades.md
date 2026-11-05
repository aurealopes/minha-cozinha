# Minha Cozinha: Problemas & Oportunidades

## Nome da iniciativa
Minha Cozinha: assistente de refeições com IA
*(alternativa: Minha Cozinha: planejamento de refeições sem desperdício)*

## Descrição
Usar IA para ajudar quem cozinha no dia a dia a transformar os ingredientes que já tem em refeições viáveis, reduzindo desperdício, compras desnecessárias e a dependência de comida pronta.

## Objetivo do negócio/produto
- Ajude quem cozinha no dia a dia a decidir o que preparar com o que já tem em casa
- Reduza o desperdício de alimentos e as compras desnecessárias
- Crie um hábito de uso recorrente, com várias refeições por semana
- Gere receita com um modelo freemium (assinatura para planejamento semanal e lista de compras inteligente)

## Premissas e princípios
- **Premissa:** Durante a semana, a pessoa tem no máximo uns 40 min para cozinhar
- **Premissa:** Tempo e custo pesam mais na escolha do que variedade
- **Premissa:** O usuário não vai cadastrar a despensa manualmente nem manter isso atualizado *(confirmada no desk research)*
- **Premissa:** A pessoa já busca receita em sites, redes sociais e IAs genéricas, e o produto compete com esse hábito
- **Princípio:** Viável agora > receita perfeita
- **Princípio:** Instrução clara > repertório grande
- **Princípio:** Menor esforço possível para informar o que tem em casa
- **Princípio:** A IA sugere e explica, a pessoa decide

## Restrições e pontos de atenção
- Concorrência com IAs genéricas (ChatGPT, Gemini), com sites e redes de receita (TudoGostoso, Panelinha, TikTok, Instagram) e com assistentes de marcas no WhatsApp (Qualy, Perdigão)
- Baixa retenção histórica de apps de receita (o pessoal baixa e desinstala); 
- Precisão do reconhecimento de ingredientes por foto ou nota fiscal
- Risco de a IA gerar receita que não funciona ou com erro de medida e tempo
- Segurança alimentar: alergias, restrições e validade dos alimentos
- Custo de processamento da IA por uso, que pesa num modelo freemium
- LGPD: fotos da geladeira e cupons fiscais podem expor dados de saúde (remédios, insulina)
- Premissas baseadas em pesquisa de 2021 + benchmarking atual; validação com usuários prevista no teste do protótipo

## Como a IA pode ajudar?
- Reconhecimento de ingredientes por foto da geladeira, voz ou QR Code da NFC-e (hipótese a testar), sempre com confirmação do usuário
- Inventário aproximado e fácil de corrigir ("pouco", "suficiente"), sem exigir controle perfeito da despensa
- Sugestão de receitas com o que tem em casa, considerando tempo e orçamento
- Sugestões que respeitam automaticamente o perfil alimentar (restrições, alergias e preferências)
- Priorização de ingredientes perto de vencer, para reduzir desperdício
- Substituição de ingredientes e conversão de medidas no contexto da receita
- Assistente conversacional durante o preparo, para tirar dúvidas de técnica e ponto
- Planejamento semanal e lista de compras com base no histórico e nas preferências

## Para a fase de funcionalidades
- Perfil alimentar em 4 níveis (preferência, intolerância, alergia, condição clínica); restrições críticas como regra determinística, não instrução ao modelo (ver [02-desk-research](02-desk-research.md))

---
Base: [case original de 2021](https://aurealopes.notion.site/Minha-Cozinha-4355b686b1fc47ed833cb706725863bc) (curso de UX da Awari)
