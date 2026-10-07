# Etapas do TCC

Última atualização: 07/10/2026.

Este arquivo serve como roteiro de execução do TCC. A ideia é consultar esta página antes de começar uma nova sessão de escrita para saber **o que fazer agora**, **o que ainda falta** e **quando uma etapa pode ser considerada concluída**.

---

## 1. Objetivo do trabalho

Desenvolver uma ferramenta web capaz de interpretar modelos do FTOOL e auxiliar na análise estrutural e no pré-dimensionamento de estruturas treliçadas de palitos destinadas à CP3.

### Questão de pesquisa

> Como integrar a interpretação de modelos do FTOOL à análise e ao pré-dimensionamento de pontes de palitos em uma ferramenta web acessível aos participantes da CP3?

### Regra principal de escrita

O TCC não deve ser apresentado apenas como documentação de software.

A narrativa do trabalho deve seguir esta sequência:

**problema de engenharia → fundamentos → solução computacional → método de verificação → resultados → limitações → conclusão**

O código é o meio utilizado para resolver o problema, não o objeto principal do texto.

---

## 2. Situação atual

- [x] Estrutura básica do TCC criada em LaTeX.
- [x] Introdução escrita e revisada.
- [x] Problema de pesquisa definido.
- [x] Objetivo geral definido.
- [x] Cinco objetivos específicos definidos.
- [x] Organização do trabalho adicionada à introdução.
- [x] Bibliografia inicial criada e revisada.
- [ ] Fundamentação teórica consolidada.
- [ ] Trabalhos relacionados escritos.
- [ ] Metodologia completa e alinhada ao código atual.
- [ ] Plano de validação executado.
- [ ] Resultados escritos.
- [ ] Conclusão escrita.
- [ ] Resumo e abstract finais.
- [ ] Revisão final de texto, referências e formatação.

### Prioridade atual

**Capítulo 2 — Fundamentação teórica.**

Depois dele, seguir para **Trabalhos Relacionados** e só então consolidar a **Metodologia**.

### Versionamento e acompanhamento

- Branch atual: `fundamentacao-teorica`.
- Referência anterior a esta atualização: `3eb34a8` — versão inicial da fundamentação teórica.
- As alterações de 07/10/2026 serão registradas no commit `docs: amplia fundamentacao teorica e atualiza roteiro do TCC`.
- O envio deste novo commit ao GitHub permanece pendente.
- Atualizar este roteiro junto de cada nova alteração, preservando a organização por capítulos e checklists. Marcar uma tarefa como concluída somente após a verificação correspondente.

---

# 3. Ordem recomendada de trabalho

Não escrever o TCC necessariamente na ordem em que ele aparece no PDF.

A sequência recomendada é:

1. consolidar a Introdução;
2. concluir a Fundamentação Teórica;
3. escrever os Trabalhos Relacionados;
4. documentar a Metodologia com base no código atual;
5. definir e executar os testes de validação;
6. escrever Resultados e Discussão;
7. revisar a Introdução à luz dos resultados;
8. escrever a Conclusão;
9. escrever Resumo e Abstract;
10. revisar o documento completo.

---

# 4. Capítulo 1 — Introdução

Arquivo:

`2-textuais/1-introducao.tex`

## Finalidade

Explicar:

- o contexto das competições de pontes de palitos;
- o papel da análise estrutural;
- a utilização do FTOOL;
- a necessidade de transformar os resultados estruturais em informações úteis ao pré-dimensionamento;
- o problema de pesquisa;
- os objetivos do trabalho;
- a organização do documento.

## Estado

**Praticamente concluído.**

Evitar acrescentar detalhes de implementação, equações, funcionamento do parser ou arquitetura do sistema neste capítulo.

## Antes de considerar concluído

- [x] Contexto apresentado.
- [x] CP3 apresentada.
- [x] FTOOL contextualizado.
- [x] Problema de pesquisa explícito.
- [x] Objetivo geral coerente com o problema.
- [x] Objetivos específicos verificáveis.
- [x] Limitação das estimativas mencionada.
- [x] Organização do trabalho apresentada.
- [ ] Fazer uma leitura final após concluir Resultados e Conclusão.

---

# 5. Capítulo 2 — Fundamentação teórica

Arquivo:

`2-textuais/2-fundamentacao-teorica.tex`

## Finalidade

Fornecer ao leitor os conceitos necessários para compreender o problema e a solução.

Este capítulo **não deve explicar como o código foi implementado**.

## Estrutura recomendada

