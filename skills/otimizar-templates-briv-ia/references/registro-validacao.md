# Registro de execução e validação

Preencher somente com operações, medições e comparações realizadas. Usar em cada lote e retomar pelo estado real dos arquivos. Manter os registros fora das artes.

## Escopo

- Modo: completo, parcial, continuação ou somente análise.
- Arquivo/páginas, peças abrangidas e exclusões.
- Fontes pertinentes da base de conhecimento.
- Referência visual aprovada: identificação, origem e versão.
- Estado inicial e destino das cópias.
- Assets: etapa padrão ativa ou explicitamente desativada pelo usuário.

## Mapeamento

| Original ID/link | Cópia otimizada ID/link | Modelo/adaptação | Assets ID/link | Registro no índice | Estado e pendências |
| --- | --- | --- | --- | --- | --- |

## Comparações por etapa

| Peça e etapa | Estado anterior: versão/captura | Resultado atual: versão/captura | Comparação com anterior | Conferência com referência aprovada | Cobertura, diferenças e correção |
| --- | --- | --- | --- | --- | --- |

Comparar com tamanho, fundo e renderização equivalentes. Inspecionar regiões sensíveis e casos complexos em tamanho original. Se uma mudança corrigir a composição em direção à referência aprovada, explicar por que difere do estado anterior. Anotar a última etapa validada e não propagar regressões.

## Máscaras restantes — um registro por máscara

| ID/localização | Função e origem | Alternativas avaliadas | Justificativa técnica | Evidência visual | Impacto na substituição e pendência |
| --- | --- | --- | --- | --- | --- |

Registrar inclusive máscaras intencionais. Se nenhuma permanecer, afirmar isso somente após inspecionar o escopo completo. Conveniência não é justificativa para preservar máscara herdada com alternativa fiel e reutilizável.

## Textos separados

| Origem ID e conteúdo | Destinos em ordem | Conteúdo e pontuação | Destaques/estilos | Quebras intencionais | Divergências e correção |
| --- | --- | --- | --- | --- | --- |

Conferir a união ordenada dos trechos; não normalizar diferenças silenciosamente. Registrar marcadores, destaques e quebras relevantes. Nenhuma informação pode desaparecer, duplicar ou mudar de sentido.

## Normalização tipográfica e geométrica

| Peça/ID e trecho ou propriedade | Valor/unidade anterior | Valor/unidade final | Família/estilo preservados | Conferência visual e de quebras | Exceção ou pendência |
| --- | --- | --- | --- | --- | --- |

Conferir todas as caixas editáveis, incluindo trechos mistos: fontes inteiras, entrelinhas percentuais explícitas de 100%, 110%, 120%… e tracking com até uma casa decimal na unidade original. Registrar fonte original F0, fonte final inteira F1, altura efetiva original H0 e percentual final escolhido pela menor diferença em px, conforme a seção 13.1. Registrar como AUTO foi resolvido; AUTO não resolvido é pendência.

Conferir x/y, dimensões, gaps, paddings, raios, espessuras, espaçamentos de parágrafo e outras medidas de layout em px de todos os objetos após o fluxo final. Frações restantes e outras violações são pendências com ID, propriedade, valor e motivo; não declarar conformidade integral. Coeficientes de transformação e pontos de curvas não se confundem com medidas de layout. Preservar estilos e variáveis globais. Distinguir ajustes intencionais de regressões.

## Varredura de formatos nominais e microdesvios

| Frame ID/nome | Evidência do formato nominal | Largura/altura nominal | Largura/altura real antes | Diferença por eixo em px e % | Dentro da tolerância | Ação e dimensões finais | Conferência visual e pendência |
| --- | --- | --- | --- | --- | --- | --- | --- |

Inspecionar todos os frames principais. Usar a tolerância da seção 13.1: até 3 px e 0,5% em cada eixo, salvo limite explícito do usuário. Conferir o exemplo nominal 1080x1350 versus real 1081x1351, corrigido para 1080x1350 sem escalar toda a arte. Não tratar conversão de formato como microcorreção. Distinguir altura nominal fixa de altura Hug descritiva em e-mails. Repetir a varredura depois da normalização e da organização final.

## Listas, bullets e checkboxes

| Lista/ID | Referência aprovada | Estrutura final e wrappers removidos/justificados | Largura da linha, ícone, gap, padding e largura Fill do texto | Entrelinha por item e gap vertical | Testes curto/multilinha/crescimento e suporte/vizinhos | Limites, overflow e pendências |
| --- | --- | --- | --- | --- | --- | --- |

Conferir um auto-layout horizontal por item, ícone e texto diretos e pilha vertical. Confirmar Fill/Hug em todos os textos e contenção na largura útil, não apenas aparência na renderização atual. Registrar entrelinha compacta (normalmente 120% ou 130%) e espaço entre itens pelo gap; se a entrelinha original era um espaçador artificial, registrar a correção intencional em vez de preservar o valor inflado pela regra de aproximação. Registrar qualquer container adicional e sua função concreta. Testar crescimento intermediário, deslocamento dos próximos itens, manutenção do gap, suporte e chamada seguinte; remover o ensaio. Não afirmar teste executado sem evidência.

## Assets e testes de substituição

- Página existente, section, localização e vínculo com as peças; conteúdo anterior preservado.
- Asset completo versus recorte de aplicação; origem, transparência e resolução observadas.
- Peça/cópia temporária, alteração exata testada, resultado e evidência.
- Restauração de conteúdo e remoção dos temporários.
- Testes não realizados e seu motivo; não tratar uma amostra como garantia geral.

## Entrega

Informar quantidade real de peças, localização, mudanças estruturais, agrupamentos, textos conferidos, assets, máscaras substituídas e restantes, índice, comparações e testes. Distinguir concluído, parcial, não executado e bloqueado. Indicar o que foi desativado pelo usuário, o que falta verificar e a cobertura de cada comparação.

## Consolidação de recortes e geometria útil

Para cada unidade consolidada, registrar no relatório da execução: origem e destino estáveis; função da unidade; fragmentos incluídos; elementos independentes preservados; resolução; transparência real; recorte de alfa; posição, escala e sobreposição; constraints; comparação antes/depois e na composição; inspeção de cabelo e bordas sobre fundos claros e escuros; dependências de mesclagem e limitações.

Na revisão estrutural, verificar também unidades fragmentadas sem isMask, limites reais dos descendentes, padding que reproduz posição de canvas e vínculo entre texto e suporte. Testar o efeito do crescimento nos vizinhos. Uma contagem zero de máscaras não substitui essas verificações.

Atualizar o vínculo do índice para o asset consolidado final. Manter fontes completas e acervo anterior, distinguindo-os do recorte específico da aplicação.
