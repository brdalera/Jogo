# Jogo – assets ajustados

Todos os PNGs têm transparência real, borda sem halo claro e quadros de tamanho uniforme.

## camera_npc_luz/
4 quadros 520x373 com a MESMA moldura e alinhamento (resíduos das bordas removidos).
luz_0_claro, luz_1_medio, luz_2_escuro, luz_3_medio_claro + luz_sheet_2x2.png
Sugestão de pisca: 0 -> 1 -> 2 -> 1 -> 3 -> 0 (ritmo de 0,5 s ou mais por quadro).

## johnny/walk/
Cada quadro tem o mesmo tamanho (120x163). Âncora: centro do tronco na horizontal, pés na base.
- dir_r0c0..c3: de costas
- dir_r1..r3: de lado (olhando para a direita; espelhe para a esquerda). r3c0 é um quadro agachado.
- base_r0c0, base_r0c1: de frente / 3/4 de frente; base_r0c2, base_r0c3: de costas
- base_r1c0..c3: caminhada de lado (com bolso/cinto visível)
Corrigido: mancha branca (buraco) na faixa da cabeça nos quadros de costas.

## johnny/duto/
Quadros 352x200. O duto (retângulo preto) fica na MESMA posição em todos os quadros da linha;
use essa posição para colocar o duto na ilha.
- r0: agachar e entrar (duto à direita) | r1: andar e entrar | r2: pular e subir (duto acima) | r3: repete r0 (duplicado)

## johnny/extras_engatinhar/
6 poses recortadas da linha quebrada de movimentos_base (4 engatinhando, 1 meio curvado, 1 curvado).
A ordem do ciclo precisa ser conferida.

## npc/
- bravo: 16 quadros 240x209 (reações de raiva). rotina_cafe: 20 quadros 240x177 (idle, bocejo, café, levantar, cadeira vazia, volta rindo).
- Quadros de uma mesma linha compartilham a base (monitor) alinhada.

## Problemas que NÃO dá para resolver por código (precisam de nova geração/retoque)
- npc/rotina_cafe/rotina_r4c0: NPC em pé ao lado da cadeira cortado na borda direita na imagem original.
- Antebraços do NPC (quadros do café) e alguns dedos (bravo r1c1/r1c2) têm falhas de transparência vindas do recorte original.
- Johnny de frente andando e engatinhar completo não existem nas folhas originais.
- Escala: a ilha (2816 px de largura) e os sprites do Johnny (~165 px de altura) vieram em escalas diferentes; escolha uma escala única.