### 2.1 Pontes treliçadas de palitos de picolé

Abordar:

- uso de competições de pontes no ensino;
- relação entre teoria, projeto, construção e ensaio;
- características das pontes de palitos;
- contexto da CP3 quando necessário.

Referências já disponíveis:

- `silva2024metodologia`
- `lamberti2025ponte`
- `rodriguessilva2022trelicadas`
- `mendes2018analise`

### 2.2 Análise estrutural de treliças

Explicar:

- nós e barras;
- condições de apoio;
- carregamentos;
- esforços internos;
- reações;
- deslocamentos;
- esforço axial;
- diferença entre tração e compressão.

Não aprofundar ainda o algoritmo do programa.

### 2.3 Ferramentas computacionais aplicadas à análise estrutural

Discutir o papel de programas e métodos computacionais na análise e no ensino.

Referências:

- `branchier2020softwares`
- `maciel2022ftool`
- `martha2022ftool`
- `passinho2025ftool`

#### 2.3.1 FTOOL

Apresentar:

- objetivo do programa;
- modelagem de estruturas planas;
- carregamentos e apoios;
- resultados fornecidos;
- uso educacional.

Não explicar ainda como o arquivo `.ftl` é interpretado pelo projeto.

#### 2.3.2 anaStruct

Apresentar:

- biblioteca Python de análise estrutural 2D;
- representação programática de estruturas;
- possibilidade de integração com aplicações computacionais.

Referências:

- `dumka2025anastruct`
- `vink2026anastruct`

### 2.4 Pré-dimensionamento de barras de palitos

Introduzir a ligação entre:

**esforço obtido → propriedades do material → geometria da seção → estimativa da composição da barra**

#### 2.4.1 Tração

Abordar conceitualmente:

- força axial de tração;
- tensão normal;
- área resistente;
- resistência do material.

#### 2.4.2 Compressão e flambagem

Abordar:

- esforço de compressão;
- estabilidade;
- esbeltez;
- flambagem;
- influência da geometria e do comprimento.

Referências importantes:

- `souza2015flambagem`
- `silva2026ruptura`
- `abnt2022nbr7190`

### 2.5 Limitações do modelo teórico

Explicar que:

- madeira possui variabilidade;
- colagem e montagem influenciam o protótipo;
- imperfeições geométricas não são totalmente representadas;
- consistência do cálculo não equivale a validação física da ponte;
- o resultado do sistema deve ser tratado como pré-dimensionamento.

## O que ainda falta no Capítulo 2

A versão atual já contém as seções de pontes treliçadas, análise estrutural, ferramentas computacionais (FTOOL e anaStruct), pré-dimensionamento, tração, compressão e considerações sobre o modelo. As equações de tensão normal e de área da seção composta também foram incluídas. A existência dessas seções não encerra sua revisão.

- [ ] Adicionar uma referência clássica de Análise Estrutural ou Resistência dos Materiais.
- [ ] Corrigir ocorrências como “interpretaçãodos” e “aferramenta” e revisar a expressão “nós biarticulados”.
- [ ] Distinguir as limitações da análise plana das verificações de estabilidade das barras nos dois eixos realizadas no pré-dimensionamento.
- [ ] Consolidar a seção de treliças.
- [ ] Consolidar análise estrutural.
- [ ] Consolidar FTOOL.
- [ ] Consolidar anaStruct.
- [ ] Consolidar tração.
- [ ] Consolidar compressão/flambagem.
- [ ] Revisar as afirmações normativas com a NBR 7190-1.
- [ ] Conferir se toda afirmação técnica importante possui fonte adequada.

## Critério de conclusão

O capítulo está pronto quando um leitor consegue entender **todos os conceitos usados no restante do TCC sem precisar conhecer o código**.

---

# 6. Capítulo 3 — Trabalhos relacionados

Arquivo:

`2-textuais/3-trabalhos-relacionados.tex`

## Finalidade

Mostrar o que outros trabalhos já fizeram e deixar clara a contribuição desta proposta.

Não transformar esta seção em uma segunda fundamentação teórica.

## Trabalhos candidatos

Avaliar principalmente:

- `silva2024metodologia`
- `lamberti2025ponte`
- `silva2026ruptura`
- `dumka2025anastruct`
- `fairclough2021layopt`
- trabalhos sobre FTOOL e análise computacional que tenham relação direta com a proposta.

## Para cada trabalho, responder

