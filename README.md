# LernWelten · Mathematik

Protótipo original para uma demonstração escolar na semana de 16–20/11/2026. Interface em alemão, Klassen 2–4. Destino exclusivo: `eucidioarruda/lernwelten`.

## Experimentar

Abra `index.html` no navegador ou acesse a página publicada. Não há instalação, conta nem serviço de dados. São 54 tarefas (18 por série), em três oficinas:

- Zahlenwerkstatt: material de valor posicional, sequências, números ouvidos, reta numérica e investigação de erros.
- Rechen-Abenteuer: comparar estratégias, justificar compensações, descobrir algarismos e resolver situações de partilha e agrupamento.
- Größen-Labor: prever e testar uma massa desconhecida na balança, estimar, comparar unidades, ordenar pesos e questionar se aparência implica massa.

Após cada acerto, a criança pode registrar um raciocínio ou uma nova pergunta. O campo é aberto: não recebe correção automática. As explicações são lidas pela pessoa responsável pela aula. A balança é uma simulação discreta com pesos em múltiplos de 50 g, não um simulador físico.

## Roteiro de apresentação (5–8 minutos)

1. Selecione o perfil fictício Fuchs e Klasse 3.
2. Abra Größen-Labor: formule uma previsão para a caixa, adicione pesos e observe o equilíbrio.
3. Responda 750 g, explique o caminho e continue para estimativas e comparações.
4. Mostre a ordenação de pesos e discuta por que unidades diferentes precisam ser relacionadas.
5. Abra Lehrkraft: veja tentativas, dicas, previsão, explicação e exportação CSV.
6. Mostre Zahlenwerkstatt e a escolha de estratégias em Rechen-Abenteuer.

## Limites da demonstração

Somente os perfis fictícios Fuchs, Eule e Otter. Resultados no localStorage deste navegador, sem sincronização, autenticação ou gestão de turmas. O painel é aberto. Não utilizar dados reais de alunos. Em modo privado ou com armazenamento bloqueado, os resultados podem desaparecer. A fala de números depende das vozes alemãs disponíveis no dispositivo e tem alternativa para leitura pela pessoa responsável. O motor de fala do navegador pode usar serviços do sistema: não há garantia de operação de áudio totalmente offline.

Cada oficina contém seis tarefas fixas por série; o Lernstand-Check reutiliza a primeira tarefa das três oficinas. É uma amostra para conversa pedagógica, não uma avaliação padronizada, validação curricular ou diagnóstico. Tentativas iniciais contam a cada nova abertura; tarefas concluídas contam IDs únicos. Tempo é o tempo decorrido desde a abertura, incluindo pausas. Pedidos de dicas sem uma resposta posterior não ficam registrados. O histórico mostra as últimas 50 respostas; o CSV exporta todas as respostas do perfil e série selecionados.

## Fontes e preservação

Foram lidos os anexos `foedima_3_4_sob_zv_zr1000000.pdf`, `AB50_Gewichte.pdf`, `ab_3.11` (PDF de adição escrita) e `lad-zahlen-hoeren-zr1mio-swt-getauscht.pptx`. Seus formatos pedagógicos orientaram as tarefas originais. Nenhuma página, ilustração, áudio ou arquivo-fonte desses materiais foi republicado. Os avisos dos materiais Klett restringem seu uso aos próprios fins de ensino; os originais permanecem fora deste repositório.

Referências de páginas existentes, somente para leitura:

- https://github.com/eucidio/mathe — blob observado `d09bd01fea18f8b9ae8dca786299ec183ce65f6a`
- https://github.com/eucidio/mathe2 — blob observado `9661b099574d6248a7b7135b96b6ee2166a7fdad`
- https://github.com/eucidio/deutsch
- https://github.com/eucidio/alien

Os dois jogos Mathe têm estrutura espacial com contas, níveis, pontuação e modo professor. Este protótipo foi escrito de forma independente para ampliar a investigação e a explicação. Nenhum arquivo das contas/repositórios anteriores foi modificado. MiniMax e Zebra são referências mencionadas pelo usuário; não se afirma fidelidade a uma edição específica, ainda não fornecida. Deutsch e Medien são apenas expansões futuras identificadas na página.

## Publicação

Página estática sem dependências externas: GitHub Pages, branch main, pasta raiz. O commit inicial do repositório permanece no histórico. A publicação e a visibilidade pública deste novo projeto foram autorizadas expressamente pelo usuário.
