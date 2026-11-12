# LernWelten · Mathematik

Protótipo original para uma demonstração escolar na semana de 16–20/11/2026. Interface em alemão, Klassen 2–4. Destino exclusivo: `eucidioarruda/lernwelten`.

## Experimentar

Abra `index.html` no navegador ou acesse a página publicada. Não há instalação, conta nem serviço de dados. São 96 tarefas (32 por série), em cinco oficinas, além de um jogo espacial com rodadas geradas por série:

- Zahlenwerkstatt: materiais que podem ser arrastados com mouse, caneta ou dedo, com alternativa por toque: placas vermelhas de centenas, palitos azuis de dezenas, bolinhas verdes de unidades e cubos verdes de milhares, sequências, números ouvidos, marcação na reta e saltos do sapinho.
- Rechen-Abenteuer: comparar estratégias, justificar compensações, descobrir algarismos, explorar operações inversas e voltar com saltos na reta.
- Größen-Labor: estimar a massa de uma mochila, um apontador e uma lancheira em uma balança que oscila ao receber pesos. Os pesos podem ser arrastados, colocados e retirados. As respostas aceitam intervalos aproximados explicitados após o acerto. Também é possível estimar, comparar unidades, ordenar pesos, marcar o fim de um segmento em uma régua e questionar se aparência implica massa.
- Formen-Atelier: identificar formas desenhadas e giradas, explorar seus vértices e comparar propriedades. Quadrados são apresentados como um caso particular de retângulo. Há duas tarefas de associação por arraste ou toque entre objetos cotidianos e sólidos (esfera, cilindro, cubo, prisma retangular, cone e pirâmide).
- Lesen & Forschen: três textos com informações em dois trechos e seleção do trecho decisivo (inclusive um caso em que os dados úteis já estão no primeiro trecho); três desafios abertos de Fermi com informações conhecidas, dados faltantes, estratégia de investigação, suposições, estimativa, modelo e verificação. Modelos abertos não recebem nota automática.

Após cada acerto, a criança pode registrar um raciocínio ou uma nova pergunta. O campo é aberto: não recebe correção automática. As explicações são lidas pela pessoa responsável pela aula. A balança é uma simulação discreta com pesos em múltiplos de 50 g. Os desenhos dos pesos têm tamanhos distintos e são esquemáticos, não estão em escala física. A régua é uma representação em centímetros, não uma régua calibrada ao tamanho da tela. O caminho final dos saltos fica registrado no painel e no CSV; usar o botão de desfazer remove o último salto desse caminho.

As cores dos valores posicionais seguem a convenção verde (unidades e milhares), azul (dezenas) e vermelho (centenas). As placas, palitos e bolinhas são uma adaptação digital solicitada pelo usuário, não uma reprodução integral de material Montessori. Referência para a convenção: https://montessoriacademy.com.au/material-spotlight-large-number-cards/ .

## Roteiro de apresentação (5–8 minutos)

1. Selecione o perfil fictício Fuchs e Klasse 3.
2. Abra Größen-Labor: formule uma previsão para a caixa, adicione pesos e observe o equilíbrio.
3. Responda 750 g, explique o caminho e continue para estimativas e comparações.
4. Mostre a ordenação de pesos e discuta por que unidades diferentes precisam ser relacionadas.
5. Abra Lehrkraft: veja tentativas, dicas, previsão, explicação e exportação CSV.
6. Mostre Zahlenwerkstatt e a escolha de estratégias em Rechen-Abenteuer.

## Limites da demonstração

Somente os perfis fictícios Fuchs, Eule e Otter. Resultados no localStorage deste navegador, sem sincronização, autenticação ou gestão de turmas. O painel é aberto. Não utilizar dados reais de alunos. Em modo privado ou com armazenamento bloqueado, os resultados podem desaparecer. A fala de números depende das vozes alemãs disponíveis no dispositivo e tem alternativa para leitura pela pessoa responsável. O motor de fala do navegador pode usar serviços do sistema: não há garantia de operação de áudio totalmente offline.

Cada oficina contém seis tarefas fixas por série; o Lernstand-Check reutiliza a primeira tarefa das cinco oficinas. É uma amostra para conversa pedagógica, não uma avaliação padronizada, validação curricular ou diagnóstico. Tentativas iniciais contam a cada nova abertura; tarefas concluídas contam IDs únicos. Tempo é o tempo decorrido desde a abertura, incluindo pausas. Pedidos de dicas sem uma resposta posterior não ficam registrados. O histórico mostra as últimas 50 respostas; o CSV exporta todas as respostas do perfil e série selecionados.

## Fontes e preservação

