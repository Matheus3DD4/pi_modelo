# Projeto Integrador - Modelo

Um modelo para o desenvolvimento do Projeto Integrador do Curso de Técnico em Desenvolvimento de Sistemas para a Internet Integrado ao Ensino Médio do IFC - Campus Araquari.

Professores: [Marco André Mendes](github.com/marcoandre) e [Alann Perini](https://github.com/AlannKPerini).

**Equipe:**
- [Matheus Marques Gobetti](github.com/Matheus3DD4)

# Como usar esse modelo para o Projeto Integrador

1. Faça um fork desse repositório para a sua conta do GitHub.
2. Clone o repositório para o seu computador.
3. Abra o arquivo README.md no seu editor de texto favorito (recomendamos o [Visual Studio Code](https://code.visualstudio.com/)).
4. Tenha instalada a extensão [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one) no seu editor de texto.
5. Edite o arquivo README.md com as informações do seu projeto.

# Situação Problema

A Biblioteca Pública do Paraná (BPP) fundada em 1857 trabalha há anos proporcionando o acesso da população à leitura. Com um acervo de cerca de 730 mil volumes, entre livros, periódicos, fotografias e materiais multimídia. 

Além de oferecer atendimento especial às crianças e às pessoas com deficiência visual ou baixa visão, tendo um acervo com mais de 7.200 itens — entre obras em braille e audiolivros. A biblioteca é gerenciada por uma equipe de bibliotecários e outros funcionários, como assistentes, técnicos e funcionários administrativos. Esses profissionais ajudam a gerenciar o fluxo de materiais e fornecem assistência aos usuários, auxiliando na manutenção do espaço físico

Em seu acervo a biblioteca recebe diariamente em média 2 mil usuários e realiza aproximadamente 500 empréstimos de livros. Com a aquisição de livros através da compra ou doação. O processamento para livros novos se dá em 4 etapas: 1 - Catalogar, 2 - Etiquetar, 3 - Registrar e 4 - Disponibilizar. 
1 - Catalogação: É atribuído ao livro um número de classificação e um número de identificação único para que possa ser encontrado facilmente na biblioteca.
2 - Etiquetamento:  O livro é preparado para uso na biblioteca, incluindo a aplicação de etiquetas de identificação e de segurança.
3 - Registro: O livro é registrado na planilha Excel de gerenciamento da biblioteca, incluindo por coluna informações como título, autor, editora, ano de publicação, etc
4 - Disponibilização: O livro é disponibilizado na estante da biblioteca para os usuários acessarem e emprestarem

 A biblioteca como instituição necessita de segurança e precisão de dados para que seja funcional e pela sua demanda é necessário um sistema que permita agilidade ao mesmo tempo que cumpra esses requisitos para que o acesso ao acervo seja prático.

# Descrição da proposta

A BPP não possui sistema onde cada material é catalogado em um sistema de gerenciamento, que ajuda a gerenciar o empréstimo, devolução, reserva e inventário dos materiais. Nem oferece serviços como empréstimo de materiais, renovação de empréstimos, reservas e acesso a esses recursos online. Nesse primeiro momento os livros são o objeto piloto do sistema, pela sua corriqueira usabilidade. Com um sistema prático haverá um aumento no número de empréstimos e agilidade no serviço dos atendentes, funcionando da seguinte forma: ao usuário informar o livro cujo deseja realizar o empréstimo o bibliotecário consulta o sistema e verifica se o título está disponível para que, então se registre o empréstimo. Caso o título não esteja disponível, o bibliotecário registra um pedido de reserva do livro e informa ao usuário a data prevista de disponibilidade. Quando o empréstimo for realizado o bibliotecário informa ao usuário a data de devolução que será automaticamente prevista pelo sistema. Quando ocorrer a devolução de um título o bibliotecário verifica se houve atraso na devolução, se o livro foi devolvido dentro do prazo o bibliotecário registra no sistema, já se o livro foi devolvido com atraso é calculado a multa e registrado a devolução no sistema. Com a devolução, o sistema também irá atualizar o status do título, permitindo a geração de relatórios de empréstimos, devoluções e reservas para facilitar o controle de gestão da biblioteca.
