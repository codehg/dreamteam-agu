# Visão geral

Esse documento determina o fluxo de trabalho para cada projeto, desde sua concepção até o ciclo de desenvolvimento.

## Engenharia de Requisitos

O processo de engenharia de requisitos compreende um conjunto de atividades. Elas estão listadas a seguir:

1. Concepção: Aqui é preciso definir quem são os clientes (ex.: pessoas da AGU) responsáveis por passar suas necessidades para os analistas de requisitos e qual a visão geral do produto que deve ser desenvolvido.
2. Elicitação: Nessa etapa, os requisitos são descobertos através de algumas técnicas. É preciso ter a disposição os stakeholders para que sejam interrogados quanto as suas necessidades para o sistema. As técnicas que podem ser utilizadas são:
   * Entrevistas;
   * Questionários;
   * *Brainstorming*;
   * Análise de documentos;
   * Observação;
   * Introspecção;
3. Especificação: Nessa etapa, detalha-se cada requisito descrito em linguagem natural em modelos conceituais. Alguns diagramas são:
   * Diagramas de Caso de Uso;
   * Diagramas de bloco;
   * Diagramas Paramétricos;
   * Diagramas de Requisitos;
   * Diagramas de Sequência;
   * Diagramas de Máquina de Estados;
4. Revisão: Nessa etapa, os requisitos devidamente especificados(documentados) serão verificados com todos os envolvidos antes de seguirem para a prototipação.

O resultado dos processos acima será o documento de visão [padrão da IBM](https://www.ibm.com/docs/pt-br/elm/6.0.5?topic=requirements-vision-document) com o backlog do produto definido em *Recursos do Produto*.

## Prototipação

Uma vez que os requisitos tenham sido devidamente elicitados e documentados, será necessário realizar a prototipação das telas para evitar que código tenha que ser refatorado por conta de aspectos visuais. O *designer* deve validar as telas com os analistas de requisitos para garantir que as telas atendem os requisitos. As telas devem ser vinculadas aos itens do *backlog* do produto e posteriormente inseridas nas *issues* criadas.

## Planejamento de Sprint

No início de *sprint*, a equipe (analistas de requisitos e time de desenvolvimento) deve se reunir para fazer a escolha das atividades da *sprint* com base no *backlog* do produto. Após a seleção de atividades, o item selecionado do *backlog* do produto deve ser transformado em uma *issue* no repositório, conforme o *template* de *issue* adequado ([bug](../issue_templates/bug.md) ou [feature](/issue_templates/feature.md)). Cada desenvolvedor ou grupo de desenvolvedores deve ser atribuída uma *issue* que deve ser entregue ao término da *sprint*. Um item do *backlog* do produto (que essencialmente é um requisito), poderá ser resolvido por completo por uma ou mais *issues*.

## Desenvolvimento

Após a *issue* ser designada para um desenvolvedor ele deve iniciar os trabalhos necessários para sua realização. O desenvolvedor deve atualizar o estado da *issue* para “*Em andamento*” e buscar atualizar o *Scrum Master* a medida que algum impedimento ou dúvida ocorra.

É papel do desenvolvedor se manter atento aos padrões estabelecidos para realizar suas contribuições, como o padrão de [*commits*](/politicas/contribuicao.md#Commits) e também ao [*template* da **Merge Request**](../merge_request_templates/mr_template.md) que deverá ser aberta ao final do desenvolvimento.

Idealmente, a *issue* deverá ter uma carga de trabalho que caiba no período de uma única *sprint*, caso o trabalho seja maior que o esperado o *Scrum Master* deverá ser notificado para poder tomar as providências necessárias, como dividir a *issue* em unidades menores de trabalho.

## Testes

O desenvolvimento de testes unitários faz parte da etapa de desenvolvimento da *issue* e devem cobrir as principais funcionalidades e trechos críticos do código, seguindo os padrões de cobertura definidos para o projeto em questão.

Além disso, testes manuais devem ser realizados antes de a *issue* poder ser enviada para revisão. Código que não foi testado não deve ser considerado completo.

## Revisão

Ao finalizar a *issue* o desenvolvedor deverá abrir uma *Merge Request* (ou equivalente) e preencher as informações disponibilizadas no [*template de Merge Request*](/merge_request_templates/mr_template.md) e atualizar o estado da *issue* como “*Em revisão*”. Estas informações são importantes para possibilitar a validação de seu trabalho por outros desenvolvedores por meio da explicação das alterações e de como testá-las, além de lembrar o desenvolvedor da *issue* de passos extras como realizar o teste de seu código e atualizar a documentação.

O código deverá ser revisado por outro desenvolvedor da equipe, seguindo os passos descritos no *Merge Request* para realizar o teste do código. A revisão também pode ser realizada por um *Scrum Master* ou *Product Owner* para garantir que atende aos requisitos definidos na *issue*. Idealmente, durante o processo de revisão o revisor entra na *branch* em questão e verifica se o código funciona. Nessa etapa ele também pode fazer testes manuais e colocar comentários no *merge request* corresponde caso haja necessidade.

O desenvolvedor da *issue* é responsável por resolver os conflitos de código que impação a realização do *merge* de suas alterações. Quando o *merge* é feito a *issue* deverá ter seu estado atualizado para “*Em validação*”.

## Validação

A etapa final de uma *issue* ocorre com a validação das alterações por parte do cliente/PO/analista de requisitos. Nesta etapa deverá ser demonstrado para o cliente o que a *issue* desenvolvida faz e comparar com os requisitos levantados para a *issue*.

Caso o cliente/PO/analista aprove as alterações, a *issue* pode ser considerada “*Concluída*”, caso o que foi desenvolvido não corresponda com o que foi pedido deverá ser retornada como **Defeito**, caso o cliente mude de ideia ou tenha algum desagrado em relação ao comportamento da *issue*, ou em relação a algum aspecto do *design* uma nova *issue* de **Melhoria** deverá ser criada.

## Fechamento da Sprint

Ao final de uma *sprint* a equipe deve se reunir para fazer um balanço do que foi desenvolvido, concluído e do que virará dívida técnica. Além disso, a equipe deve se posicionar sobre aspectos positivos e negativos do que ocorreu na *sprint* para aprimorar o processo de desenvolvimento.



