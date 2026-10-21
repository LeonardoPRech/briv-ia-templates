# Aprendizados gerais para otimizar templates

Princípios aplicáveis a qualquer cliente, formato ou canal. O objetivo é preservar a composição e transformar a estrutura importada em unidades simples de substituir, posicionar e adaptar por pessoas e por IA.

## 1. Representar unidades de edição

Cada frame ou grupo deve corresponder a uma unidade que será movimentada, alinhada, substituída ou dimensionada em conjunto. Usar o menor número de containers que preserve essas relações. Uma contagem alta de auto-layouts não comprova flexibilidade; uma contagem baixa de camadas também não comprova qualidade.

Em continuações, melhorar as cópias existentes e aproveitar o que já está correto. Preservar originais, referências e o acervo anterior.

## 2. Separar posição de composição de padding

Posicionar uma coluna de conteúdo na região correta da arte e expressar as relações entre os campos em coordenadas locais simples. Não transformar o x/y de cada texto em padding de um wrapper próprio.

Um espaço interno grande pode ser necessário pela geometria de uma faixa. Nesse caso, aplicá-lo uma única vez à unidade adequada. Distinguir margem funcional, alinhamento e deslocamento no canvas. Usar um wrapper por texto somente quando ele tiver uma função própria que o container existente não consiga representar.

## 3. Vincular texto e suporte

Texto, faixa, etiqueta ou painel formam uma unidade semântica comum. Preferir preenchimento nativo quando a forma for simples. Para uma forma irregular, manter o vetor como fundo absoluto do mesmo frame de auto-layout, com o texto em fluxo e ancoragens coerentes.

Vincular a unidade ao fluxo superior quando corpo, chamada ou marca precisarem acompanhar o crescimento. Definir se o suporte cresce, mantém tamanho fixo ou impõe um limite de conteúdo. Não confundir um fundo de canvas com a faixa de um texto apenas porque ele está atrás da caixa.

## 4. Conter a geometria real

O clipping do frame principal não substitui a correção de camadas excessivamente grandes. Fundos devem acompanhar a arte; marcas devem ocupar a região da assinatura; formas decorativas devem terminar nos limites adequados; fotografias devem usar uma região de aplicação coerente.

Priorizar preenchimentos nativos para fundos e fotografias em formas. Preservar vetores simples e aparar sua geometria quando atravessarem o formato. Uma pequena extrapolação intencional de imagem pode ser aceitável; caixas com várias vezes o tamanho útil não são uma solução de template.

Definir constraints pela função e pelo limite real do elemento. Preservar frações necessárias a curvas, proporções e recortes exatos, sem forçar arredondamentos que deformem a aparência.

## 5. Consolidar fragmentos de uma mesma imagem

Uma pessoa recortada deve ser uma única imagem raster com transparência real. Cabelo, corpo, mãos, bordas e remendos complementares não devem permanecer em várias imagens que só funcionam juntas, mesmo que nenhum nó esteja marcado como máscara.

Reconhecer a técnica herdada de editores de imagem: fotografia de fundo, elementos gráficos intermediários e uma cópia recortada da pessoa em primeiro plano, às vezes acompanhada de patches ou camadas em Multiply. Preservar essa ordem visual e manter fundo e pessoa substituíveis separadamente. Consolidar apenas os fragmentos do mesmo recorte.

Procedimento:

1. Identificar a unidade visual e suas dependências, inclusive alfa, opacidade, filtros, sombras e mesclagem.
2. Isolar somente os fragmentos que formam a pessoa, produto, ícone ou montagem indivisível.
3. Gerar uma única imagem transparente em resolução adequada à escala de uso.
4. Recortar o excedente de alfa no próprio raster, incluindo margem suficiente para bordas suaves.
5. Substituir o conjunto por um único nó de imagem, preservando escala, posição, sobreposição e ancoragens.
6. Conferir o asset isolado e sua aplicação antes de remover as camadas redundantes da cópia.

Não basta renomear o grupo, desativar isMask ou transformar os fragmentos em filhos de outro frame. A fonte raster final precisa ser consolidada de fato.

Modos de mesclagem dependentes do fundo exigem atenção: exportar sobre transparência não garante equivalência. Conferir cabelo, contornos e regiões semitransparentes sobre fundos claros e escuros e na composição real. Evitar halos, vazios, duplicação de opacidade ou incorporação acidental do fundo. Se a fonte não permitir independência fiel, registrar a limitação e buscar a fonte apropriada, sem inventar partes ausentes.

Não fundir pessoas distintas, fundo, filtros, textos ou decorações que precisem ser trocados independentemente. Uma borboleta ou outro elemento gráfico sobreposto à pessoa pode continuar separado. Uma montagem de pessoas que se substitui como uma única fotografia pode constituir um único asset.

## 6. Usar máscaras com parcimônia

Substituir máscaras herdadas quando houver alternativa nativa ou raster fiel e reutilizável. Avaliar também composições que simulam máscaras por fragmentos, frames com clipping ou imagens sobrepostas.

