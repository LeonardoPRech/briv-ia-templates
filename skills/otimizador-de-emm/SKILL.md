---
name: otimizador-de-emm
description: "Use para otimizar e-mails ou EMM do Briv.IA no Figma por reconstrução semântica em cópia: seções simples em auto-layout real, textos Fill/Hug, pixels inteiros, banners limpos e header/footer compartilhados. Preserve a composição, teste crescimento e compare com os originais."
---

# Otimizador de EMM

## Solução adotada

Reconstruir o e-mail em um novo frame ao lado do original, de dentro para fora, com uma hierarquia pequena e dirigida pelo conteúdo. Usar o original como referência visual e de conteúdo. O objetivo é um template limpo, escalável e fácil de interpretar e replicar por uma IA.

Esta é a solução para e-mails importados, estruturas manuais e conversões inadequadas. Não ativar auto-layout no frame externo para depois compensar as posições herdadas. Não conservar uma estrutura inadequada só para manter seus IDs.

Trabalhar somente nas peças indicadas. “E-mail” e “EMM” ajudam a localizar a página, sem ampliar o escopo. Se o pedido for somente análise, não editar. Usar a integração Figma e suas instruções operacionais. Na primeira reconstrução, preservar originais e versões anteriores e criar as novas cópias ao lado. Em uma continuação, identificar a versão reconstruída e corrigir essa cópia; não proliferar versões sem necessidade. Uma instrução explícita para criar nova versão prevalece.

## 1. Registrar e compreender

Antes de criar:
- Inspecionar a renderização de cada original e registrar ID, nome, largura, altura, conteúdo, estilos, imagens, composição, ordem e visibilidade.
- Separar conteúdo visível de sobras importadas, textos ocultos e auxiliares. Não transportar conteúdo encoberto como se fosse uma mensagem nova.
- Identificar header, banner, introdução, benefícios, listas, cards, unidades, agendamento, condições e footer.
- Medir paddings, gaps, alinhamentos e faixas que atravessam toda a largura.
- Se houver referência exemplar, ler sua estrutura e seus exemplos; adotar as relações de layout sem copiar identidade visual, largura ou conteúdo de outro cliente.

## 2. Definir a largura do cliente

Verificar os e-mails do próprio cliente e identificar o padrão predominante. 600 px é comum, mas não é obrigatório. Registrar a evidência, usar uma largura única no conjunto autorizado e adequar as peças fora desse padrão. Redimensionar seus conteúdos proporcionalmente e revisar cada seção; não esticar a peça inteira indiscriminadamente.

A largura do template é controlada. A altura total é Hug e responde ao conteúdo. Pequenas mudanças de altura e de quebra natural podem ser necessárias para obter uma estrutura limpa; preservar a composição e registrar essas diferenças. Não prometer igualdade pixel a pixel sem evidência.

## 3. Montar a estrutura simples

Usar um frame raiz vertical com largura padrão, altura Hug e gap zero:

- Header: componente compartilhado, opcional.
- Banner: seção em fluxo contendo a arte principal.
- Corpo: seção vertical com subseções semânticas.
- Extra: somente quando existir conteúdo próprio, como condições ou chamada adicional.
- Footer: instância do componente compartilhado do cliente.

Não criar seções vazias apenas para preencher esse esquema. Condições podem ficar junto da oferta correspondente. O corpo pode conter Introdução, Vacinas por idade, Unidades e Agendamento, por exemplo.

Todo container que organiza conteúdo deve usar auto-layout real. Usar um único grupo quando os elementos compartilham padding, gap e alinhamento. Criar outro somente para uma relação semântica ou de layout concreta. Evitar wrappers por linha, colunas vazias, espaçadores e alturas fixas que apenas reproduzem coordenadas antigas.

## 4. Construir o corpo de dentro para fora

1. Carregar todas as fontes usadas.
2. Criar textos, itens de lista, ícones e unidades gráficas.
3. Criar linhas, cards e subseções com padding e gap explícitos.
4. Montar as seções intermediárias.
5. Montar o Corpo e a raiz por último.
6. Após anexar os nós, configurar explicitamente os modos de largura e altura e verificar o estado efetivamente salvo.

