# Etapas do TCC

Última atualização: 06/10/2026.

## Regra de acompanhamento

Atualizar este arquivo junto de cada nova alteração do trabalho, conforme solicitado pelo autor. Registrar o que mudou, o que permanece em andamento, o próximo passo e a verificação realizada. Não marcar uma etapa como concluída apenas porque existe texto inicial ou porque o PDF compilou.

Manter a introdução curta, com conectivos naturais e sem repetir informações. Reservar os fundamentos para a fundamentação teórica, os procedimentos para a metodologia e as evidências obtidas para os resultados.

## Situação atual

- Etapa em andamento: revisão e consolidação da introdução.
- Branch atual: `introducao`.
- Repositório: https://github.com/aliranTi/TCC.
- Último commit enviado: `142020b` — estrutura do TCC e etapa de introdução.
- As revisões posteriores da introdução, fundamentação, metodologia e referências estão locais, ainda sem commit ou envio. Este registro também ainda não foi enviado.
- A introdução ocupa duas páginas no PDF, incluindo problema de pesquisa e objetivos.
- Fundamentação e metodologia contêm textos iniciais realocados da introdução; ainda precisam ser desenvolvidas.
- Trabalhos relacionados e resultados contêm apenas os títulos. A conclusão ainda contém orientação do template.

## O que foi feito

### Versionamento

- Inicializado o Git local e conectado ao repositório informado pelo autor.
- Criada e publicada a branch `introducao`, preservando o commit inicial de `master`.
- Configurado o `.gitignore` para excluir temporários do LaTeX, `documento.pdf`, configurações locais e contexto dos agentes.
- Mantidos no versionamento os fontes, a bibliografia, os arquivos de estilo e os recursos necessários ao documento.

### Texto e comentários do PDF

- Revisadas pontuação, concordância, transições e repetições na introdução.
- Lidos 14 comentários e identificadas 18 marcações no PDF recebido em `C:/Users/TI/Downloads/documento.pdf`.
- Reduzida a abertura da introdução de 11 para 4 parágrafos.
- Consolidado o problema de pesquisa e reduzidos os objetivos específicos de 9 para 5.
- Identificada a CP3 como vinculada à UFERSA, campus Pau dos Ferros, com referência institucional.
- Reunida a apresentação da proposta no último parágrafo da abertura.
- Transferidos os fundamentos de pré-dimensionamento para `2-textuais/2-fundamentacao-teorica.tex` e os detalhes computacionais para `2-textuais/4-metodologia.tex`.
- Substituídos os exemplos do template da fundamentação pelo conteúdo inicial realocado.
- Mantida a verificação computacional como objetivo verificável; retirada a promessa de comparação experimental futura dos objetivos.
- Interpretado o comentário “estruturas treinadas” como “estruturas treliçadas”, em coerência com o tema. Essa interpretação deve ser confirmada na revisão do autor/orientador.
- Mantida a descrição do FTOOL como ferramenta de análise de estruturas planas, conforme a documentação oficial, sem restringi-lo às estruturas isostáticas.

### Bibliografia e compilação

- Substituídos acentos nos nomes dos autores por comandos LaTeX compatíveis com o BibTeX, corrigindo a geração de iniciais com bytes UTF-8 inválidos.
- Removidos delimitadores Markdown que estavam dentro do arquivo `.bib`.
- Protegido o sobrenome composto “Timoteo Júnior” e ajustada a ordem das citações agrupadas na abertura.
- Acrescentadas as referências institucionais da CP3 e do FTOOL; a página do FTOOL foi registrada sem data de publicação (`s.d.`).
- Regenerados a bibliografia e o PDF. Última compilação concluída sem erros; o PDF completo possui 24 páginas. Isso não significa que todos os capítulos estejam concluídos.
- Executado `git diff --check`, sem erros de espaços em branco. Avisos de conversão LF/CRLF não impediram a verificação.

## O que fazer e como fazer

