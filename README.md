# Briv.IA — Templates

Versão 1.4.3. Plugin privado com três skills independentes e dois modelos auxiliares de otimização. Usa o app Figma existente; não hospeda servidor próprio. A integração e os arquivos precisam estar acessíveis na conversa de execução. A base de conhecimento é fornecida pelo contexto ou pelas fontes conectadas, não embutida neste pacote.

## O que contém

- `skills/otimizar-templates-briv-ia/SKILL.md`: fluxo completo com as 26 seções originais revisadas e contexto de execução.
- `references/indice-templates.md`: modelo de índice fora das artes, com observações, capacidade aproximada e resultados de testes.
- `references/registro-validacao.md`: mapeamento, duas referências de comparação, integridade textual e justificativas por máscara.
- `skills/organizador-de-assets-briv-ia/SKILL.md`: organização externa de nomes, posições e sections para posts, banners, e-mails e outros materiais, sem alterar o interior ou dimensões das artes.
- `skills/otimizador-de-emm/SKILL.md`: reconstrução semântica de e-mails em cópias, seções escaláveis, componentes compartilhados e validação visual e de crescimento.
- `.app.json`: vínculo com a integração Figma verificada no ambiente de criação.

## Uso

Selecionar o plugin e indicar o arquivo/página ou peças do Figma, exclusões, referência aprovada e base pertinente. Na skill geral, sem indicação de modo parcial, a otimização é completa. Para conversão estrutural de e-mails/EMM, usar a skill especializada e seu escopo próprio. Na primeira execução, trabalhar em cópias; na continuação, melhorar as cópias existentes. Para avaliação sem edição, pedir “somente análise”.

No fluxo geral de otimização, assets reutilizáveis são organizados por padrão em uma página existente sem alterar seu conteúdo anterior. Para desativar, dizer “não organizar a biblioteca de imagens”. O índice fica fora das artes e identifica o que foi observado, testado e não testado. Falta de ferramenta ou acesso deve aparecer como limitação, nunca como operação concluída.

## Escolha da skill

- Para otimizar e-mails: usar “Otimizador de EMM”. Reconstrói uma cópia ao lado por seções simples em auto-layout real, usa a largura padrão do cliente, textos Fill/Hug, pixels inteiros, header/footer compartilhados e zero camadas ignorando layout no corpo. A otimização gráfica completa da skill geral é aplicada somente ao banner; o procedimento pixel perfect de tipografia, dimensões e posições vale para todo o e-mail. Inclui comparação visual de cada modelo e ensaios de crescimento de texto, listas, componentes e troca independente de imagem.

- Para otimizar peças: usar “Otimizar templates Briv.IA”. Além da estrutura, exige tamanhos de fonte, dimensões e posições inteiros, entrelinhas explícitas em 100%, 110%, 120%… e tracking com no máximo uma casa decimal. Inspeciona formatos nominais e corrige microdesvios comprovados de até 3 px e 0,5% por eixo. Preserva família e estilo de fonte e registra exceções.
- Para organizar a página/board: usar “Organizador de assets Briv.IA”. Renomeia frames principais e organiza posição das peças, hierarquia, nomes, estilo, tamanho e posição das sections. Não altera conteúdo, tipografia, geometria interna nem dimensões das artes. Os padrões do organizador estão contidos na própria skill; não exige o arquivo de referência original.
- Quando ambos forem solicitados: otimizar as peças e depois fazer a organização final da página, respeitando o escopo de cada skill.

## Origem e revisão

Baseado na leitura integral de `otimizar-templates-briv-ia.txt`, preservando os princípios e as 26 seções. Alterações consolidadas:

1. Biblioteca de imagens no fluxo completo por padrão, desativável pelo usuário.
2. Substituição prioritária de máscaras herdadas; identificação e justificativa de cada máscara restante.
3. Fundo, filtro/degradê nativo e pessoa com transparência real separados para substituições independentes.
4. Comparações por etapa com estado anterior e fidelidade final com referência aprovada, prevalecendo a arte refeita pelo usuário quando aprovada.
5. Conferência objetiva de conteúdo, ordem, pontuação, destaques e quebras intencionais após separar textos.
6. Grupos como unidades de edição conjunta, evitando camadas soltas e wrappers sem função.
7. Índice de seleção com finalidade, formato, blocos de texto, imagens, capacidade observada, campos, limitações e adaptações.

Os arquivos de origem e as peças do Figma não foram modificados na criação deste plugin. Este pacote contém instruções e modelos vazios de registro, não uma otimização já executada nos templates.

A versão 1.1.0 adiciona normalização tipográfica/geométrica à otimização e incorpora o fluxo de `organizador-assets.txt` como skill independente. O organizador mantém os padrões de nomes, hierarquia, estilos e espaçamentos do material de referência, ampliados para todos os tipos de materiais do Briv.IA.

A versão 1.2.0 adiciona a skill “Otimizador de EMM” com o texto fornecido pelo usuário, em Markdown, e contexto para sua seleção no plugin. As duas skills anteriores permanecem disponíveis; o fluxo de e-mails não reorganiza a página nem executa automaticamente a otimização geral.

A versão 1.4.0 consolida a reconstrução semântica como solução de e-mails, com a otimização gráfica limitada ao banner e nomenclatura de e-mail “Modelo N - Tipo”. As regras dos demais canais e a integração Figma permanecem preservadas.

A versão 1.4.1 simplifica a organização externa somente em páginas dedicadas a e-mails (E-mail, EMM ou equivalente): sections de modelos diretamente na página, lado a lado, sem níveis de editoria/categoria ou tipo/formato. Usa padding de 200 px, gap de 100 px entre e-mails da mesma section e de 200 px entre sections, conforme a referência LAFE. Preserva agrupamentos explícitos de modelos e a identificação individual de cada frame. O Otimizador de EMM aplica essa exceção ao chamar o organizador; as demais páginas mantêm as regras gerais.


A versão 1.4.2 torna a normalização pixel perfect obrigatória nas duas skills de otimização, inclusive em todo o e-mail. Converte entrelinhas em px/AUTO para percentuais múltiplos de 10 a partir de 100%, escolhendo a altura mais próxima da original com a fonte final inteira. Exige dimensões, posições e medidas de layout inteiras, com tracking como única medida que admite até uma casa decimal. Inclui varredura de formatos e microcorreção de até 3 px e 0,5% por eixo, preservando o fluxo Hug dos e-mails. Frações ou impedimentos restantes são pendências, sem declaração de conformidade integral.

A versão 1.4.3 reforça a simplificação de listas, bullets e checkboxes na skill geral: uma linha horizontal por item com ícone e texto diretos, texto Fill/Hug e pilha vertical sem wrappers compensatórios. Exige contenção e crescimento dos containers e do suporte. Em listas com entrelinha inflada pela importação, usa entrelinha compacta (em geral 120% ou 130%) e separa os itens pelo gap vertical; essa correção estrutural prevalece sobre aproximar a entrelinha artificial original. Inclui testes de texto curto, multilinha e crescimento intermediário. A referência LAFE observada usa 24 px de gap, sem transformar esse valor em padrão universal.