Regras:
- Textos: largura Fill, altura Hug, redimensionamento vertical por conteúdo.
- Seções e colunas de conteúdo: largura Fill ou largura controlada; altura Hug.
- Raiz e Corpo: fluxo vertical, altura Hug.
- Ícones e imagens com proporção rígida: dimensões fixas, participando do fluxo.
- Cards, botões e caixas: frame nativo com preenchimento, borda, raio e padding; texto dentro do frame. Substituir retângulo solto com texto por cima.
- Faixa de cor que ocupa a largura inteira: preenchimento nativo da própria seção.
- Corte diagonal: vetor lateral em uma linha de auto-layout; o conteúdo controla a altura. Usar Fill na altura do adorno quando adequado.
- Sobreposição intencional: gap negativo entre unidades em fluxo, com ordem de desenho e limites conferidos.

No Corpo, Header, Extra e Footer, exigir zero camadas em “Ignorar layout automático”. Não aceitar coordenadas absolutas, deslocamentos ou wrappers compensatórios como substitutos do fluxo.

Ao trocar o sentido de um auto-layout, redefinir os modos de largura e altura: a troca de eixos pode conservar uma altura fixa indesejada. Ao clonar ou reparentear textos, conferir novamente Fill/Hug; não presumir que o modo anterior foi preservado.

## 5. Textos e listas

Preservar conteúdo, ordem, pontuação, família, peso, cor e destaques. Separar parágrafos e itens por significado. Remover apenas quebras de linha que serviam como posicionamento visual, permitindo a quebra natural; preservar quebras semânticas em endereços, grupos e chamadas quando necessárias. Conferir o texto após dividir ou unir trechos.

Cada item de lista deve ser uma linha horizontal própria:
- marcador ou ícone alinhado à primeira linha;
- texto Fill/Hug;
- gap e padding inteiros.

Não usar uma coluna fixa de marcadores ao lado de um único bloco de texto com vários itens. O crescimento de um item deve deslocar o próximo. Em duas colunas, cada coluna deve ter altura Hug e o container acompanhar a maior delas.

Conferir especialmente textos brancos ou claros: seu fundo colorido deve ser reconstruído junto, para não sumirem no branco. Não rasterizar conteúdo do corpo.

## 6. Pixels inteiros

No corpo, usar posições, larguras, paddings e gaps inteiros. Normalizar as pequenas escalas e inclinações acidentais da importação que produzam medidas fracionárias, preservando a aparência. Carregar fontes antes de alterar textos.

Preservar a matriz completa de transformação quando ela representar um recorte, flip ou composição intencional. Não substituir transformações gráficas por x/y sem análise.

Normalizar tamanhos e entrelinhas do corpo ao pixel inteiro quando necessário para obter o layout solicitado; preservar as famílias e pesos e revisar as quebras. As regras tipográficas específicas da skill geral pertencem somente ao banner. Conferir os alinhamentos centrais: larguras ou alturas de paridades diferentes podem gerar meio pixel.

Não arredondar cegamente curvas e recortes de imagens. Pixels inteiros de layout não autorizam deformar marcas, pessoas ou fotografias.

## 7. Otimizar somente a arte do banner com a skill geral

Aplicar [Otimizar templates Briv.IA](../otimizar-templates-briv-ia/SKILL.md) somente à arte do Banner. O restante segue este fluxo de e-mail.

A seção Banner participa normalmente do auto-layout do e-mail. Dentro dela, a arte é uma composição gráfica de tamanho controlado:
- fundo/fotografia;
- filtro ou degradê nativo;
- pessoa recortada com transparência real;
- grafismos e marcas;
- blocos de texto agrupados por relação.

A composição manual dentro da arte é legítima; não precisa ser simulada com dezenas de camadas ignorando um auto-layout. Organizar chamadas relacionadas em blocos de auto-layout e manter as unidades gráficas fáceis de substituir.

Remover máscaras herdadas:
- aplicar fotografia como preenchimento com crop em vetor nativo, quando fiel;
- consolidar fragmentos de uma mesma pessoa em um único PNG transparente, com área útil e resolução adequada;
- manter fotografia, filtro e pessoa separados;
- conservar formas e degradês nativos quando possível.

Não rasterizar o banner inteiro nem o e-mail inteiro. Exportar somente unidades indivisíveis, como pessoa, montagem de produto, marca ou ícone. Uma montagem de produto deve virar um asset independente, sem incluir texto do corpo. Não confundir o acervo com uma peça final.

