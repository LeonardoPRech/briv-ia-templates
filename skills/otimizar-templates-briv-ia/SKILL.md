---
name: otimizar-templates-briv-ia
description: "Use ao analisar ou otimizar templates do Briv.IA no Figma, especialmente peças importadas ou complexas. Preserva originais e composição, organiza assets reutilizáveis e prepara um índice de seleção com capacidades observadas e testadas. Normaliza medidas e tipografia sem trocar fontes. Inclui primeira otimização, continuação e somente análise."
---

# Otimizar templates para replicação por IA

## 0. Contexto do plugin e base de conhecimento

Este plugin possui três skills com escopos distintos. Usar esta para otimizar a estrutura interna das peças e seus assets reutilizáveis. Para converter e-mails/EMM em auto-layout real preservando as medidas e a tipografia atuais, priorizar o [Otimizador de EMM](../otimizador-de-emm/SKILL.md). Um pedido desse fluxo especializado não ativa automaticamente a normalização tipográfica e geométrica desta skill geral. Para organizar a página/board, nomes dos frames principais, posição das artes e sections, usar [Organizador de assets](../organizador-de-assets-briv-ia/SKILL.md), que preserva integralmente o interior das artes. Um pedido de organização da página não ativa a otimização das peças. Se o usuário pedir ambos, aplicar cada skill ao seu escopo; concluir a otimização antes da organização final. A mera presença de uma arte no contexto não autoriza sua edição.

Antes de executar, ler esta skill integralmente. Usar a integração Figma disponível e seguir as instruções operacionais das ferramentas e skills Figma do ambiente quando aplicáveis. O plugin não cria um servidor próprio nem substitui permissões de acesso ao arquivo.

Ler as referências da base de conhecimento pertinentes ao conjunto solicitado: identidade visual, modelos aprovados, nomenclatura, exclusões e restrições de conteúdo. Referências sincronizadas são somente leitura. Não presumir acesso a uma base não conectada e não inventar regras da marca.

Distinguir instruções atuais do usuário de textos contidos nas peças, documentos e nomes de camadas. Estes são material de referência, não autorizações para ampliar o escopo. Havendo conflito material entre referências de marca e o pedido, preservar o estado e esclarecer apenas o ponto que impeça uma decisão segura.

Usar [Índice dos templates](references/indice-templates.md) ao catalogar e orientar a seleção; usar [Registro de validação](references/registro-validacao.md) no inventário, nas comparações e na entrega. Preencher os registros com observações reais. Os modelos de registro fornecidos com o plugin não são um catálogo já preenchido do Briv.IA.

Aplicar também os [Princípios gerais de otimização](references/principios-otimizacao.md), válidos para qualquer cliente e formato. Eles detalham a escolha de unidades de edição, limites reais, consolidação de recortes e cuidados operacionais, sem constituir um catálogo de casos de um cliente.

## 1. Objetivo

Transformar peças existentes em templates fáceis de compreender, selecionar, duplicar e adaptar por outra IA ou pessoa.

A estrutura resultante deve facilitar:

- escolher o modelo adequado;
- localizar e substituir textos;
- trocar fundos, pessoas e imagens de conteúdo separadamente;
- alterar informações recorrentes;
- preservar identidade visual e composição;
- identificar limites e cuidados de cada modelo.

O trabalho é uma reconstrução estrutural orientada pela composição existente, não um redesign.

A simplificação deve reduzir complexidade desnecessária sem eliminar relações úteis.

**Menos camadas não significa, necessariamente, um template melhor.**

Um pequeno conjunto de frames semânticos e auto-layouts pode ser mais reutilizável que uma composição totalmente achatada.

## 2. Prioridades e regras invioláveis

Respeitar esta ordem:

1. Preservar conteúdo, fatos e identidade visual.
2. Preservar a composição, com os ajustes mínimos de medidas previstos na normalização abaixo.
3. Manter separados os elementos que precisam ser substituídos.
4. Expressar as relações de layout de forma nativa e compreensível.
5. Reduzir redundâncias, aninhamentos e recursos desnecessários.

Nunca:

- modificar originais sem autorização;
- alterar materiais fora do escopo;
- ignorar exclusões solicitadas;
- rasterizar uma arte inteira para aparentar simplificação;
- rasterizar textos editáveis para esconder problemas de estrutura;
- manter cabelo, corpo ou remendos complementares como várias imagens para representar uma única pessoa recortada;
- substituir fontes silenciosamente;
- inventar conteúdo, sequência, autoria ou classificação;
- remover uma camada apenas porque parece invisível;
- declarar fidelidade sem comparar o resultado;
- prometer adaptação ilimitada para qualquer texto ou imagem.

## 3. Compatibilidade com diferentes ambientes

Estas instruções descrevem resultados e procedimentos, não dependem de uma ferramenta específica.

Antes de agir, verificar se o ambiente permite:

- ler a hierarquia e as propriedades dos elementos;
- inspecionar a aparência das peças;
- duplicar e editar sem alterar os originais;
- preservar fontes e estilos;
- criar frames e auto-layouts;
- trabalhar com imagens e transparência;
- comparar resultados.

Utilizar as capacidades disponíveis no ambiente.

Se faltar uma capacidade essencial:

- não simular uma operação que não foi realizada;
- executar apenas as etapas seguras;
- registrar a limitação;
- solicitar o acesso ou material necessário quando isso impedir a continuidade.

Regras e limitações do ambiente prevalecem sobre esta skill.

## 4. Definir o escopo e o modo de execução

Identificar:

