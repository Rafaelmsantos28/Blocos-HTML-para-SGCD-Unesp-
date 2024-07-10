# Manual de uso dos blocos de HTML no sistema SGCD

O bloco de HTML permite que você insira conteúdo HTML incorporado diretamente na sua grade.

É importante salientar, no entanto, que alguns cuidados devem ser tomados:

1. **Código HTML inválido pode "quebrar" completamente sua página**
   
   A inserção de código HTML inválido, ou o não fechamento de tags abertas pode potencialmente danificar o layout da sua página, e até o funcionamento do gerenciador de arquivos. Quando isso ocorrer, será necessário abrir um chamado de suporte técnico pelo e-mail sgcd@unesp.br e não há uma previsão exata de quanto o chamado poderá ser atendido.

2. **Evite ao máximo declarar CSS em tags de style no bloco de HTML**
   
   CSS declarado diretamente em tags `style` dentro de blocos HTML pode injetar alterações em partes padronizadas do layout, como títulos, parágrafos, barras de menu, etc. Prefira sempre utilizar CSS inline nas suas tags em vez de declarar um bloco `style`.

3. **Não é possível fazer a importação de Javascript utilizando a tag script**
   
   Por questões de segurança, a importação de Javascript por meio de tags é desativada. Ainda é possível, no entanto, utilizar Javascript em eventos de elementos, como `onclick` ou `onmouseover`.

4. **Conteúdos de bloco HTML não são garantidos em futuras atualizações do sistema**
   
   Qualquer conteúdo inserido por meio de blocos HTML pode eventualmente perder seu layout em futuras atualizações do Portal Unesp. Se em um momento houver uma grande atualização do layout do Portal, e essa atualização invalidar ou prejudicar conteúdos gerados por blocos HTML, a manutenção de tais conteúdos fica sob responsabilidade do grupo ou indivíduo responsável pelo subsite. As atualizações de layout do Portal podem ocorrer sem aviso.