Se o banner de origem for uma imagem única, reconstruir texto editável e grafismos nativos e aproveitar somente a região fotográfica sem texto. Registrar a origem raster e qualquer diferença residual de fidelidade. Não inventar uma fonte ou declarar uma marca vetorial se ela continua raster.

Organizar os assets reutilizáveis na página existente de imagens, preservando o conteúdo anterior, conforme a skill geral. Testar em uma cópia a substituição independente de pelo menos uma unidade representativa e remover o ensaio.

## 8. Header e footer compartilhados

Inspecionar a página de Componentes antes de criar:
- localizar o componente correto e verificar a marca do cliente;
- reutilizar o componente compatível;
- se não existir, reconstruir o conteúdo correto com auto-layout, criar o componente nessa página e aplicar instâncias em todos os e-mails do conjunto;
- preservar componentes de outras marcas; não os reaproveitar silenciosamente como se fossem do cliente.

O header é recomendado, mas opcional. Se a marca já estiver integrada ao banner, pode haver uma instância compartilhada oculta para evitar assinatura duplicada e preservar o visual. Registrar essa decisão. Não adicionar um cabeçalho visível redundante.

Footer deve ter textos legais editáveis, informações do cliente e unidades de marca/ícones separadas. Usar auto-layout também dentro dos containers, com altura Hug. Conferir expansão de textos em uma instância temporária e confirmar a conexão de todas as instâncias ao mesmo componente principal.

## 9. Organizar e nomear

Aplicar [Organizador de assets Briv.IA](../organizador-de-assets-briv-ia/SKILL.md) na organização externa autorizada, depois de validar o interior.

Para e-mails, usar o modelo seguido do tipo:
- Section: `Modelo 5 - Vacinas`.
- Frame: `E-mail / Modelo 5 - Vacinas / 600x1800`.

O campo central reproduz exatamente a section de modelo. Manter as categorias existentes, usar sections nativas e os estilos, paddings e gaps do organizador. Não colocar campanha ou título de conteúdo no nome final. A numeração precisa de evidência ou autorização; não atribuir modelos por mera ordem de camadas.

## 10. Verificação final independente

Fazer a segunda etapa de qualidade depois da reconstrução. Conferir todos os e-mails, não apenas o piloto:

**Estrutura**
- largura padrão, raiz e corpo Hug;
- todos os containers do corpo em auto-layout;
- textos Fill/Hug e sem cortes;
- zero “Ignorar layout automático” fora da composição gráfica;
- zero máscaras em todos os templates;
- padding e gaps inteiros, sem escalas acidentais;
- ausência de caixas vazias, duplicatas, sobras e colisões;
- componentes corretos e compartilhados;
- conteúdo e destaques preservados;
- originais e versões de referência intactos.

**Comportamento**
- ampliar texto representativo em uma cópia de cada modelo e verificar que as próximas seções e o footer se deslocam;
- testar item de lista com várias linhas e confirmar deslocamento dos próximos itens e alinhamento do marcador;
- testar header opcional e expansão de informação do footer;
- confirmar que nenhuma altura fixa de container provoca corte ou sobreposição;
- remover todos os ensaios e ler novamente os templates finais.

**Visual**
- renderizar o resultado de cada modelo e comparar com o respectivo original;
- revisar composição, recortes, posição das pessoas, legibilidade, fundos coloridos, ordem, margens, quebras, botões, endereços, marcas e footer;
- verificar todos os ajustes feitos durante a revisão, sem considerar uma auditoria anterior suficiente;
- aceitar apenas pequenas diferenças necessárias para o fluxo; registrar diferenças materiais e corrigir o que for viável.

Se restar qualquer pendência, criar uma caixa de aviso visível no Figma, fora da arte, com o modelo, problema, impacto e ação necessária. Não esconder a pendência em camadas nem declarar entrega integral se ela não foi resolvida.

## 11. Índice e entrega

Manter um índice fora das artes com modelos, finalidade, formato real, campos editáveis, assets/componentes, capacidade observada, testes e limites. Distinguir teste estrutural de aprovação visual de uma nova campanha.

Entregar links para os modelos e os componentes, quantidade concluída, largura, resultado da auditoria, diferenças relevantes e pendências. Relatar que os corpos são escaláveis; a arte de tamanho controlado ainda exige revisão quando a chamada ou a fotografia mudarem. Não apresentar ativação de auto-layout, contagens de camadas ou uma renderização isolada como prova suficiente de qualidade.