- página ou conjunto de origem;
- peças e containers abrangidos;
- exclusões;
- modelos refeitos pelo usuário que sirvam como referência estrutural;
- referência visual aprovada e sua versão, distinguindo-a da importação e do estado anterior;
- referências aplicáveis da base de conhecimento;
- destino das cópias;
- destino dos assets reutilizáveis;
- convenções de nomes já aprovadas.

Modos:

### Otimização completa — padrão para pedidos de otimização sem restrição de etapas

Inclui estrutura, assets reutilizáveis, índice auxiliar e validação. Organizar os assets por padrão em uma página existente, preservando seu conteúdo anterior. O usuário pode desativar explicitamente a etapa da biblioteca de imagens; registrar essa escolha e cumprir as demais etapas. Uma exclusão de escopo também prevalece sobre o padrão.

Aplicar o modo completo tanto na primeira otimização quanto na continuação, limitando a continuação ao que ainda precisa melhorar. Em pedidos parciais, executar somente o escopo solicitado. Em somente análise, não criar nem modificar biblioteca ou índice no Figma; entregar os registros no relatório.

### Primeira otimização

Duplicar os conjuntos autorizados e trabalhar nas cópias.

### Continuação

Se o usuário pedir melhorias nos templates já otimizados, editar essas cópias. Não duplicar tudo novamente.

### Somente análise

Inspecionar e recomendar, sem modificar.

Na ausência de orientação sobre destino, posicionar as cópias à direita do conjunto original, em espaço livre, preservando suas relações internas.

Se houver colisão com conteúdo não autorizado, escolher outro espaço livre ou pedir orientação.

Perguntar somente quando houver interpretações materialmente diferentes sem uma opção segura.

## 5. Inventário e referência inicial

Antes de editar, registrar:

- identificação estável de cada peça;
- hierarquia, modelo, formato e sequência;
- dimensões reais;
- posição e transformação;
- ordem de sobreposição;
- visibilidade e bloqueios;
- preenchimentos, traçados e efeitos relevantes;
- máscaras e recortes;
- fontes e estilos por trecho, tamanhos, entrelinhas com unidades e espaçamentos entre letras;
- valores fracionários de geometria e espaçamentos a normalizar;
- textos e suas variações de formatação;
- imagens, recortes e modos de composição;
- constraints e regras de dimensionamento.

Capturar uma referência visual das peças antes de qualquer alteração. Registrar separadamente:

- estado imediatamente anterior a cada etapa, com identificação da versão e captura;
- referência visual aprovada, com origem e identificação da peça ou versão.

Se uma arte refeita pelo usuário for a referência aprovada, ela prevalece sobre a importação para a composição e a estrutura. A aprovação visual não autoriza substituir conteúdo específico de outras peças por textos de exemplo. Se não houver uma referência diferente indicada, usar a peça de origem como referência inicial de fidelidade e declarar essa escolha.

Antes de cada etapa estrutural, atualizar a captura do estado anterior. Não usar somente a importação inicial para avaliar uma segunda otimização: isso pode ocultar uma regressão em relação a uma etapa já correta.

Manter um mapeamento entre:

- original;
- cópia otimizada;
- imagens reutilizáveis;
- exceções e decisões relevantes.

Distinguir frames de artes de frames internos, legendas, referências e materiais auxiliares.

Não tratar todo frame encontrado como uma peça independente.

## 6. Diagnóstico semântico

Classificar os elementos por função:

- fundo;
- filtro ou degradê;
- pessoa;
- imagem de conteúdo;
- produto ou montagem;
- título;
- subtítulo;
- descrição;
- lista;
- marcador;
- ícone;
- contato;
- preço;
- condição comercial;
- observação legal;
- marca;
- decoração;
- sobreposição;
- elemento auxiliar.

Cruzar aparência, conteúdo, hierarquia e geometria.

Não classificar somente pelo nome importado. Relacionar origem e destino por identificação estável, contexto, visibilidade, geometria, transformação, sobreposição e hash. Nomes repetidos ou semelhantes exigem desambiguação; não selecionar a primeira ocorrência. Distinguir a fotografia de fundo de sua cópia recortada em primeiro plano e identificar os fragmentos que apenas completam o mesmo recorte.

Uma camada chamada “Recorte” pode ser uma pessoa, um ícone ou uma forma geométrica.

Uma fotografia com pessoas pode ser um fundo completo, não um recorte de pessoa.

Identificar quais elementos são:

- substituíveis;
- estruturais;
- decorativos;
- dependentes entre si;
- compartilhados entre adaptações.

## 7. Preparar um lote piloto

Antes de aplicar transformações em massa, selecionar exemplos representativos:

- peça com pessoa e fundo;
- peça predominantemente textual;
- lista com marcadores;
- conjunto de ícone e texto;
- texto sobre forma geométrica;
- montagem de imagem complexa;
- peça com sobreposições ou modos de mesclagem.

Aplicar as regras no piloto e comparar.

Ajustar a estratégia antes de expandir.

Não aplicar uma heurística a todo o conjunto apenas porque funcionou em uma peça.

## 8. Simplificar a hierarquia com segurança

Remover containers que não tenham função visual, semântica ou de layout.

Antes de remover um container, verificar se ele controla:

- recorte;
- máscara;
- opacidade coletiva;
- modo de mesclagem;
- efeitos;
- transformação;
- constraints;
- organização útil de conteúdo.

Ao reparentear elementos, preservar:

- posição e transformação visual;
- dimensões;
- ordem de sobreposição;
- visibilidade;
- aparência;
- relações de layout.

