# 3. DOCUMENTO DE ESPECIFICAÇÃO DE REQUISITOS DE SOFTWARE

Nesta parte do trabalho você deve detalhar a documentação dos requisitos do sistema proposto de acordo com as seções a seguir. Ressalta-se que aqui é utilizado como exemplo um sistema de gestão de cursos de aperfeiçoamento.

## 3.1 Objetivos deste documento
Esta especificação de requisitos tem como objetivo fornecer um guia completo e preciso para o desenvolvimento do sistema Senectus, uma plataforma digital que visa melhorar a qualidade de vida de idosos, conectando-os a serviços de saúde, atividades físicas e conteúdos informativos. Este documento serve como referência para a equipe de desenvolvimento, stakeholders do projeto e futuros colaboradores, garantindo que o sistema seja construído de acordo com as necessidades dos usuários e os objetivos do projeto.

## 3.2 Escopo do produto

### 3.2.1 Nome do produto e seus componentes principais
O produto que será criado neste projeto será denominado "Senectus" que da tradução direta do latim para o português, significa idoso, referenciando o público alvo que o sistema visa atingir. Para que o sistema Senectus seja capaz de atingir seus objetivos, o mesmo terá os seguintes componentes:
- **Biblioteca de Exercícios**: componente dedicado a exibir uma biblioteca de exercícios em formato de vídeo, fornecendo instruções de execução para os idosos;
- **Gestor de cadastro de profissionais**: componente dedicado a gerenciar o fluxo de cadastro de novos profissionais no Senectus;
- **Gestor de eventos remotos e presenciais**: componente dedicado a fornecer meios de cadastro de novos eventos relacionados a saúde e exercícios por profissionais. Além disso, o componente também é responsável por permitir a pesquisa destes eventos e fornecer informações sobre como participar;
- **Gestor de pesquisa de profissionais**: componente dedicado a gerenciar o fluxo de pesquisa de profissionais da área da saúde, fornecendo os meios de contato mais adequados do mesmo.
- **Página de blog**: componente dedicado a fornecer conteúdos e recomendações sobre saúde e bem estar para o grupo da terceira idade;

### 3.2.2 Missão do produto
Senectus visa fornecer informações e ferramentas para o melhorar a qualidade de vida dos idosos. Trazendo assim, novos meios de contato com profissionais da saúde, uma coletânea de informações sobre exercícios físicos adequados para o público e uma série de eventos das quais os usuários podem participar.

### 3.2.3 Limites do produto
Senectus apesar de fornecer os meios de contatos e informações de eventos, não é responsável por promover nenhum meio de comunicação ou pagamento dentro da plataforma, utilizando-se assim, de sistemas externos, como, por exemplo, os clientes de email e telefone responsáveis para estabelecer um meio de comunicação entre o idoso e o profissional, ou links de formulários externos para permitir que os organizadores de eventos coletem informações dos participantes. Além disso, Senectus não armazena os vídeos de instruções de exercícios, necessitando, assim, de uma plataforma externa para tal.

### 3.2.4 Benefícios do produto

| # | Benefício | Valor para o Cliente |
|--------------------|------------------------------------|----------------------------------------|
| 1 | Facilidade no acesso de um amplo catalogo de exercícios variados | Essencial |
| 2 | Acessibilidade para idosos com pouca experiência digital | Essencial |
| 3 | Acesso rápido e sem necessidade de cadastro | Essencial |
| 4 | Facilidade na busca por profissionais | Essencial |
| 5 | Facilidade em cadastrar profissionais | Essencial |
| 6 | Acesso ao blog de conteúdos | Recomendável |
| 7 | Conexão entre eventos físicos e virtuais | Recomendável |

## 3.3 Descrição geral do produto

### 3.3.1 Requisitos Funcionais

| Código | Requisito Funcional (Funcionalidade) | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| RF1 | Gerenciar Curso de Aperfeiçoamento |	Processamento de Inclusão, Alteração, Exclusão e Consulta de Cursos de Aperfeiçoamento |
| RF2 |	Gerenciar Professor	| Processamento de Inclusão, Alteração, Exclusão e Consulta de professores |
| RF3	| Gerenciar Matrícula |	Processamento de Inclusão, Alteração, Exclusão e Consulta de Matrículas de alunos em Cursos de Aperfeiçoamento |
| ... |	...	| ... |

### 3.3.2 Requisitos Não Funcionais

| Código | Requisito Não Funcional (Restrição) |
|--------------------|------------------------------------|
| RNF1 | O ambiente operacional a ser utilizado é o Windows XP. |
| RNF2 | O sistema deverá executar em um computador configurado com uma impressora de tecnologia laser ou de jato de tinta, a ser usada para impressão dos relatórios. |
| RNF3 |	Segurança	O produto deve restringir o acesso por meio de senhas individuais para o usuário. |
| ... |	... |	... |

### 3.3.3 Usuários 

