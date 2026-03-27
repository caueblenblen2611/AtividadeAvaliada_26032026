Sistema Integrado de Gestão de Farmácia – Saúde & Vida

Aluno: Caue B Blenblen
RA: 24001158

1. Regras de Negócio

RN01 – Um produto só poderá ser vendido caso exista quantidade suficiente no estoque da unidade.

RN02 – Sempre que uma venda for realizada, o sistema deverá atualizar automaticamente o estoque da farmácia.

RN03 – Quando uma venda for realizada a prazo, o sistema deverá gerar automaticamente um registro em contas a receber para controle do pagamento.

RN04 – Sempre que uma compra de produtos for registrada no sistema, o estoque da unidade deverá ser atualizado e também deverá ser criado um registro em contas a pagar.

RN05 – Caso a quantidade de um produto fique abaixo do nível mínimo definido, o sistema deverá emitir um alerta para o gerente da unidade.

RN06 – Apenas usuários com perfil de gerente poderão cadastrar novos produtos ou alterar informações já existentes no sistema.

RN07 – Medicamentos controlados somente poderão ser vendidos após a validação e autorização de um farmacêutico responsável.

2. Requisitos Funcionais

RF01 – O sistema deve permitir o cadastro de novos clientes.

RF02 – O sistema deve permitir a pesquisa de produtos pelo nome, código de barras ou fabricante.

RF03 – O sistema deve permitir o registro de vendas realizadas no balcão da farmácia.

RF04 – O sistema deve verificar automaticamente se existe quantidade disponível em estoque antes de confirmar uma venda.

RF05 – O sistema deve permitir o registro de compras de produtos feitas com fornecedores.

RF06 – O sistema deve possibilitar o controle e gerenciamento de contas a pagar.

RF07 – O sistema deve possibilitar o controle e gerenciamento de contas a receber.

RF08 – O sistema deve emitir um comprovante ao final de cada venda realizada.

RF09 – O sistema deve permitir a geração de relatórios de vendas por período.

RF10 – O sistema deve permitir a geração de relatórios relacionados ao estoque de cada unidade.

3. Requisitos Não Funcionais

RNF01 – O sistema deve possuir controle de acesso baseado em perfis de usuários, garantindo que cada pessoa tenha acesso apenas às funções permitidas.

RNF02 – O sistema deve garantir a segurança e integridade das informações armazenadas.

RNF03 – A interface do sistema deve ser simples e fácil de utilizar, facilitando o trabalho dos funcionários.

RNF04 – As consultas realizadas no sistema devem responder rapidamente, preferencialmente em até 3 segundos.

RNF05 – O sistema deve estar disponível para utilização durante todo o horário de funcionamento das farmácias.

4. Atores do Sistema

Os principais usuários que irão interagir com o sistema são:

Atendente – responsável por registrar vendas, consultar produtos e identificar clientes.

Farmacêutico – responsável por validar receitas médicas e autorizar a venda de medicamentos controlados.

Gerente – responsável por cadastrar produtos, atualizar preços e gerenciar o estoque da unidade.

Financeiro – responsável pelo controle das contas a pagar e contas a receber.

Administrador – responsável por gerenciar usuários, permissões e configurações gerais do sistema.

Cliente – pessoa que realiza a compra de produtos na farmácia.

5. Casos de Uso

UC01 – Cadastrar Cliente
UC02 – Consultar Produto
UC03 – Registrar Venda
UC04 – Validar Receita Médica
UC05 – Registrar Venda a Prazo
UC06 – Registrar Compra
UC07 – Atualizar Estoque
UC08 – Gerenciar Contas a Pagar
UC09 – Gerenciar Contas a Receber
UC10 – Gerar Relatórios

6. Relações Include e Extend
Relações <<include>>

Registrar Venda <<include>> Consultar Produto

Registrar Venda <<include>> Atualizar Estoque

Registrar Compra <<include>> Atualizar Estoque

Relações <<extend>>

Registrar Venda a Prazo <<extend>> Registrar Venda

Validar Receita <<extend>> Registrar Venda

Cadastrar Cliente <<extend>> Registrar Venda

7. Documentação dos Casos de Uso
UC01 – Cadastrar Cliente

Ator: Atendente

Descrição:
Este caso de uso permite que um atendente registre um novo cliente no sistema, possibilitando que suas compras fiquem vinculadas ao seu histórico.

Fluxo Principal

O atendente seleciona a opção de cadastrar cliente no sistema.
O sistema solicita as informações do cliente.
O atendente preenche os dados necessários.
O sistema registra o cliente no banco de dados.
UC02 – Consultar Produto

Ator: Atendente

Descrição:
Permite que o atendente busque informações sobre um produto disponível na farmácia.

Fluxo Principal

O atendente informa o nome do produto, código de barras ou fabricante.
O sistema realiza a busca no banco de dados.
O sistema apresenta as informações do produto encontrado.
UC03 – Registrar Venda

Ator: Atendente

Descrição:
Este caso de uso permite registrar a venda de produtos para um cliente.

Fluxo Principal

O atendente inicia uma nova venda no sistema.
O sistema solicita os produtos que serão vendidos.
O atendente informa os itens e as quantidades.
O sistema verifica se existe estoque disponível.
O sistema registra a venda realizada.
O estoque é atualizado automaticamente.
O sistema emite o comprovante da venda.
UC04 – Validar Receita