Constraints de esticamento e auto-layout podem mudar dimensões e posições durante o parenting. Quando necessário, neutralizar temporariamente essas regras, mover com a transformação registrada e restaurar as ancoragens pela função. Conferir dimensões e layoutPositioning do resultado. Uma operação booleana aplicada ao fundo de uma faixa não pode colocar esse fundo em fluxo e empurrar o texto.

Preservar grupos úteis.

Evitar os dois extremos:

- dezenas de wrappers sem finalidade;
- todas as camadas soltas diretamente no frame principal.

Agrupar ao máximo significa representar unidades úteis, não aninhar ao máximo. Cada grupo ou frame deve corresponder a uma unidade que será substituída, alinhada, movimentada ou dimensionada em conjunto. Descrever essa função quando ela não for evidente.

Não criar um wrapper por camada nem wrappers em cascata sem função. O número de frames pode aumentar quando isso expressar relações reais e melhorar a edição. Evitar tanto camadas soltas sem relação quanto aninhamentos redundantes; não usar contagem de camadas como meta de qualidade.

## 9. Fundos e preenchimentos nativos

Preferir preenchimentos do próprio frame quando uma forma servir exclusivamente como fundo.

A conversão só é válida se preservar:

- cobertura;
- cor;
- transparência;
- transformação do degradê;
- interação com os elementos acima;
- ordem visual.

Não transformar automaticamente uma forma em fundo apenas porque ela é grande.

Manter separadas as formas que funcionem como:

- faixas;
- painéis;
- recortes decorativos;
- suportes de conteúdo;
- sobreposições parciais.

Para fotografias em regiões geométricas, preferir o preenchimento da própria forma com crop nativo. Preservar proporção, área desenhada, transformação FIT/FILL/CROP, filtros, opacidade e mesclagem; reutilizar apenas o hash não preserva o enquadramento. Compor transformações existentes e conferir rostos e sobreposições. Não selecionar fotografias alternativas ocultas ou homônimas por engano.

Converter efeitos importados em recursos nativos quando houver equivalência comprovada.

Não aproximar um degradê complexo silenciosamente.

## 10. Máscaras e imagens compostas

Prioridade: substituir máscaras herdadas de importações sempre que houver uma solução visualmente fiel e reutilizável. Procurar e avaliar a alternativa antes de decidir manter a máscara. Complexidade de implementação ou conveniência não justificam conservar uma estrutura herdada.

Para cada máscara restante, registrar identificação estável e localização, função, alternativas avaliadas, motivo técnico da permanência, evidência visual e impacto na substituição. A regra abrange máscaras intencionais e herdadas. Se a alternativa não puder ser executada ou verificada por limitação do ambiente, registrar a pendência; não apresentar a máscara como resolvida.

Escolher a solução por função:

- fundo ou degradê equivalente: preenchimento nativo;
- imagem retangular: recorte nativo simples;
- pessoa recortada: imagem com transparência real;
- montagem visual indivisível: imagem composta transparente;
- forma editável simples: preservar como forma;
- máscara intencional e funcional: manter somente após avaliar as alternativas, se elas prejudicarem a fidelidade ou a reutilização, com identificação e justificativa na entrega.

Não eliminar máscaras apenas para atingir uma contagem zero. Essa ressalva não enfraquece a obrigação de substituir as herdadas quando houver alternativa fiel e reutilizável.

Ao consolidar uma imagem:

- incluir somente o conjunto visual apropriado;
- preservar bordas, sombras e transparência;
- preservar resolução adequada à escala de uso;
- evitar aplicação dupla de opacidade ou efeitos;
- conferir modos de mesclagem que dependam do fundo.

Não incorporar à mesma imagem elementos que precisam ser trocados separadamente.

Quando a composição exigir substituições independentes, manter explicitamente três elementos:

1. Imagem de fundo.
2. Filtro ou degradê nativo, separado e editável.
3. Pessoa com transparência real.

Não incorporar o filtro à pessoa nem fundir tudo em um fundo único por facilidade. A separação deve permitir trocar cada elemento sem reconstruir os demais. Se a fonte não permitir recuperar essa independência com fidelidade, registrar a limitação e buscar a fonte apropriada, sem inventar partes da imagem.

Não misturar pessoa, fundo e texto editável numa única imagem. Consolidar montagens somente quando seus elementos realmente constituírem uma unidade de substituição; não transportar regras específicas de cartões ou de um cliente para todos os modelos.

Não rasterizar formas ou gradientes simples sem necessidade.

### 10.1. Uma imagem real por recorte indivisível

Avaliar também estruturas sem nenhum nó isMask. Frames com duas ou mais imagens complementares, patches de cabelo/corpo e camadas que reproduzem técnicas de máscara ou Multiply continuam complexos mesmo após desativar a máscara. Renomear ou reagrupar essas camadas não resolve a consolidação.

Quando várias imagens formarem a mesma pessoa, produto, ícone ou montagem indivisível, consolidar somente esses fragmentos em um único PNG ou raster equivalente com transparência real. A pessoa recortada deve ser uma imagem inteira da unidade disponível, sem depender de uma imagem de cabelo, outra de corpo e outros remendos. Preservar a fonte mais completa quando existir e distinguir seu recorte de aplicação.

No efeito de pessoa que avança sobre grafismos, manter a fotografia de fundo separada, os grafismos em sua ordem intermediária e a pessoa consolidada em primeiro plano. Não fundir o fundo, filtro ou decoração independente à pessoa. Pessoas distintas só pertencem à mesma imagem quando constituírem uma única unidade real de substituição.