| Etapa | Estado | Próxima ação e procedimento |
| --- | --- | --- |
| Introdução | Em andamento | Revisar a versão resumida com o autor/orientador. Conferir contexto, problema, objetivo geral e cinco objetivos específicos. Manter o tamanho atual como referência, sem acrescentar detalhes de implementação. |
| Referências | Em andamento | Conferir os metadados nas publicações originais, os nomes compostos e a correspondência entre afirmações e fontes. Acrescentar fontes ao desenvolver os capítulos e regenerar o BibTeX. |
| Fundamentação teórica | Iniciada | Desenvolver treliças, análise estrutural, propriedades da madeira, tração, compressão, flambagem, representação computacional e execução no navegador. Definir símbolos, unidades e hipóteses; fundamentar as equações em fontes técnicas. O texto atual é apenas o início desse capítulo. |
| Trabalhos relacionados | Pendente | Ler os trabalhos selecionados e comparar objetivo, método, ferramenta, validação e limitações. Explicar a relação de cada trabalho com a proposta, sem atribuir resultados que não foram verificados na fonte. |
| Metodologia | Iniciada | Conferir o código atual do sistema antes de descrever a implementação. Detalhar leitura do `.ftl`, reconstrução do modelo, integração com anaStruct, pré-dimensionamento, execução com Pyodide e interface Web. Informar parâmetros, hipóteses e procedimentos de verificação. |
| Resultados | Pendente | Executar casos de referência e registrar entradas, configurações e saídas. Comparar geometria, esforços e reações com referências; conferir o pré-dimensionamento por cálculo independente. Apresentar diferenças, limitações, tabelas e figuras. |
| Conclusão | Pendente | Redigir após os resultados, respondendo à questão de pesquisa e relacionando evidências aos objetivos. Separar contribuições, limitações e trabalhos futuros. |
| Elementos pré-textuais | Pendente | Definir título e revisar capa, folha de aprovação e demais campos do template. Escrever resumo e abstract após consolidar método e resultados. Atualizar listas conforme o conteúdo final. |
| Revisão final | Pendente | Conferir citações, unidades, legendas, referências cruzadas e formatação. Compilar o documento completo e revisar o PDF visualmente. |
| Publicação das revisões | Pendente | Revisar o diff, registrar as alterações da etapa em commit e enviar a branch quando solicitado. Atualizar neste arquivo o estado do envio. |

## Critérios para continuar

- Não confundir camadas na seção transversal com quantidade física de palitos.
- Não apresentar parâmetros padrão do software como resultados de ensaios.
- Distinguir verificação do programa de validação física da ponte.
- Não declarar otimização estrutural ou validação experimental sem implementação e evidências correspondentes.
- Não ampliar o escopo nem prometer experimentos apenas para preencher objetivos.
- Conferir comentários técnicos do orientador com as fontes antes de transformar sugestões em afirmações no texto.

## Fluxo das próximas alterações

1. Consultar este registro e conferir a branch e as alterações locais.
2. Editar os arquivos da etapa, preservando alterações feitas pelo autor.
3. Atualizar as referências quando houver novas afirmações fundamentadas.
4. Compilar quando houver alterações em LaTeX ou na bibliografia e verificar o trecho afetado no PDF.
5. Atualizar o estado das etapas e acrescentar uma entrada curta no histórico abaixo.
6. Ao mudar de etapa, usar uma branch com nome correspondente, como `fundamentacao-teorica`, `trabalhos-relacionados`, `metodologia`, `resultados` ou `conclusao`. Preservar os commits anteriores; não considerar uma nova branch como encerramento automático da etapa anterior.

Compilação local: executar `pdflatex documento.tex`, `bibtex documento` e `pdflatex documento.tex` duas vezes. Nesta máquina, os executáveis estão em `J:/MiKTeX/miktex/bin/x64/`. Se houver um `.bbl` inválido já gerado e um `.aux` utilizável, regenerar primeiro a bibliografia com `bibtex documento`. Corrigir a origem em `referencias.bib`, pois alterações manuais no `.bbl` são sobrescritas.

## Histórico

### 06/10/2026

- Publicada a estrutura inicial na branch `introducao` (`142020b`).
- Corrigidos problemas de acentuação na bibliografia e revisada a redação da introdução.
- Aplicadas as observações do PDF com redução da introdução e redistribuição de conteúdo.
- Conferida a compilação do PDF revisado: 24 páginas no total; introdução nas páginas numeradas 14 e 15.
- Criado este acompanhamento. Próximo passo: revisar a introdução resumida com o autor/orientador antes de consolidar a etapa.
