# Projeto Integrador - Modelo

Um modelo para o desenvolvimento do Projeto Integrador do Curso de Técnico em Desenvolvimento de Sistemas para a Internet Integrado ao Ensino Médio do IFC - Campus Araquari.

Professores: [Marco André Mendes](github.com/marcoandre) e [Alann Perini](https://github.com/AlannKPerini).

**Equipe:**
- [Matheus Marques Gobetti,](github.com/Matheus3DD4) [Ana Laura de Paiva](https://github.com/analauracpaiva) e [Thiago de Paula](https://github.com/thigasmonteiro)
  
# Situação Problema

  A Biblioteca Pública do Paraná (BPP) fundada em 1857 trabalha há anos proporcionando o acesso da população à leitura. Com um acervo de cerca de 730 mil volumes, entre livros, periódicos, fotografias e materiais multimídia. 

  Além de oferecer atendimento especial às crianças e às pessoas com deficiência visual ou baixa visão, tendo um acervo com mais de 7.200 itens — entre obras em braille e audiolivros. A biblioteca é gerenciada por uma equipe de bibliotecários e outros funcionários, como assistentes, técnicos e funcionários administrativos. Esses profissionais ajudam a gerenciar o fluxo de materiais e fornecem assistência aos usuários, auxiliando na manutenção do espaço físico.

  Em seu espaço físico a biblioteca recebe diariamente em média 2 mil pessoas e realiza aproximadamente 500 empréstimos de livros. O processo de empréstimos de livros ocorre da seguinte maneira: Antes de poder fazer um empréstimo o usuário se cadastra na biblioteca, fornecendo informações pessoais básicas e criando um perfil. Após escolher no acervo os livros que deseja emprestar a pessoa se dirige ao balcão de atendimento e assim o bibliotecário registra os livros emprestados. O prazo do empréstimo é definido e ao final deve-se devolver os materiais à biblioteca. Se os materiais não forem devolvidos dentro do prazo estipulado, a biblioteca cobrará uma multa por atraso.

  A biblioteca como instituição aberta ao público necessita de melhor atuação em seus atendimentos, pela sua demanda é necessário um sistema que permita o acesso do cliente de forma que fique viável, seguindo o devido processo de cadastro e empréstimo, tornando o contato com o acervo prático e não necessariamente na biblioteca.

# Descrição da proposta


A BPP não oferece esses serviços como: empréstimo de materiais, renovação de empréstimos, etc, diretamente para o usuário. Então, nesse primeiro momento os livros são o objeto piloto do sistema, pela sua corriqueira usabilidade. Com um sistema prático para os usuários da biblioteca haverá um aumento no número de empréstimos e agilidade no serviço dos atendentes, funcionando da seguinte forma: O usuário abre o aplicativo da biblioteca em seu dispositivo móvel . Ele já está previamente cadastrado e fez login usando suas credenciais. Na página inicial do aplicativo, o usuário é recebido com opções como "Buscar Livros", "Meu Perfil", "Empréstimos", entre outros. Ele seleciona a opção "Buscar Livros" para encontrar o livro que deseja emprestar. Na página de busca, o usuário digita o título do livro ou o nome do autor na barra de pesquisa e pressiona "Buscar". O aplicativo exibe uma lista de resultados correspondentes à pesquisa. O usuário encontra o livro desejado na lista de resultados e clica na sua capa para obter mais detalhes. Ele verifica a disponibilidade do livro para empréstimo e informações como o prazo de devolução. Satisfeito com a disponibilidade e os detalhes do livro, o usuário pressiona o botão "Empréstimo" na página de detalhes do livro. O aplicativo exibe uma mensagem confirmando o empréstimo e o prazo de devolução. O usuário precisa ir á BPP para retirar o livro dentro de 3 dias. Há a possibilidade de renovação do empréstimo caso seja necessário mais tempo para concluir a leitura pelo aplicativo. Mas o ponto forte do aplicativo é na seção "Empréstimos", onde o usuário pode visualizar seus livros atualmente emprestados e o periodo de progresso entre as datas de empréstimo e de devolução. O usuário recebe uma notificação por e-mail, lembrando-o da data de devolução próxima do livro. Ao final do prazo renovado o usuário é notificado das multas diárias de 1 real que irá receber a partir daquele dia, a não ser que devolva no mesmo dia na BPP. Após esse processo o aplicativo confirma a devolução do livro e remove-o da lista de empréstimos ativos do usuário.

**Regras de Negócio**

**RN01 - Cadastro de Leitores:** Os funcionários precisam fazer o cadastro do usuário na biblioteca antes para que o tal poder realizar empréstimos.

**RN02 - Realizar Empréstimo:** Para realizar o empréstimo é preciso que o usuário seja cadastrado e não tenha nenhuma multa pendente.

**RN03 - Registro de Empréstimo:** O usuário deverá ter acesso aos registros de seus empréstimos. 

**RN04 - Pagamento de Multa:** O usuário que ultrapassar 15 dias da data de devolução do livro deverá pagar a multa de acordo com os dias de atraso como listado na tabela padrão da BPP.

**RN05 - Status de livros:** O sistema deve permitir que o usuário tenha atualizações diárias de seu status literário.

# Requisitos funcionais

**Entradas**
- **R.F. 01 - Cadastro de Leitores:** O sistema terá uma interface onde ocorrerá o cadastro de novos usuários.
  - **Dados necessários:** Nome completo, CPF, e-mail, senha e login.
  - **Usuários:** Novos usuários.

- **R.F. 02 - Acesso de Usuário:** O sistema permitirá o usuário analisar sua situação e realizar empréstimos. 
  - **Dados necessários:** Nome/Login, senha, nível de permissão. 
  - **Usuários:** usuário.

**Processamentos**

- **R.F 03 - Devolução do Livro:** O sistema deve permitir verificar se há atrasos após a devolução.
  - **Dados Necessários:** login, senha.
  - **Usuários:** usuário.

- **R.F 04 - Empréstimo do Livro:** O sistema deve permitir verificar se há pendências para a validação de empréstimos.
  - **Dados Necessários:** Nome completo, e-mail, CPF.
  - **Usuários:** bibliotecário.

**Saída**

- **R.F 05: Relatório de Empréstimo:** O sistema deve permitir emitir os relatórios de empréstimos de livros e quantidade emprestada.
  - **Dados Necessários:** data inicial, data final 
  - **Usuários:** bibliotecário

- **R.F 06: Relatório de Empréstimos Atrasados:** O sistema deve permitir emitir os relatórios de empréstimos de livros atrasados e quantidade emprestada,  
  - **Dados Necessários:** data inicial, data final. 
  - **Usuários:** bibliotecário.

# Requisitos não funcionais

- **R.F. 01 - Software em Processamento:** O sistema faz parte de um ambiente interno e será utilizado de acordo com as horas de trabalho da biblioteca, estando ativo 16 horas por dia, durante os dias úteis da semana.

- **R.F. 02 - Autenticação:** Para realizar o acesso ao sistema é necessário ter um usuário de autenticação criado pelo administrador, além da possibilidade de solicitar um envio de redefinição de senha.

- **R.F. 03 - Aviso de empréstimo:** O sistema deve avisar o usuário que tem empréstimos em aberto 1(um) dia antes do vencimento.

- **R.F. 04 - Limitação de empréstimo:** O sistema deve limitar um número de empréstimos para cada usuário a depender do tempo de cadastro na BPP.

- **R.F. 06 - Tecnologia Front-end:** Para a exibição em front-end, o software utilizará o CSS3 e o HTML5, além das bibliotecas de Vue.

- **R.F. 07 - Tecnologia Back-end:**  O software será desenvolvido pela linguagem de programação Django.