| Ator | Descrição |
|--------------------|------------------------------------|
| Profissional da Saúde |	Usuário profissional da saúde que deseja encontrar novas formas de divulgação do seu trabalho com idosos. |
| Familiar de Idoso |	Familiar que necessita contratar um profissional para auxiliar seu parente. |
| Idoso |	Usuário da terceira idade com compreensão das tecnologias e que deseja encontrar um profissional de saúde ou instruções para realizar exercícios em casa, como alongamentos. |	
| Organizador de Evento | Usuário que deseja divulgar melhor o evento com foco no público de terceira idade em que é responsável. |

## 3.4 Modelagem do Sistema

### 3.4.1 Diagrama de Casos de Uso
Como observado no diagrama de casos de uso da Figura 1, a secretária poderá gerenciar as matrículas e professores no sistema, enquanto o coordenador, além dessas funções, poderá gerenciar os cursos de aperfeiçoamento.

#### Figura 1: Diagrama de Casos de Uso do Sistema.

![dcu](https://github.com/user-attachments/assets/41f6b731-b44e-43aa-911f-423ad6198f47)
 
### 3.4.2 Descrições de Casos de Uso

Cada caso de uso deve ter a sua descrição representada nesta seção. Exemplo:

#### Gerenciar Professor (CSU01)

Sumário: A Secretária realiza a gestão (inclusão, remoção, alteração e consulta) dos dados sobre professores.

Ator Primário: Secretária.

Ator Secundário: Coordenador.

Pré-condições: A Secretária deve ser validada pelo Sistema.

Fluxo Principal:

1) 	A Secretária requisita manutenção de professores.
2) 	O Sistema apresenta as operações que podem ser realizadas: inclusão de um novo professor, alteração de um professor, a exclusão de um professor e a consulta de dados de um professor.
3) 	A Secretária seleciona a operação desejada: Inclusão, Exclusão, Alteração ou Consulta, ou opta por finalizar o caso de uso.
4) 	Se a Secretária desejar continuar com a gestão de professores, o caso de uso retorna ao passo 2; caso contrário o caso de uso termina.

Fluxo Alternativo (3): Inclusão

a)	A Secretária requisita a inclusão de um professor. <br>
b)	O Sistema apresenta uma janela solicitando o CPF do professor a ser cadastrado. <br>
c)	A Secretária fornece o dado solicitado. <br>
d)	O Sistema verifica se o professor já está cadastrado. Se sim, o Sistema reporta o fato e volta ao início; caso contrário, apresenta um formulário em branco para que os detalhes do professor (Código, Nome, Endereço, CEP, Estado, Cidade, Bairro, Telefone, Identidade, Sexo, Fax, CPF, Data do Cadastro e Observação) sejam incluídos. <br>
e)	A Secretária fornece os detalhes do novo professor. <br>
f)	O Sistema verifica a validade dos dados. Se os dados forem válidos, inclui o novo professor e a grade listando os professores cadastrados é atualizada; caso contrário, o Sistema reporta o fato, solicita novos dados e repete a verificação. <br>

Fluxo Alternativo (3): Remoção

a)	A Secretária seleciona um professor e requisita ao Sistema que o remova. <br>
b)	Se o professor pode ser removido, o Sistema realiza a remoção; caso contrário, o Sistema reporta o fato. <br>

Fluxo Alternativo (3): Alteração

a)	A Secretária altera um ou mais dos detalhes do professor e requisita sua atualização. <br>
b)	O Sistema verifica a validade dos dados e, se eles forem válidos, altera os dados na lista de professores, caso contrário, o erro é reportado. <br>
 
Fluxo Alternativo (3): Consulta

a)	A Secretária opta por pesquisar pelo nome ou código e solicita a consulta sobre a lista de professores. <br>
b)	O Sistema apresenta uma lista professores. <br>
c)	A Secretária seleciona o professor. <br>
d)	O Sistema apresenta os detalhes do professor no formulário de professores. <br>

Pós-condições: Um professor foi inserido ou removido, seus dados foram alterados ou apresentados na tela.

### 3.4.3 Diagrama de Classes 

A Figura 2 mostra o diagrama de classes do sistema. A Matrícula deve conter a identificação do funcionário responsável pelo registro, bem com os dados do aluno e turmas. Para uma disciplina podemos ter diversas turmas, mas apenas um professor responsável por ela.

#### Figura 2: Diagrama de Classes do Sistema.
 
![classes](https://github.com/user-attachments/assets/4d0db51f-95bb-451c-ba03-fa35b9bb0d28)

### 3.4.4 Descrições das Classes 

| # | Nome | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| 1	|	Aluno |	Cadastro de informações relativas aos alunos. |
| 2	| Curso |	Cadastro geral de cursos de aperfeiçoamento. |
| 3 |	Matrícula |	Cadastro de Matrículas de alunos nos cursos. |
| 4 |	Turma |	Cadastro de turmas.
| 5	|	Professor |	Cadastro geral de professores que ministram as disciplinas. |
| ... |	... |	... |