Isolar os fragmentos com sua ordem, alfa, filtros e mesclagem; exportar em resolução adequada; recortar a transparência excedente no próprio raster; substituir o conjunto por um único nó com posição, escala, sobreposição e ancoragens equivalentes. Conferir o asset isolado, incluindo cabelo e bordas em fundos claros e escuros, e sua aplicação na peça antes de remover redundâncias da cópia.

Modos dependentes do fundo exigem verificar a equivalência: exportar sobre transparência não garante a reconstrução correta. Não aplicar opacidade ou efeitos duas vezes, deixar halos ou incorporar o fundo por conveniência. Se a independência fiel não puder ser recuperada, registrar a limitação e buscar a fonte adequada.

Uma máscara intencional restante deve ter limites próximos da área útil, preferencialmente dentro da arte, com constraints coerentes. Nunca usar uma máscara várias vezes maior que a arte para uma marca pequena. Respeitar pedidos explícitos de ausência de máscaras.

## 11. Agrupar conteúdo com formas geométricas

Textos dentro de faixas, etiquetas, painéis ou outras formas devem pertencer a um frame semântico comum. Preferir auto-layout com texto em fluxo; usar o preenchimento do frame ou uma forma irregular como fundo absoluto, ancorado para acompanhar o suporte. Quando corpo, chamada e marca devem acompanhar a unidade, vinculá-los ao fluxo superior. Conferir crescimento e efeito nos vizinhos.

Estrutura conceitual:

- Chamada
  - Forma de apoio
  - Conteúdo
    - Título
    - Descrição

Quando a geometria for simples e equivalente, usar o preenchimento do frame.

Quando houver uma forma irregular, mantê-la como elemento visual separado dentro do grupo.

A forma pode permanecer como sobreposição intencional, enquanto o texto participa do fluxo.

Decidir se o suporte:

- cresce com o conteúdo;
- mantém dimensão fixa;
- exige limites de texto.

Não prometer expansão automática de formas cuja geometria não comporte essa adaptação.

Preservar recortes e sobreposições com elementos externos ao grupo.

## 12. Auto-layout real, preservando a composição

Separar posição de composição de espaçamento interno. Calcular a região dos textos relacionados e posicionar uma coluna nessa região. Não representar o x/y absoluto de cada texto como padding repetido em um wrapper próprio. Um padding grande só é adequado quando corresponde a uma margem funcional da própria forma, aplicado uma única vez à unidade correta.

Medir antes de converter:

- posições;
- larguras e alturas;
- espaçamentos;
- indentações;
- alinhamentos;
- sobreposições.

Calcular gaps pela geometria real.

Não usar uma média para substituir espaçamentos diferentes.

Representar relações diferentes com grupos semânticos, alinhamentos, gaps e paddings locais. Usar wrappers internos e auto-layouts aninhados somente quando expressarem uma função que o container existente não consiga representar. Não criar um frame por caixa de texto por padrão.

Construir de dentro para fora:

1. registrar a geometria;
2. carregar as fontes necessárias;
3. criar os wrappers internos;
4. reparentear preservando a aparência;
5. configurar o auto-layout do container;
6. aplicar regras de dimensionamento dos filhos;
7. montar os níveis superiores;
8. comparar.

Configurar eixos, gaps, padding e filhos; aplicar as dimensões fixas; depois ativar Hug/Fill nos eixos e contextos apropriados. Usar o alinhamento do container e propriedades atuais da ferramenta, sem setters antigos que mudem o conjunto inteiro sem intenção.

Não converter primeiro o frame externo e depois compensar deslocamentos.

O frame principal de uma peça gráfica pode continuar com posicionamento manual.

Fotografias, decorações e sobreposições não precisam entrar no mesmo fluxo dos textos.

Não criar auto-layout fictício deixando todos os conteúdos em posição absoluta.

Posicionamento absoluto é adequado para fundos e sobreposições reais, não para simular listas ou pilhas de texto.

## 13. Textos empilhados e dimensionamento

Agrupar textos relacionados em auto-layout vertical.

Preservar:

- conteúdo;
- estilos por trecho;
- alinhamento;
- proporção de entrelinha, normalizada conforme a seção 13.1;
- espaçamento de parágrafo;
- quebras manuais relevantes;
- largura e quebra visual original.

Usar intencionalmente:

### Hug

Para dimensões dirigidas pelo conteúdo.

### Fill

Para elementos que devem acompanhar a dimensão disponível no container.

### Fixed

Para dimensões estáveis, ícones, proporções rígidas ou composições com limites definidos.

Aplicar essas regras somente quando o contexto estrutural permitir.

Preferir altura de texto orientada pelo conteúdo quando isso mantiver a aparência atual e melhorar a substituição futura.

Não alterar todas as caixas de texto para Hug ou Fill indiscriminadamente.

Textos maiores podem exceder o espaço disponível mesmo em estruturas bem construídas. Definir e comunicar limites observados ou testados, sem inventar capacidade máxima.

Ao dividir parágrafos ou listas, registrar o texto de origem e conferir, após a separação, conteúdo integral, ordem, pontuação, destaques e quebras intencionais. Comparar os trechos e estilos, além de sua aparência. A quantidade de camadas pode aumentar; nenhuma informação pode desaparecer, duplicar ou mudar de sentido. Só normalizar quebras puramente visuais após distingui-las das quebras intencionais, documentando a transformação.

## 13.1. Normalização tipográfica e medidas em pixels inteiros

