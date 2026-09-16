---
name: aulas-numeros-idosos
description: Planeia e cria aulas semanais de matemática para idosos da disciplina «Os números à nossa volta», incluindo título apelativo, objetivo, pergunta inicial e apresentação HTML Reveal.js coerente com o template oficial, pronta a apresentar e exportar para PDF. Usar ao propor temas, preparar aulas, rever apresentações ou adaptar atividades desta disciplina.
---

# Aulas de «Os números à nossa volta»

## Contexto

Preparar aulas práticas e participativas sobre os números presentes no quotidiano: preços, notícias, saúde, rótulos, televisão e outros exemplos familiares. Escrever em português europeu, com linguagem clara e tom descontraído. Tratar os participantes como adultos; evitar infantilização. Explicar cada conceito com um exemplo concreto antes de introduzir símbolos ou fórmulas.

## Processo de planeamento

1. Identificar o tema, a duração e eventuais materiais fornecidos. Se faltar um tema, propor um tema específico ligado ao quotidiano e avançar com uma hipótese explícita.
2. Criar um título curto, apelativo e bem-humorado; preferir trocadilhos compreensíveis ou adaptações naturais de provérbios portugueses. Evitar trocadilhos forçados e ambiguidade que esconda o tema.
3. Formular um objetivo geral observável, centrado numa capacidade útil após a aula, com uma frase simples.
4. Criar uma pergunta inicial aberta que convide todos a partilhar experiências sem exigir cálculo ou expor informação pessoal. Preparar uma pergunta de seguimento caso o grupo fique em silêncio.
5. Organizar uma sequência: conversa inicial, exemplo próximo da vida real, exploração guiada, participação ou jogo, aplicação prática e síntese. Ajustar o número de slides à duração e ao ritmo do grupo.
6. Rever valores e afirmações factuais. Distinguir exemplos inventados de dados reais; indicar fonte e data dos dados reais no próprio slide ou em notas visíveis. Em temas médicos ou financeiros, usar exemplos educativos e evitar inferir decisões pessoais a partir de um número isolado.

## Produção do HTML

1. Usar `assets/template-aula.html` desta competência como ponto de partida **em todas as aulas**. No repositório original, consultar também `examples/html_template_os_numeros_a_nossa_volta.html`; se houver uma versão mais recente desse ficheiro, atualizar o recurso da competência antes de criar a aula.
2. Preservar as regras visuais e técnicas do template: Reveal.js 5.2.1, apresentação 1024 × 768 (4:3), paleta teal, fonte Atkinson Hyperlegible, numeração manual, navegação por rato/teclado e estilos de impressão. Manter os seletores de slide como descendentes de `.reveal .slides section`, sem exigir que o `section` seja filho direto: no modo PDF o Reveal.js coloca cada slide dentro de `.pdf-page`. Preservar também a regra `html.reveal-print .reveal .slides .pdf-page > section`, que repõe a dimensão e o padding 4:3 na exportação. Alterar o conteúdo dos slides e acrescentar componentes no mesmo vocabulário visual, sem substituir a folha de estilos inteira.
3. Incluir sempre capa, objetivo geral, pergunta inicial, desenvolvimento interativo e fecho com uma ideia prática. Usar os layouts do template conforme o conteúdo; eliminar os slides de demonstração que não sirvam a aula. Atualizar `<title>`, título da capa, subtítulo, rótulos e números dos slides.
4. Manter um conceito principal por slide, texto breve, letras grandes, contraste forte e exemplos legíveis à distância. Fazer cada composição caber integralmente na área `.slide-content` (entre 78 px do topo e 68 px do fundo); deixar uma margem visual antes do número do slide. Antes de reduzir a tipografia, encurtar texto, dividir o conteúdo por mais slides ou escolher um layout com menos cartões. Evitar tabelas densas, excesso de animações e dependência exclusiva da cor. Reservar tempo para conversa e para resolver exercícios em conjunto.
5. Para interação com rato, usar os controlos Reveal.js e verificar que nenhum elemento essencial depende de hover. Usar `fragment` apenas quando a revelação gradual ajuda a discussão; garantir que todo o conteúdo aparece no PDF.
6. Guardar cada aula como HTML autónomo na pasta `aulas/` da raiz do repositório. Usar sempre o nome `aulaXX.html`, em que `XX` é o número da aula com pelo menos dois algarismos: `aulas/aula01.html`, `aulas/aula02.html`, `aulas/aula11.html` (e `aulas/aula100.html` a partir da centésima aula). Confirmar o número da aula e verificar se o ficheiro já existe antes de o criar ou substituir. Manter caminhos relativos ou URLs públicos para recursos necessários ao alojamento estático; não depender de ficheiros locais da máquina do professor.

## Verificação e entrega

1. Abrir o HTML num navegador e percorrer todos os slides com o rato. Confirmar texto, acentos, numeração, legibilidade, ausência de conteúdo cortado e funcionamento em ecrã 4:3.
2. Incluir o atalho visual `Imprimir / PDF`, que abre a própria aula com `?view=print`; este é o modo de exportação do Reveal.js. Na nova página, usar Chrome ou Chromium e abrir a impressão do navegador para guardar como PDF, com orientação horizontal, margens a zero e gráficos de fundo ativados. Configurar `pdfSeparateFragments: false` e `pdfMaxPagesPerSlide: 1` para imprimir todos os elementos de cada slide numa única página.
3. Inspecionar o PDF para confirmar formato 4:3, um slide por página, conteúdo completo e ausência do atalho de impressão.
4. Entregar o HTML, o título, o objetivo geral e a pergunta inicial em resumo. Indicar o caminho do ficheiro e qualquer dependência externa relevante. Se o navegador ou a exportação não estiverem disponíveis, declarar exatamente o que foi validado e o que ficou por testar.

## Recurso

- `assets/template-aula.html`: template oficial completo e base obrigatória para o HTML de cada aula.