Ator: Farmacêutico

Descrição:
Permite que o farmacêutico valide receitas médicas quando a venda envolve medicamentos controlados.

Fluxo Principal

O sistema identifica que o produto exige receita médica.
O farmacêutico analisa a receita apresentada pelo cliente.
O farmacêutico autoriza ou rejeita a venda do medicamento.
UC05 – Registrar Venda a Prazo

Ator: Atendente

Descrição:
Permite registrar uma venda em que o pagamento será realizado posteriormente.

Fluxo Principal

O atendente realiza o registro da venda normalmente.
O atendente seleciona a opção de pagamento a prazo.
O sistema gera automaticamente um registro em contas a receber.
UC06 – Registrar Compra

Ator: Gerente

Descrição:
Permite registrar compras realizadas com fornecedores para reposição do estoque.

Fluxo Principal

O gerente seleciona a opção registrar compra.
O sistema solicita os dados da compra.
O gerente informa o produto, quantidade e fornecedor.
O sistema registra a compra no sistema.
O estoque da unidade é atualizado.
O sistema gera automaticamente uma conta a pagar.
UC07 – Atualizar Estoque

Ator: Sistema

Descrição:
Esse processo ocorre automaticamente sempre que ocorre uma venda, compra, devolução ou qualquer movimentação de produtos.

UC08 – Gerenciar Contas a Pagar

Ator: Financeiro

Descrição:
Permite que o setor financeiro acompanhe e registre pagamentos de fornecedores e outras despesas da unidade.

UC09 – Gerenciar Contas a Receber

Ator: Financeiro

Descrição:
Permite controlar valores que ainda serão recebidos de clientes ou empresas conveniadas.

UC10 – Gerar Relatórios

Ator: Gerente / Financeiro

Descrição:
Permite visualizar informações importantes para análise e tomada de decisão.

Exemplos de relatórios disponíveis

Produtos mais vendidos
Estoque por unidade
Vendas por período
Compras realizadas por fornecedor
Contas a pagar e contas a receber
8. Diagrama de Casos de Uso (PlantUML)
@startuml

actor Atendente
actor Farmaceutico
actor Gerente
actor Financeiro
actor Administrador

Atendente --> (Registrar Venda)
Atendente --> (Consultar Produto)
Atendente --> (Cadastrar Cliente)

Farmaceutico --> (Validar Receita)

Gerente --> (Registrar Compra)
Gerente --> (Gerar Relatorios)

Financeiro --> (Gerenciar Contas a Pagar)
Financeiro --> (Gerenciar Contas a Receber)

(Registrar Venda) .> (Consultar Produto) : <<include>>
(Registrar Venda) .> (Atualizar Estoque) : <<include>>
(Registrar Compra) .> (Atualizar Estoque) : <<include>>

(Registrar Venda a Prazo) .> (Registrar Venda) : <<extend>>
(Validar Receita) .> (Registrar Venda) : <<extend>>
(Cadastrar Cliente) .> (Registrar Venda) : <<extend>>

@enduml
9. Diagrama de Atividade – Registrar Venda
@startuml

start

:Cliente solicita um produto;

:Atendente consulta o produto no sistema;

if (Produto disponível no estoque?) then (Sim)

:Registrar venda;
:Atualizar estoque;
:Emitir comprovante da venda;

else (Não)

:Informar ao cliente que o produto está indisponível;

endif

diagrama 1= <img width="377" height="367" alt="image" src="https://github.com/user-attachments/assets/bbf51b86-fb5a-4a7a-9fe7-cb45beba2b7d" />
diagrama 2= <img width="426" height="367" alt="image" src="https://github.com/user-attachments/assets/acf2c331-1c77-47f0-9ef2-635d59b9b824" />
diagrama 3= <img width="552" height="541" alt="image" src="https://github.com/user-attachments/assets/c99555e3-638a-4b37-9388-75e76eff2d67" />
diagrama 4= <img width="331" height="312" alt="image" src="https://github.com/user-attachments/assets/1998188b-4afe-41f3-9033-717e3f0f842c" />
diagrama 5= <img width="210" height="358" alt="image" src="https://github.com/user-attachments/assets/6a819689-d23e-479c-ac78-0c430fec7089" />
diagrama 6= <img width="163" height="468" alt="image" src="https://github.com/user-attachments/assets/788bc4ba-2e35-45b7-aa96-42da01a9db95" />
diagrama 7= <img width="403" height="312" alt="image" src="https://github.com/user-attachments/assets/14e66455-4741-4759-9b37-5ec1632d76c1" />
diagrama 8= <img width="353" height="367" alt="image" src="https://github.com/user-attachments/assets/575def0d-544b-4da0-95c0-374530a18310" />
diagrama 9= <img width="373" height="367" alt="image" src="https://github.com/user-attachments/assets/9c00f715-818d-4ac8-9d24-cd4f9f968d1d" />
diagrama 10= <img width="439" height="367" alt="image" src="https://github.com/user-attachments/assets/e337666e-16fd-44a8-b164-58e1a6921fbc" />


stop