Uma máscara intencional deve ter função clara, limites próximos da região útil e, preferencialmente, ficar dentro da arte. Não usar uma máscara enorme para uma marca pequena. Respeitar uma proibição explícita de máscaras no conjunto solicitado.

Uma assinatura consolidada pode ser substituída como unidade, mas suas partes internas deixam de ser editáveis. Não usar a consolidação como justificativa para rasterizar a arte inteira, textos editáveis ou formas simples.

## 7. Identificar a fonte pelo contexto

Nomes importados não identificam conteúdo de forma confiável. Relacionar origem e destino por ID estável, modelo, função, visibilidade, geometria, transformação, ordem e hash da imagem. Resolver nomes repetidos antes de escolher a fonte; não usar a primeira ocorrência encontrada.

Deduplicar somente assets realmente equivalentes. A mesma pessoa com outro enquadramento, tratamento ou recorte pode exigir uma variante.

## 8. Preservar o enquadramento

Reutilizar o hash da fotografia não preserva automaticamente seu crop. Considerar a proporção da imagem, FIT/FILL, área desenhada, transformações anteriores, opacidade, filtros e mesclagem.

Ao converter uma fotografia para preenchimento de uma forma, mapear as coordenadas locais da forma às coordenadas normalizadas da imagem e compor as transformações existentes. Validar especialmente rostos e regiões sobrepostas. Não aplicar uma fórmula restrita a retângulos sem rotação a imagens rotacionadas ou já transformadas.

## 9. Aparar vetores sem criar bordas

Uma forma preenchida e um contorno aberto exigem tratamentos diferentes. Fechar um caminho após uma interseção pode criar uma borda que não existia. Aparar segmentos ou curvas preservando a função original do traçado.

Uma falha da operação geométrica ou da API não prova que o elemento não contribui visualmente. Inspecionar o caminho e a aparência antes de remover.

## 10. Reparentear sem alterar o layout

Preservar transformação, dimensões, sobreposição, visibilidade, opacidade, clipping e regras de dimensionamento ao mover elementos. Constraints de esticamento e auto-layout podem redimensionar ou reposicionar filhos durante a operação.

Quando necessário, neutralizar temporariamente o fluxo e as ancoragens, realizar a mudança e restaurar a intenção. Um fundo produzido por uma operação booleana deve continuar absoluto; ele não pode entrar no fluxo e empurrar o texto.

Configurar eixos, padding, gaps e filhos; aplicar as dimensões fixas; depois ativar Hug/Fill somente nos eixos e contextos apropriados. Usar alinhamento do container e regras atuais da ferramenta. Não recorrer a propriedades antigas que alterem o alinhamento do conjunto sem intenção.

## 11. Validar aparência e comportamento

Conferir estrutura, geometria e aparência. Nenhuma dessas dimensões substitui as outras. A ausência de erros da API ou de nós isMask não comprova que a peça está pronta.

Comparar com o estado anterior e com a referência aprovada. Conferir conteúdo e estilos por trecho, limites reais, recortes, rostos, bordas, quebras de texto e ordem visual. Inspecionar transparência real e a quantidade de imagens por unidade de substituição.

Testar alterações reversíveis de conteúdo em exemplos representativos. Observar se suporte e vizinhos acompanham o crescimento, além da caixa de texto. Testar a substituição da pessoa e do fundo de forma independente quando isso fizer parte do modelo.

Não reduzir texto, trocar fonte ou prometer adaptação ilimitada para fazer o teste passar. Registrar limites observados nos relatórios de execução e remover temporários ao concluir.

## 12. Manter biblioteca e índice coerentes

Reutilizar a biblioteca existente, preservar fontes completas e acrescentar apenas assets necessários. Distinguir fonte reutilizável completa do recorte aplicado a um formato; não amputar uma fonte útil por causa dos limites de uma aplicação.

Atualizar o índice existente para apontar ao asset final consolidado e ao comportamento atual. Remover referências obsoletas dos registros de seleção sem apagar o acervo histórico por conveniência. Reexecuções não devem duplicar cópias, bibliotecas ou wrappers.

## Critérios de aceitação

- Cada container representa uma unidade útil.
- Nenhum padding apenas repete a posição de canvas de uma caixa.
- Texto e suporte permanecem vinculados durante a edição.
- Fotografias, marcas e decorações possuem limites coerentes.
- Cada pessoa ou imagem indivisível usa um único raster transparente quando a consolidação for necessária.
- Fragmentos complementares não permanecem como reconstrução artificial de máscara.
- Fundo, filtros e elementos independentes continuam substituíveis separadamente.
- Máscaras restantes são intencionais, locais e justificadas.
- Escala, enquadramento, bordas, transparência e sobreposição são preservados.
- Conteúdo, fontes e estilos permanecem íntegros.
- Testes de crescimento verificam também o suporte e os elementos vizinhos.
- Originais, fontes completas e acervo anterior permanecem preservados.
- Índice e biblioteca correspondem ao estado final.