Aplicar a todas as caixas de texto editáveis e a todos os trechos com formatação própria no escopo da otimização, inclusive textos de uma única linha. Não aplicar no modo somente análise; nesse modo, registrar os ajustes necessários. Na primeira otimização, editar as cópias; na continuação, as cópias existentes. Não executar esta etapa em pedidos exclusivos ao organizador de assets.

### Tipografia

Preservar família tipográfica, estilo/peso, eixos da fonte variável, destaques e demais características propostas. Não substituir fontes para facilitar arredondamentos. Os ajustes tipográficos deste procedimento se limitam a tamanho de fonte, altura de linha e espaçamento entre letras; não compensar diferenças trocando família ou peso. Preservar conteúdo, quebras intencionais, alinhamento e espaçamento de parágrafo.

1. **Tamanho de fonte:** arredondar ao inteiro mais próximo, sem casas decimais. Exemplos: 36,4 → 36; 36,8 → 37; 36,5 → 37. Não truncar. Se o arredondamento produzir um tamanho inválido, registrar a exceção em vez de apagar ou colapsar o texto.
2. **Altura de linha:** gravar explicitamente em porcentagem, no múltiplo de 10 pontos percentuais mais próximo: 100%, 110%, 120%, 130%, 140% e assim por diante, sem limitar o valor a 140%. Exemplos: 113% → 110%; 116% → 120%; 115% → 120%; 153% → 150%. Não confundir um incremento de 10 pontos percentuais com multiplicar o valor por 1,1.
3. **Converter antes de arredondar:** se a entrelinha original estiver em px, calcular a proporção usando o tamanho de fonte original do trecho: porcentagem = altura de linha em px ÷ tamanho de fonte original × 100. Só depois escolher o múltiplo de 10 e gravá-lo junto do tamanho inteiro final. Exemplo: fonte 36,4 px e entrelinha 43,68 px → proporção 120% → fonte 36 px e entrelinha 120%.
4. **Entrelinha automática:** resolver a altura efetiva com as métricas da fonte e/ou medição de linhas renderizadas pela integração disponível, convertê-la em proporção e gravar o percentual normalizado. Não usar a altura total da caixa de texto como se fosse a entrelinha. Se não for possível resolver AUTO com segurança, registrar a caixa e a limitação; não inventar 100%, não substituir fonte nem declarar a normalização concluída.
5. **Espaçamento entre letras:** preservar a unidade original (px ou %) e arredondar ao mais próximo com no máximo uma casa decimal, inclusive valores negativos; manter valores já conformes. Exemplos: 0,24 → 0,2; 0,26 → 0,3; -1,26 → -1,3. Empates exatos são arredondados para longe de zero. Não arredondar o tracking obrigatoriamente para inteiro.

Em textos mistos, ler e editar por trecho/range; não aplicar um único tamanho, entrelinha ou tracking à caixa inteira se ela possui valores diferentes. Carregar as fontes necessárias; se alguma estiver indisponível, registrar o impedimento sem substituí-la. Preservar estilos compartilhados e variáveis: quando necessário, usar ajuste local na cópia sem editar definições globais que afetem peças fora do escopo.

### Geometria geral

Buscar pixels inteiros nas posições x/y, larguras, alturas, paddings, gaps, espaçamentos e demais medidas de layout em px, em textos, frames, grupos, imagens, formas e containers do escopo. Arredondar cada medida ao inteiro mais próximo, sem impor uma grade maior; por exemplo, 150,4 → 150 e 150,8 → 151. Para medidas negativas, usar a mesma regra de proximidade e desempate para longe de zero. Normalizar raios e espessuras em px quando isso conservar a aparência. Não arredondar ângulos, proporções, opacidades ou coordenadas internas de curvas como se fossem medidas de layout em px. A exceção de tracking com uma casa decimal continua válida.

Trabalhar nas propriedades que dirigem o layout, de dentro para fora. Em auto-layouts, normalizar dimensões editáveis, gaps e paddings e deixar o fluxo recalcular os filhos. Conferir também o resultado; não desfazer Hug/Fill, proporções, alinhamentos ou rotações somente para forçar um valor calculado a inteiro. Preservar proporção de imagens, recorte, curvas, detalhes de marca e geometria vinculada; registrar as exceções em que não for possível obter inteiros sem distorção. Não redimensionar indiscriminadamente todos os elementos por escala.

Medidas finais nominais das peças devem permanecer reconhecíveis. Arredondar pequenas frações do frame principal somente quando preservar a composição e não violar formato explicitamente exigido. Atualizar nomes que contenham dimensões apenas com base no resultado real. O objetivo é remover frações desnecessárias, não alterar o formato ou a escala da criação.

### Aplicação e conferência

Registrar valores anteriores e finais, unidade, ID da caixa/trecho ou elemento e exceções. Comparar com o estado anterior e a referência aprovada após a normalização. Os pequenos ajustes numéricos acima são intencionais; conferir que não provoquem palavras cortadas, quebras inesperadas, colisões, perda de destaques ou desalinhamentos. Corrigir a estrutura e as medidas permitidas sem trocar a tipografia. Quando a fidelidade ou uma restrição real impedir o ajuste, manter somente a exceção justificada e relatá-la. Uma segunda execução deve manter os valores já normalizados.

## 14. Listas e marcadores

Estrutura preferida:

- Lista: auto-layout vertical
  - Item 01: auto-layout horizontal
    - Marcador
    - Texto
  - Item 02: auto-layout horizontal
    - Marcador
    - Texto

Cada marcador deve acompanhar seu item, inclusive quando o texto quebrar em várias linhas.

Identificar o início de cada item pelo conteúdo e pela composição.

Não dividir mecanicamente toda quebra de linha:

