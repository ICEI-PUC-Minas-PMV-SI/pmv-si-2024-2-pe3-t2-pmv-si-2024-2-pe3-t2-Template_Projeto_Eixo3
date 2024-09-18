# 3. DOCUMENTO DE ESPECIFICAÇÃO DE REQUISITOS DE SOFTWARE

Nesta parte do trabalho você deve detalhar a documentação dos requisitos do sistema proposto de acordo com as seções a seguir. Ressalta-se que aqui é utilizado como exemplo um sistema de gestão de cursos de aperfeiçoamento.

## 3.1 Objetivos deste documento
Descrever e especificar as necessidades e funções do projeto Doe Aqui.

## 3.2 Escopo do produto

### 3.2.1 Nome do produto e seus componentes principais
O produto será denominado Doe Aqui. (Ele terá somente um componente (módulo) com os devidos elementos necessários à gestão de cursos.)

### 3.2.2 Missão do produto
Facilitar a Doação e Encontrar Instituições: O principal objetivo do projeto é auxiliar as pessoas a aprenderem como doar de forma mais eficiente e a encontrar instituições locais que estejam realizando campanhas de caridade. Isso permitirá que mais indivíduos contribuam para causas nobres de maneira fácil e direta.

### 3.2.3 Limites do produto
O Doe Aqui não fornece nenhuma forma de entrega ou recolhimento de doações.

### 3.2.4 Benefícios do produto

| # | Benefício | Valor para o Cliente |
|--------------------|------------------------------------|----------------------------------------|
|1	| Facilidade no cadastro de dados |	Essencial |
|2 | Facilidade na recuperação de informações | Essencial | 
|3 | Segurança com os dados coletados| Essencial | 
|4	| Praticidade no uso do software	| Recomendável | 
|5	| Software com o custo baixo | Recomendável | 


## 3.3 Descrição geral do produto

### 3.3.1 Requisitos Funcionais

| Código | Requisito Funcional (Funcionalidade) | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| RF1 | Página inicial |	O usuário deve escolher se deseja doar ou arrecadar. |
| RF2	| Cadastro de ponto de coleta |	O sistema deve permitir o cadastro de um ponto de coleta. |
| RF3 |	Pesquisar pontos de coleta	| O sistema deve permitir que o usuário pesquise o que ele deseja doar para encontrar pontos de coleta. |
| RF4	| Instruções de doação |	O sistema precisa apresentar intruções de como doar. |
| RF5	| Gerenciamento de ponto de coleta |	O sistema deve permitir o gerenciamento do ponto de coleta: editar, salvar e excluir. |
| RF6	| Listagem de pontos de coleta |	O sistema deve listar os pontos de coleta. |
| RF7	| Informações do ponto de coleta |	O sistema deve abrir as informações do ponto de coleta ao clicar. |

### 3.3.2 Requisitos Não Funcionais

| Código | Requisito Não Funcional (Restrição) |
|--------------------|------------------------------------|
| RNF1 | O sistema deve garantir a segurança dos dados de acordo com a LGPD. |
| RNF2 | O sistema deve possibilitar qualquer realização de tarefas em no máximo 4 cliques. |
| RNF3 |	O sistema deve processar requisições dos usuários de no máximo 3 segundos. |
| RNF4 |	O sistema deve ser desenvolvido na tecnologia JavaScript/React. |

### 3.3.3 Usuários 

| Ator | Descrição |
|--------------------|------------------------------------|
| Arrecadador |	Usuário responsável por anunciar, organizar e receber doações. |
| Doador |	Usuário que vai procurar pontos de coleta para realizar sua doação. |

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
 
![dcu](https://github.com/user-attachments/assets/97ab1aa8-eb03-4b58-9ad5-1697d414a451)

### 3.4.4 Descrições das Classes 

| # | Nome | Atributos | Métodos | Descrição |
|--------------------|------------------------------------|----------------------------------------|------------------------------------|------------------------------------|
| 1	|	Usuário | nome:String, e-mail:String, dataCadastro:Date | reclamar() |	Cadastro de informações e metodos relativos aos Usuários. |
| 2	| PJ | CNPJ:Number | setCNPJ(), adicionarCliente(), excluirCliente(), editarCliente(), rastrearDoacoes() |	Cadastro de informações e metodos relativos as Pessoas Jurídicas. |
| 3 |	PF | CPF:Number | setCPF(), doar() |	Cadastro de informações e metodos relativos as Pessoas Físicas. |
| 4 |	Doação |	nomeItem:String, descricaoItem:String, condicoes:String | adicionarDoacao() |	Cadastro de informações e metodos relativos as Doações. |
| 5	|	CNPJ |	CNPJ:Number |  |	Cadastro de informações relativos aos CNPJ. |
| 6	|	CPF |	CPF:Number |  |	Cadastro de informações relativos aos CPF. |
| 7	|	Interface Panel | | adicionarCliente(String), excluirCliente(String), editarCliente(String), rastearDoacoes() |	Cadastro de métodos relativos ao Interface Panel. |