1. Qual era o objetivo?
2. Qual problema foi tratado?
3. Qual método ou ferramenta foi utilizado?
4. Houve implementação computacional?
5. Houve validação?
6. Quais resultados foram apresentados?
7. Qual a diferença em relação a este TCC?

## Tabela comparativa sugerida

| Trabalho | FTOOL | Análise estrutural | Pré-dimensionamento | Aplicação web | Validação |
| --- | --- | --- | --- | --- | --- |

A tabela deve ser acompanhada de análise textual. Não deixar a comparação apenas na tabela.

## Critério de conclusão

- [ ] Pelo menos 4 trabalhos realmente comparados.
- [ ] Diferenças entre eles e esta proposta explicitadas.
- [ ] Nenhum resultado atribuído a uma fonte sem confirmação.
- [ ] Contribuição do TCC compreensível ao final do capítulo.

---

# 7. Capítulo 4 — Metodologia

Arquivo:

`2-textuais/4-metodologia.tex`

## Estado

**Redação pendente.** O arquivo contém o título e um parágrafo provisório gerado por `\lipsum[2]`. Esse conteúdo não representa a metodologia do trabalho e deverá ser substituído após a consolidação dos capítulos anteriores.

## Regra principal

Antes de escrever cada subseção, conferir o estado atual do repositório:

`aliranTi/ftool-parser-python`

O texto deve descrever **o que realmente está implementado**, não uma arquitetura antiga ou planejada.

## Estrutura recomendada

### 4.1 Caracterização do trabalho

Explicar a natureza aplicada/computacional do trabalho e como a ferramenta será avaliada.

### 4.2 Visão geral da solução

Apresentar um diagrama com o fluxo:

`arquivo .ftl → parser → modelo estrutural → anaStruct → análise → pré-dimensionamento → resultados`

### 4.3 Interpretação dos arquivos FTL

Explicar:

- leitura do arquivo;
- versões suportadas;
- reconstrução da topologia;
- nós derivados dos endpoints;
- materiais;
- seções;
- apoios;
- cargas;
- normalização das unidades.

Não documentar cada função do código.

### 4.4 Conversão para o modelo de análise

Explicar como o modelo interpretado é convertido para o anaStruct:

- correspondência de nós e barras;
- propriedades;
- apoios;
- cargas;
- elementos de treliça/pórtico quando aplicável.

### 4.5 Análise estrutural

Descrever:

- resultados utilizados;
- reações;
- esforços axiais;
- deslocamentos;
- convenção de sinais;
- unidades.

### 4.6 Pré-dimensionamento

Explicar claramente:

- hipóteses;
- propriedades adotadas;
- tração;
- compressão;
- flambagem;
- critérios de aprovação;
- fatores utilizados.

### 4.7 Quantidade física de palitos

Distinguir:

- número de camadas da seção;
- palitos necessários ao longo da barra;
- comprimento comercial;
- emendas/sobreposição;
- quantidade física total.

**Nunca usar “camadas” e “palitos físicos” como sinônimos.**

### 4.8 Aplicação web

Apresentar:

- Next.js/React/TypeScript;
- execução do Python no navegador;
- Pyodide;
- Web Worker;
- seleção do arquivo;
- prévia;
- confirmação;
- cálculo;
- relatório.

### 4.9 Estratégia de verificação

Definir previamente como cada parte será testada.

## Critério de conclusão

O capítulo deve permitir que outra pessoa compreenda e reproduza **o método**, mesmo sem ler diretamente todo o código.

---

# 8. Plano de verificação e validação

Esta é uma das partes mais importantes do TCC.

Executar preferencialmente nesta ordem.

## 8.1 Parser e topologia

Objetivo:

Verificar se o sistema interpreta corretamente um modelo conhecido.

Comparar:

- número de nós;
- número de barras;
- coordenadas;
- conectividade;
- apoios;
- cargas;
- materiais;
- seções.

- [ ] Caso simples definido.
- [ ] Resultado esperado registrado.
- [ ] Resultado do parser registrado.
- [ ] Diferenças analisadas.

## 8.2 Análise estrutural

Comparar os resultados do sistema com o FTOOL.

Priorizar:

- reações de apoio;
- esforços axiais;
- eventualmente deslocamentos.

Tabela sugerida:

| Elemento | FTOOL | Ferramenta | Diferença absoluta | Diferença percentual |
| --- | ---: | ---: | ---: | ---: |

- [ ] Pelo menos um modelo simples.
- [ ] Pelo menos um modelo representativo da CP3.
- [ ] Convenção de sinais documentada.
- [ ] Unidades documentadas.
- [ ] Diferenças discutidas.