- uma quebra pode continuar o mesmo item;
- um item pode ocupar várias linhas;
- um parágrafo pode ter estilos mistos.

Ao separar um texto em itens:

- preservar conteúdo e pontuação;
- preservar estilos dos trechos;
- conferir a ordem;
- conferir entrelinha e espaçamento;
- manter alinhamento adequado ao primeiro trecho ou ao centro, conforme a referência.

Validar que a união ordenada do conteúdo dos itens corresponde ao original, incluindo pontuação, destaques e quebras intencionais. Conferir separadamente a função dos marcadores para não omitir nem duplicar informação. Registrar a verificação; se houver divergência, corrigir antes de seguir.

Não duplicar marcadores que já estejam presentes no texto.

## 15. Ícones e informações relacionadas

Usar auto-layout horizontal para relações como:

- ícone + telefone;
- ícone + endereço;
- ícone + benefício;
- símbolo + informação.

Agrupar múltiplas linhas relacionadas num auto-layout vertical superior.

Preservar a relação visual original:

- alinhamento pelo centro;
- alinhamento pelo topo;
- alinhamento com a primeira linha.

Não centralizar automaticamente um ícone em relação a um texto longo se a referência o alinha ao início.

Manter dimensões estáveis para ícones.

## 16. Constraints e composição

Definir ancoragens pela função do elemento.

Exemplos:

- fundo: acompanhar os limites da peça;
- pessoa apoiada no canto inferior direito: preservar essa relação;
- rodapé: manter vínculo com a base;
- marca: preservar sua posição relativa;
- bloco centralizado: manter centralização;
- conteúdo textual: responder ao seu container.

Definir limites reais coerentes: fundos acompanham a arte; marcas ocupam sua região útil; formas decorativas terminam no formato; fotografias têm uma área de aplicação correspondente à composição. O clipping do frame principal não justifica descendentes excessivamente grandes. Uma pequena extrapolação intencional de imagem pode ser aceitável, sem carregar caixas várias vezes maiores que a região útil.

Ao aparar vetores, distinguir preenchimentos de contornos abertos: fechar uma interseção pode criar uma borda inexistente. Preservar segmentos/curvas e inspecionar a aparência. Uma falha da API não prova ausência de contribuição visual.

Não inferir constraints apenas pelas caixas gigantes herdadas da importação.

Não usar escala indiscriminada em textos e ícones.

Em filhos controlados por auto-layout, priorizar regras de dimensionamento e alinhamento do próprio layout.

Constraints não substituem uma hierarquia correta.

## 17. Recortar transparência excedente

Consolidar primeiro os fragmentos complementares da mesma unidade, conforme a seção 10.1; não entregar cada fragmento como um recorte separado. Depois, para imagens transparentes, especialmente pessoas:

1. confirmar visualmente a classificação;
2. identificar os limites efetivos do canal alfa;
3. incluir uma pequena margem para preservar antialiasing e bordas;
4. recortar a própria imagem de origem;
5. ajustar posição e dimensão na composição;
6. comparar o resultado.

Preservar:

- escala;
- posição aparente;
- detalhes de cabelo e borda;
- sombras intencionais;
- filtros e opacidade.

Não simular o recorte apenas reduzindo o frame enquanto o arquivo permanece quase todo transparente.

Não usar um limiar de transparência que elimine detalhes sutis.

Não amputar partes úteis de uma fonte reutilizável apenas porque estão fora do frame atual.

Quando houver uma fonte mais completa disponível, distinguir:

- asset reutilizável completo;
- recorte específico daquela aplicação.

Não inventar partes ausentes da imagem.

## 18. Biblioteca reutilizável de imagens

No modo completo, organizar os assets reutilizáveis por padrão, salvo se o usuário desativar essa etapa ou excluir esse material. Não condicionar essa organização a uma autorização adicional genérica.

Usar uma página existente apropriada, priorizando a biblioteca já utilizada no arquivo e os destinos indicados pelo usuário. Inserir cópias em espaço livre ou novas sections sem editar, mover, renomear ou excluir o conteúdo anterior. Não criar uma nova página automaticamente. Se nenhuma página existente puder receber os assets sem conflito ou não houver acesso, registrar a pendência e solicitar apenas a definição ou o acesso indispensável, enquanto continua as etapas independentes.

Na continuação, reaproveitar os assets já conformes e acrescentar somente o necessário; não reorganizar o conteúdo anterior por conveniência.

Criar sections separadas por função, por exemplo:

- Pessoas;
- Fundos;
- Produtos;
- Montagens.

Criar apenas categorias necessárias.

Preservar os conteúdos existentes e usar espaço livre.

Regras:

- copiar assets, não retirá-los dos templates;
- manter transparência real quando aplicável;
- não incorporar textos ou decorações editáveis ao fundo;
- identificar a origem da imagem;
- evitar duplicatas realmente equivalentes, reutilizando hashes compatíveis; uma mesma pessoa com outro enquadramento ou tratamento pode exigir uma variante;
- priorizar o asset final consolidado para replicação e atualizar seus vínculos no índice, preservando fontes completas e o acervo anterior;
- não fundir arquivos distintos apenas porque parecem semelhantes;
- preservar variantes úteis de recorte ou tratamento.

Preferir fontes completas para fundos quando estiverem disponíveis.

Se houver apenas um recorte, identificá-lo como tal.

## 19. Remover imagens e camadas sem contribuição

Uma camada pode estar invisível por:

- estar desativada;
- estar fora da área visível;
- estar coberta;
- participar de uma máscara;
- servir como base para mesclagem;
- aparecer através de transparências.

