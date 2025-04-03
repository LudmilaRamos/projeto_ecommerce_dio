# Desafio Modelo Entidade-Relacionamento

## Descrição do Projeto

Este projeto consiste em um modelo entidade-relacionamento para um sistema de e-commerce. O modelo abrange a gestão de **clientes**, **pedidos**, **produtos**, **fornecedores**, **pagamentos** e **entregas**, com a implementação dos seguintes requisitos:

- **Cliente PJ e PF**: A conta pode ser **Pessoa Jurídica (PJ)** ou **Pessoa Física (PF)**, mas não pode ser ambas.
- **Pagamento**: O sistema permite cadastrar **múltiplas formas de pagamento** para um pedido.
- **Entrega**: Cada pedido tem um status de entrega e um código de rastreamento.

O objetivo deste modelo é refletir as operações essenciais de um sistema de e-commerce, incluindo a associação entre clientes, produtos, pedidos, pagamentos e entregas.

## Entidades e Relacionamentos

O modelo inclui as seguintes entidades:
1. **Cliente**
2. **Produto**
3. **Fornecedor**
4. **Vendedor Terceiro**
5. **Pedido**
6. **Pagamento**
7. **Entrega**
8. **Devolução**

A seguir, as relações entre as entidades:
- **Produto** — *muitos para muitos* — **Fornecedor**(via tabela intermediária **Disponibilização**)
- **Produto** — *muitos para muitos* — **Vendedor Terceiro** (via tabela intermediária **produtos por vendedor**)
- **Produto** — *muitos para muitos* — **Pedido** (via tabela intermediária **Relação produto_pedido**)
- **Produto** — *muitos para muitos* — **Estoque** (via tabela intermediária **Relação produto_estoque**)
- **Cliente** — *1 para muitos* — **Pedido**
- **Pedido** — *1 para muitos* — **Pagamento**
- **Pedido** — *1 para 1* — **Entrega**
- **Pedido** — *1 para 1* — **Devolução** 
  

## Diagrama Entidade-Relacionamento

O modelo de dados foi representado visualmente no diagrama a seguir:

![Diagrama ER] (ecommerce.png) 