## 8.3 Pré-dimensionamento

Não usar apenas o resultado do próprio programa para verificar o programa.

Selecionar algumas barras e reproduzir o cálculo de forma independente.

Verificar:

- [ ] barra em tração;
- [ ] barra em compressão;
- [ ] área;
- [ ] tensão;
- [ ] esbeltez;
- [ ] flambagem;
- [ ] número de camadas;
- [ ] quantidade física de palitos.

## 8.4 Python versus navegador

Executar o mesmo caso:

- diretamente em Python;
- por Pyodide na aplicação web.

Comparar os resultados numéricos.

- [ ] Caso definido.
- [ ] Resultados equivalentes.
- [ ] Eventuais diferenças justificadas.

## 8.5 Relatório e interface

Conferir se os dados exibidos correspondem aos dados calculados.

- [ ] diagramas;
- [ ] tabela por membro;
- [ ] reações;
- [ ] quantidade total;
- [ ] unidades;
- [ ] nomes/IDs das barras.

## 8.6 Validação experimental

Somente incluir como resultado do TCC caso realmente seja executada.

Se não houver ensaio experimental, deixar claro que:

> a verificação computacional do software não constitui validação experimental da capacidade resistente do protótipo físico.

---

# 9. Capítulo 5 — Resultados e discussão

Arquivo:

`2-textuais/5-resultados.tex`

## Regra principal

Metodologia explica **como foi feito**.

Resultados mostram **o que aconteceu**.

Não misturar os dois.

## Estrutura sugerida

### 5.1 Verificação da interpretação dos arquivos FTL

Apresentar os casos e as comparações do parser.

### 5.2 Comparação da análise estrutural

Apresentar FTOOL versus sistema.

Usar tabelas e, quando útil, figuras.

### 5.3 Resultados do pré-dimensionamento

Mostrar:

- barras tracionadas;
- barras comprimidas;
- modo governante;
- camadas;
- quantidade física de palitos.

### 5.4 Aplicação web

Mostrar o fluxo final do sistema com capturas das principais telas.

### 5.5 Estudo de caso

Executar uma ponte representativa do contexto da CP3.

### 5.6 Limitações

Discutir:

- propriedades adotadas para a madeira;
- hipóteses de cálculo;
- formato FTL parcialmente interpretado;
- dependências computacionais;
- diferenças entre modelo e protótipo físico.

## Critério de conclusão

Cada objetivo específico da introdução deve possuir uma evidência correspondente nos resultados ou na metodologia.

---

# 10. Capítulo 6 — Conclusão

Arquivo:

`2-textuais/6-conclusao.tex`

Escrever somente depois dos resultados.

## Estrutura

1. retomar o problema;
2. retomar o objetivo geral;
3. sintetizar a solução desenvolvida;
4. apresentar as principais evidências obtidas;
5. responder à questão de pesquisa;
6. apontar limitações;
7. propor trabalhos futuros.

## Não fazer

- introduzir referências novas;
- apresentar resultados que não apareceram no Capítulo 5;
- afirmar validação experimental sem experimento;
- repetir literalmente a introdução.

---

# 11. Referências

Arquivo:

`3-pos-textuais/referencias.bib`

## Regras

- Preferir artigo, livro, norma, documentação oficial e publicação institucional.
- Conferir autores, título, ano, volume, páginas e DOI na fonte original.
- Não usar uma referência apenas porque ela tem palavras parecidas com o tema.
- Toda citação deve sustentar a afirmação feita no texto.
- Não colocar referências na bibliografia apenas para aumentar a quantidade.

## Pendências atuais

- [ ] Corrigir o sobrenome de Pedro Cesar Miranda e Silva em `lamberti2025ponte`.
- [ ] Completar páginas/ISSN de `martha2022ftool`.
- [x] Confirmar o DOI de `silva2026ruptura` diretamente na fonte oficial: `10.37702/REE2236-0158.v45p389-402.2026`, conferido no artigo integral em 06/10/2026 e incluído no `.bib`.
- [ ] Adicionar um livro clássico de Análise Estrutural ou Resistência dos Materiais.
- [ ] Fazer nova conferência de todas as chaves ao final do Capítulo 2.
- [ ] Fazer conferência final entre todas as `\cite{}` e o arquivo `.bib`.

---

# 12. Figuras e tabelas que provavelmente serão necessárias

Planejar desde cedo:

- [ ] diagrama geral da arquitetura/fluxo da ferramenta;
- [ ] exemplo de estrutura no FTOOL;
- [ ] representação do modelo interpretado;
- [ ] diagrama axial;
- [ ] deformada;
- [ ] visualização do pré-dimensionamento;
- [ ] captura da interface web;
- [ ] tabela FTOOL versus ferramenta;
- [ ] tabela de verificação manual do pré-dimensionamento;
- [ ] tabela de trabalhos relacionados.

Toda figura deve ser mencionada e explicada no texto.

---

# 13. Checklist de consistência técnica

Manter estas regras durante todo o trabalho:

- [ ] Informar unidades sempre que necessário.
- [ ] Informar convenção de sinais dos esforços.
- [ ] Não confundir tração com compressão.
- [ ] Não confundir camadas com palitos físicos.
- [ ] Não apresentar valores padrão como propriedades medidas experimentalmente.
- [ ] Não afirmar que o sistema prevê exatamente a ruptura real da ponte.
- [ ] Separar correção do software de validade física do modelo.
- [ ] Não descrever funcionalidades que não estejam implementadas.
- [ ] Conferir o repositório do software antes de documentar arquitetura ou comportamento.
- [ ] Diferenciar claramente FTOOL, anaStruct e resultados produzidos pela ferramenta.

---

# 14. Próximas ações imediatas

Executar nesta ordem:

## Agora

1. [ ] concluir a redação do Capítulo 2;
2. [ ] adicionar uma referência clássica de análise estrutural/resistência dos materiais;
3. [ ] revisar a NBR 7190-1 e o artigo `silva2026ruptura` para fundamentar compressão/flambagem;
4. [ ] revisar todas as citações do Capítulo 2.

## Depois

5. [ ] escrever o Capítulo 3 — Trabalhos Relacionados;
6. [ ] montar a tabela comparativa dos trabalhos;
7. [ ] revisar o código atual do `ftool-parser-python`;
8. [ ] reescrever o Capítulo 4 com base na implementação atual;
9. [ ] definir os casos utilizados na verificação;
10. [ ] executar as comparações e registrar os resultados;
11. [ ] escrever o Capítulo 5;
12. [ ] escrever o Capítulo 6.

## Por último

13. [ ] revisar Introdução e objetivos com base nos resultados;
14. [ ] escrever Resumo;
15. [ ] escrever Abstract;
16. [ ] definir o título final;
17. [ ] revisar referências;
18. [ ] revisar figuras e tabelas;
19. [ ] revisar formatação;
20. [ ] compilar e ler o PDF completo como se fosse o avaliador.

---

# 15. Quando surgir dúvida sobre onde colocar um conteúdo

Usar esta regra:

| Pergunta | Capítulo |
| --- | --- |
| Por que este problema importa? | Introdução |
| O que é esse conceito? | Fundamentação teórica |
| O que outros autores fizeram? | Trabalhos relacionados |
| Como este trabalho foi realizado? | Metodologia |
| O que foi obtido? | Resultados |
| O que esses resultados significam? | Resultados e discussão |
| O objetivo foi alcançado? | Conclusão |
| O que poderia ser feito depois? | Trabalhos futuros |

Se um trecho não responder claramente a nenhuma dessas perguntas, verificar se ele realmente precisa estar no TCC.

---

# 16. Histórico de atualizações

## 07/10/2026 — Fundamentação teórica e roteiro

- Mantida a prioridade no Capítulo 2, antes de Trabalhos Relacionados e Metodologia.
- Registrada a ampliação da fundamentação com seções sobre análise estrutural, FTOOL, anaStruct e pré-dimensionamento de barras tracionadas e comprimidas.
- Registrado o ajuste de redação do problema de pesquisa na introdução.
- Registrada a substituição do conteúdo inicial da metodologia por texto provisório; capítulo permanece pendente.
- Preservado o novo modelo deste roteiro, com finalidades, estruturas sugeridas, critérios de conclusão e checklists por capítulo.
- Identificadas pendências de revisão textual e técnica na fundamentação, sem marcar o capítulo como consolidado.
- Verificação: BibTeX e pdfLaTeX concluídos sem erros; PDF com 32 páginas, sem referências indefinidas no log final. `git diff --check` sem erros. A compilação não substitui a revisão técnica e bibliográfica pendente.
- Commit desta etapa: `docs: amplia fundamentacao teorica e atualiza roteiro do TCC`. Publicação no GitHub pendente.