Foram lidos os anexos `foedima_3_4_sob_zv_zr1000000.pdf`, `AB50_Gewichte.pdf`, `ab_3.11` (PDF de adição escrita) e `lad-zahlen-hoeren-zr1mio-swt-getauscht.pptx`. Seus formatos pedagógicos orientaram as tarefas originais. Nenhuma página, ilustração, áudio ou arquivo-fonte desses materiais foi republicado. Os avisos dos materiais Klett restringem seu uso aos próprios fins de ensino; os originais permanecem fora deste repositório.

Referências de páginas existentes, somente para leitura:

- https://github.com/eucidio/mathe — blob observado `d09bd01fea18f8b9ae8dca786299ec183ce65f6a`
- https://github.com/eucidio/mathe2 — blob observado `9661b099574d6248a7b7135b96b6ee2166a7fdad`
- https://github.com/eucidio/deutsch
- https://github.com/eucidio/alien

Os dois jogos Mathe têm estrutura espacial com contas, níveis, pontuação e modo professor. Este protótipo foi escrito de forma independente para ampliar a investigação e a explicação. Por solicitação do usuário, os formatos permanecem próximos aos materiais fornecidos, com variação de números e representações interativas próprias. A versão anterior permanece no histórico Git; os resultados locais anteriores permanecem armazenados. Tarefas substituídas permanecem no histórico de resultados, mas não contam na contagem das 32 tarefas atuais. Nenhum arquivo das contas/repositórios anteriores foi modificado. MiniMax e Zebra são referências mencionadas pelo usuário; não se afirma fidelidade a uma edição específica, ainda não fornecida. Deutsch e Medien são apenas expansões futuras identificadas na página.

## Publicação

Página estática sem dependências externas: GitHub Pages, branch main, pasta raiz. O commit inicial do repositório permanece no histórico. A publicação e a visibilidade pública deste novo projeto foram autorizadas expressamente pelo usuário.

## Touch, acessibilidade e movimento

O arraste usa Pointer Events, captura do ponteiro e tratamento de cancelamento; não depende de HTML drag-and-drop. Nos materiais e pesos, um toque adiciona, e um toque no item colocado o retira. Na associação de sólidos, toque primeiro no objeto e depois no destino. Os gestos ficam restritos aos materiais e ao jogo; o restante da página continua rolável. Os controles têm pelo menos 48 px de altura. O layout foi conferido em larguras de 390 e 1024 px no navegador. O caminho compartilhado de eventos foi testado também com eventos unitários de tipo touch; falta validação em um iPad físico com Safari. Movimento reduzido desativa a oscilação e os efeitos decorativos; as bolas do jogo continuam se movendo como parte da mecânica e podem ser pausadas.

O milhar é representado por um cubo verde, com grade frontal de 10 × 10. São representações digitais esquemáticas, sem promessa de escala física. A balança usa massas de exemplo, não valores universais de objetos reais. A tolerância pertence a cada tarefa; o equilíbrio visual usa a massa exata do modelo, enquanto uma resposta próxima pode ser aceita.

Ao voltar com o sapo por um caminho já percorrido, os trechos correspondentes são apagados. Um retorno parcial encurta o último arco; se o retorno ultrapassar o início, apenas o caminho restante é desenhado. O botão de desfazer remove a última etapa.

## Weltraum-Mathe

O jogo é novo e independente dos jogos antigos. A operação fica em um painel claro de alto contraste. Multiplicação usa `·` e divisão usa `:`. As respostas aparecem em três bolas que caem: toque na bola, mova a nave com o dedo e use Fangen, ou use teclado. Há pausa, encerramento e revisão das contas.

A série, turma demonstrativa (a/b/c) e ano escolar são escolhidos antes de iniciar. Na Klasse 2, adição/subtração ficam até 100 e multiplicação/divisão usam 2, 5 e 10; Klasse 3 usa adição/subtração até 1 000 e tabuadas pequenas; Klasse 4 amplia até 10 000 e inclui multiplicações de dois algarismos por um algarismo. Essa seleção é uma progressão para o protótipo, não validação curricular individual.

Após três acertos o nível sobe. A duração de uma queda diminui progressivamente até o limite de 4,5 s. A missão termina após 12 rodadas ou cinco erros/bolas perdidas. As contas erradas ficam visíveis por mais tempo, com a resposta, antes da próxima rodada. São salvos localmente até 100 resumos de missões, separados dos registros das oficinas. Turma e ano são demonstrativos, sem cadastro nem autenticação real. Os registros antigos sem turma continuam disponíveis no painel; novos registros são filtrados pela turma/ano selecionados.

## Referência Fermi fornecida

Foi lido o arquivo de 21 páginas `Fermi-Aufgaben Unterrichtsreihe.pdf`, enviado pelo usuário. As orientações de investigação de dados faltantes, estratégias, modelagem, verificação e explicação (incluindo a checklist da p. 15) orientaram as atividades originais. O PDF, suas ilustrações e páginas não foram enviados ao repositório. Os enunciados de duas partes são próprios e distinguem perguntas com resposta determinada dos modelos abertos de Fermi.
