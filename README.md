# Projeto Integrador - Modelo

Um modelo para o desenvolvimento do Projeto Integrador do Curso de Técnico em Desenvolvimento de Sistemas para a Internet Integrado ao Ensino Médio do IFC - Campus Araquari.

Professores: [Marco André Mendes](github.com/marcoandre) e [Alann Perini](https://github.com/AlannKPerini).

**Equipe:**
- [Matheus Marques Gobetti,](github.com/Matheus3DD4) [Ana Laura de Paiva,](https://github.com/analauracpaiva) e [Thiago de Paula](https://github.com/thigasmonteiro)
  
# Situação Problema

A Biblioteca Pública do Paraná (BPP) fundada em 1857 trabalha há anos proporcionando o acesso da população à leitura. Com um acervo de cerca de 730 mil volumes, entre livros, periódicos, fotografias e materiais multimídia. 

Além de oferecer atendimento especial às crianças e às pessoas com deficiência visual ou baixa visão, tendo um acervo com mais de 7.200 itens — entre obras em braille e audiolivros. A biblioteca é gerenciada por uma equipe de bibliotecários e outros funcionários, como assistentes, técnicos e funcionários administrativos. Esses profissionais ajudam a gerenciar o fluxo de materiais e fornecem assistência aos usuários, auxiliando na manutenção do espaço físico.

Em seu espaço físico a biblioteca recebe diariamente em média 2 mil pessoas e realiza aproximadamente 500 empréstimos de livros. O processo de empréstimos de livros ocorre da seguinte maneira: Antes de poder fazer um empréstimo o usuário se cadastra na biblioteca, fornecendo informações pessoais básicas e criando um perfil. Após escolher no acervo os livros que deseja emprestar a pessoa se dirige ao balcão de atendimento e assim o bibliotecário registra os livros emprestados. O prazo do empréstimo é definido e ao final deve-se devolver os materiais à biblioteca. Se os materiais não forem devolvidos dentro do prazo estipulado, a biblioteca cobr uma multa por atraso.

 A biblioteca como instituição aberta ao público necessita de melhor atuação em seus atendimentos, pela sua demanda é necessário um sistema que permita o acesso do cliente de forma que fique viável, seguindo o devido processo de cadastro e empréstimo, tornando o contato com o acervo prático e não necessariamente na biblioteca.

# Descrição da proposta

A BPP não oferece esses serviços como: empréstimo de materiais, renovação de empréstimos, etc, diretamente para o usuário. Então, nesse primeiro momento os livros são o objeto piloto do sistema, pela sua corriqueira usabilidade. Com um sistema prático para os usuários da biblioteca haverá um aumento no número de empréstimos e agilidade no serviço dos atendentes, funcionando da seguinte forma: ao usuário informar o livro que deseja realizar o empréstimo o bibliotecário consulta o sistema e verifica se o título está disponível para que, então se registre o empréstimo. Caso o título não esteja disponível, o bibliotecário registra um pedido de reserva do livro e informa ao usuário a data prevista de disponibilidade. Quando o empréstimo for realizado o bibliotecário informa ao usuário a data de devolução que será automaticamente prevista pelo sistema. Quando ocorrer a devolução de um título o bibliotecário verifica se houve atraso na devolução, se o livro foi devolvido dentro do prazo o bibliotecário registra no sistema, já se o livro foi devolvido com atraso é calculado a multa e registrado a devolução no sistema. Com a devolução, o sistema também irá atualizar o status do título, permitindo a geração de relatórios de empréstimos, devoluções e reservas para facilitar o controle de gestão da biblioteca.

**Regras de Negócio**

**RN01 - Cadastro de Leitores:** Os funcionários precisam fazer o cadastro do usuário para que o tal poder realizar empréstimos.

**RN02 - Realizar Empréstimo:** Para realizar o empréstimo é preciso que o usuário seja cadastrado e não tenha nenhuma multa pendente.

**RN03 - Registro de Empréstimo:** O bibliotecário deverá ter acesso a registros de empréstimosde todos os usuários. O sistema deve permitir que o bibliotecário tenha acesso aos registros de empréstimos.

**RN04 - Pagamento de Multa:** O usuário que ultrapassar 15 dias da data de devolução do livro deverá pagar a multa de acordo com os dias de atraso como listado na tabela padrão da BPP.

**RN05 - Catalogação de livros:** O sistema deve permitir que o bibliotecário faça atualizações diárias de todo o acervo literário.

**RN06 - Controle de estoque:** O sistema deve permitir o parâmetro dos livros presentes na biblioteca.


# Requisitos funcionais

**Entradas**
- **R.F. 01 - Cadastro de Leitores:** O sistema terá uma interface onde ocorrerá o cadastro de novos usuários.
  - **Dados necessários:** Nome completo, CPF, número de telefone, e-mail, senha e login.
  - **Usuários:** bibliotecário/novos funcionários.

- **R.F. 02 - Acesso de Usuário:** O sistema permitirá o funcionário verificar se o usuário pode acessar, caso possa, poderá analisar sua situação e realizar empréstimos. 
  - **Dados necessários:** Nome/Login, senha, nível de permissão. 
  - **Usuários:** bibliotecário.

- **R.F. 03 - Autenticação de Devolução:** Não é necessário cadastro para devolução.
  - **Dados necessários:** Nome/Login, senha, nível de permissão. 
  - **Usuários:** bibliotecário.


**Processamentos**

- **R.F 04 - Devolução do Livro:** O sistema deve permitir verificar se há atrasos após a devolução.
  - **Dados Necessários:** nenhum
  - **Usuários:** bibliotecário.

- **R.F 05 - Empréstimo do Livro:** O sistema deve permitir verificar se há pendências para a validação de empréstimos.
  - **Dados Necessários:** Nome completo, e-mail, Telefone, CPF, Endereço.
  - **Usuários:** bibliotecário.

- **R.F 06 - Catalogação Diária de Livros:** O sistema deve permitir que o bibliotecário faça atualizações dos livros (re)adicionados ao acervo literário no dia.
  - **Dados Necessários:** Nome/Login, senha.
  - **Usuários:** bibliotecário.

**Saída**

- **R.F 07: Relatório de Empréstimo:** O sistema deve permitir emitir os relatórios de empréstimos de livros e quantidade emprestada.
  - **Dados Necessários:** data inicial, data final 
  - **Usuários:** bibliotecário

- **R.F 08: Relatório de Empréstimos Atrasados:** O sistema deve permitir emitir os relatórios de empréstimos de livros atrasados e quantidade emprestada,  
  - **Dados Necessários:** data inicial, data final. 
  - **Usuários:** bibliotecário.

- **R.F 09: Relatório de Clientes:** O sistema deve permitir emitir os relatórios dos usuários, fazendo a verificação das pendências para a validação de empréstimos.
  - **Dados Necessários:** Nome completo.
  - **Usuários:** bibliotecário.

# Requisitos não funcionais

- **R.F. 01 - Software em Processamento:** O sistema faz parte de um ambiente interno e será utilizado de acordo com as horas de trabalho da biblioteca, estando ativo 16 horas por dia, durante os dias úteis da semana.

- **R.F. 02 - Autenticação:** Para realizar o acesso ao sistema é necessário ter um usuário de autenticação criado pelo administrador, além da possibilidade de solicitar um envio de redefinição de senha.

- **R.F. 03 - Aviso de empréstimo:** O sistema deve avisar o usuário que tem empréstimos em aberto 1(um) dia antes do vencimento.

- **R.F. 04 - Limitação de empréstimo:** O sistema deve limitar um número de empréstimos para cada usuário a depender do tempo de cadastro na BPP.

- **R.F. 06 - Tecnologia Front-end:** Para a exibição em front-end, o software utilizará o CSS3 e o HTML5, além das bibliotecas de Vue.

- **R.F. 07 - Tecnologia Back-end:**  O software será desenvolvido pela linguagem de programação Django.