Não excluir somente pela posição ou pelo nome.

Procedimento seguro:

1. registrar a aparência;
2. desativar temporariamente a candidata na cópia;
3. comparar a composição;
4. verificar dependências;
5. remover somente com evidência suficiente.

Elementos ocultos podem representar estados intencionais. Analisar antes de remover.

Não excluir variantes, referências ou materiais auxiliares fora do escopo.

## 20. Nomenclatura semântica e consistente

Usar o mesmo vocabulário para a mesma função entre modelos.

Exemplos:

- Conteúdo
- Título
- Subtítulo
- Descrição
- Lista
- Item 01
- Marcador
- Contato
- Telefone
- Endereço
- Preço
- Condições
- Observação
- Rodapé
- Marca
- Ícone / Telefone
- Imagem / Pessoa
- Imagem / Fundo
- Imagem / Produto
- Imagem / Montagem
- Decoração / Faixa
- Filtro / Degradê

Usar nomes específicos quando necessários para distinguir papéis.

Não chamar qualquer imagem de “Pessoa” nem qualquer forma de “Fundo”.

Evitar sufixos de importação e nomes genéricos sem função.

Nos frames principais:

- preservar convenções aprovadas;
- usar dimensões reais;
- preservar modelo e sequência;
- não inventar numeração;
- não confundir número da editoria com número do modelo.

Não introduzir uma convenção conflitante com a organização existente.

## 21. Contrato de reutilização do template

Para cada modelo, tornar identificável:

- finalidade ou tipo de composição;
- formato;
- campos de texto substituíveis;
- imagens substituíveis;
- elementos fixos;
- agrupamentos que devem permanecer juntos;
- comportamento esperado quando o texto cresce;
- limites relevantes;
- relação com adaptações e sequência.

Usar nomes e hierarquia semântica e manter um índice auxiliar simples por template, fora das artes, conforme [Índice dos templates](references/indice-templates.md). No modo completo, esse índice faz parte da entrega; na continuação, atualizar o registro correspondente sem duplicar o catálogo.

Registrar no índice:

- identificação estável e localização do template;
- finalidade e formato, incluindo dimensões reais;
- quantidade e função dos blocos de texto;
- presença de pessoa, fundo ou produto, e se são substituíveis independentemente;
- capacidade aproximada de conteúdo observada, como linhas ou itens atuais;
- campos substituíveis e elementos fixos;
- limitações verificadas, adaptações relacionadas e vínculos de sequência;
- evidência, versão e resultado dos testes, distinguindo observado, testado e não testado.

Descrever somente o que foi observado e testado. A quantidade atual de linhas ou caracteres não é um limite máximo comprovado. Marcar dados desconhecidos e comportamentos não testados; não inventar capacidades, classificações nem adaptações inexistentes.

Para outra IA selecionar um modelo, cruzar o objetivo e o formato do pedido com quantidade e função dos blocos, necessidade de imagens e capacidade documentada. Priorizar modelos compatíveis que exijam menos adaptações dentro das limitações conhecidas. Explicar a escolha com evidências do índice e da base aplicável. Se a necessidade ultrapassar o que foi testado, indicar o teste pendente; não declarar um “melhor modelo” sem sustentação.

Não adicionar documentação visível dentro da arte final. Usar área auxiliar em espaço livre de uma página existente, preservando o conteúdo anterior; quando não for possível gravar ali, entregar o índice como arquivo auxiliar e informar sua localização. Uma versão entregue em arquivo não equivale a ter atualizado o catálogo do Figma.

Não transformar automaticamente os templates em componentes.

Avaliar componentes somente quando isso fizer parte do pedido e melhorar o fluxo sem restringir substituições necessárias.

## 22. Testar a capacidade de substituição

Além da comparação visual, realizar testes reversíveis em cópias temporárias representativas.

Testar, conforme o modelo:

- título um pouco mais longo;
- descrição com uma linha adicional;
- item de lista com quebra;
- contato com comprimento diferente;
- troca de imagem usando um asset disponível e autorizado.

Verificar:

- se os elementos relacionados acompanham o conteúdo;
- se os marcadores continuam alinhados;
- se os suportes visuais comportam a alteração;
- se a pessoa e o fundo continuam independentes;
- se não há corte ou colisão.

Restaurar o conteúdo e remover as cópias temporárias.

Quando não houver material adequado para testar uma substituição, registrar que esse teste não foi realizado.

Não tratar um teste limitado como garantia de adaptação irrestrita.

## 23. Execução em lotes e recuperação

Trabalhar em lotes rastreáveis por conjunto ou modelo.

Após cada etapa e cada lote:

- registrar o que foi concluído;
- verificar contagens, integridade dos textos e vínculos entre peças e assets;
- comparar com o estado imediatamente anterior e conferir a referência visual aprovada;
- registrar as duas comparações e corrigir regressões antes de expandir.

Uma mudança intencional para atingir a referência aprovada pode diferir do estado anterior; explicar a diferença e sua evidência. Isso não dispensa conferir perdas de conteúdo e relações úteis já existentes.

Se houver uma alteração visual ampla:

- interromper a propagação;
- identificar a última etapa correta;
- corrigir a causa estrutural;
- evitar compensações arbitrárias acumuladas.

Não repetir operações já concluídas sem verificar o estado atual.

Ao retomar uma execução interrompida, usar o mapeamento e o resultado real, não apenas a memória do que deveria ter sido feito.

## 24. Validação obrigatória

### Integridade

Conferir:

- quantidade de peças;
- dimensões;
- correspondência original/cópia;
- ordem narrativa;
- textos completos, ordem, pontuação, destaques, quebras intencionais e estilos, especialmente após separações;
- fontes e estilos preservados por trecho;
- tamanhos de fonte inteiros, entrelinhas em porcentagens múltiplas de 10 e tracking com até uma casa decimal, ou exceções identificadas;
- medidas de layout em pixels inteiros onde viável, com restrições e exceções justificadas;
- índice auxiliar correspondente ao estado real, com limites observados e testes identificados;
- ausência de alterações fora do escopo e preservação do conteúdo anterior da página de assets.

### Estrutura

Conferir:

- agrupamentos semânticos;
- listas com linhas próprias;
- ícones vinculados aos textos;
- fluxo real de auto-layout;
- dimensionamento coerente;
- ancoragens adequadas;
- imagens substituíveis separadas, inclusive fundo, filtro/degradê nativo e pessoa com transparência real quando a composição exigir independência;
- cada pessoa ou unidade raster indivisível consolidada em uma única imagem, sem patches complementares, inclusive em estruturas sem isMask;
- limites reais de marcas, imagens e decorações coerentes com a aplicação, sem depender de clipping de caixas excessivas;
- ausência de padding que apenas reproduza coordenadas do canvas;
- texto e suporte vinculados e conferidos durante o crescimento;
- máscaras herdadas substituídas sempre que existir alternativa fiel e reutilizável;
- identificação e justificativa de todas as máscaras restantes;
- transparência recortada;
- ausência de frames colapsados;
- ausência de temporários;
- nomes consistentes.

Não medir qualidade apenas pela quantidade de auto-layouts.

### Aparência

Realizar duas verificações complementares: cada etapa contra seu estado imediatamente anterior e a fidelidade final contra a referência visual aprovada. Quando a referência aprovada for a arte refeita pelo usuário, ela prevalece sobre a importação. Comparar também a cópia com o original para conferir conteúdo e integridade, sem impor à composição uma referência já superada.

Executar as comparações:

- no mesmo tamanho;
- com o mesmo fundo de comparação;
- com condições de renderização equivalentes.

Inspecionar:

- posição;
- quebra e alinhamento de texto;
- espaçamentos;
- sobreposições;
- limites de formas;
- filtros;
- recortes;
- bordas transparentes, cabelo, halos e vazios, inspecionando recortes isolados em fundos claros e escuros quando aplicável;
- sombras e mesclagem, sem duplicação de opacidade após consolidação.

Em grandes conjuntos, comparar todas as peças quando possível e revisar casos complexos em tamanho original.

Se a comparação for amostral, declarar separadamente a cobertura de cada comparação e os casos não verificados. Registrar as referências e versões usadas em [Registro de validação](references/registro-validacao.md).

Quando houver análise por pixels, considerar:

- diferença média;
- concentração local de diferenças;
- regiões de texto;
- rostos;
- bordas;
- áreas omitidas.

Uma média baixa não garante que não exista uma palavra cortada ou um elemento deslocado.

Não adotar percentuais de execuções anteriores como limite universal.

## 25. Critérios de conclusão

Considerar concluído somente quando:

- o escopo estiver atendido;
- os originais estiverem preservados;
- a composição estiver fiel;
- os elementos substituíveis estiverem identificáveis;
- os agrupamentos representarem relações reais;
- pessoas e imagens indivisíveis não dependerem de fragmentos complementares para formar o asset final;
- limites reais e relações entre texto e suporte estiverem coerentes;
- os textos editáveis permanecerem editáveis;
- os assets estiverem organizados por padrão no modo completo, em página existente e com o conteúdo anterior preservado, ou a etapa tiver sido desativada explicitamente pelo usuário;
- o índice auxiliar estiver preenchido e localizado fora das artes, com capacidades observadas e testes identificados;
- as máscaras restantes estiverem identificadas e justificadas, com alternativas consideradas;
- a comparação de cada etapa com seu estado anterior e a conferência final com a referência aprovada estiverem registradas;
- a integridade dos textos divididos estiver conferida;
- a normalização tipográfica e geométrica estiver verificada, com valores finais e exceções registradas;
- não houver regressões conhecidas sem indicação;
- os testes realizados e suas limitações estiverem registrados.

Uma nova execução deve reconhecer o que já está conforme, evitando:

- duplicar novamente sem necessidade;
- criar novas bibliotecas redundantes;
- aninhar wrappers repetidos;
- renomear continuamente os mesmos elementos;
- recompor imagens já consolidadas sem benefício.

## 26. Entrega

Apresentar um resumo objetivo com:

- quantidade de peças processadas;
- localização dos templates;
- principais mudanças estruturais;
- normalização de fontes, entrelinhas, tracking e medidas em px, com exceções e limitações;
- listas e relações de ícone + texto organizadas;
- imagens recortadas ou consolidadas;
- biblioteca de assets organizada, complementada, desativada pelo usuário ou pendente, com página e localização;
- índice auxiliar dos templates e sua localização, incluindo evidências e campos não testados;
- máscaras substituídas e inventário de cada máscara restante com justificativa;
- camadas removidas com segurança;
- conferência de integridade dos textos após separações;
- cobertura das comparações com o estado anterior e com a referência aprovada, identificando as versões;
- testes de substituição realizados;
- limitações e pendências.

Distinguir claramente:

- concluído;
- parcialmente concluído;
- não executado;
- bloqueado.

Não apresentar estimativas como medições.

Não afirmar que todo texto é editável quando parte dele estiver incorporada em imagens.

O resultado final deve ser fiel como peça gráfica e compreensível como sistema de template.
