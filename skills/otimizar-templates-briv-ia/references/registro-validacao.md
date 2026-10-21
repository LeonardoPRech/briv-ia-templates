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

Conferir todas as caixas editáveis, incluindo trechos mistos: fontes em inteiros, entrelinhas explícitas em múltiplos de 10% e tracking com até uma casa decimal na unidade original. Registrar a fonte original usada na conversão de px para percentual e como AUTO foi resolvido. Não apresentar AUTO não resolvido como normalizado. Conferir x/y, dimensões, gaps, paddings e outras medidas em px; registrar frações mantidas por proporção, fluxo calculado, rotação ou fidelidade. Preservar estilos e variáveis globais. Distinguir ajustes intencionais de regressões.

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
