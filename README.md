# 📊 Refinando um Projeto Conceitual de Banco de Dados - E-COMMERCE

## 📋 Sobre o Projeto

Este projeto faz parte da **Database Experience** da **DIO** e tem como objetivo refinar um modelo conceitual de banco de dados para um sistema de e-commerce. O projeto apresenta uma estrutura completa e normalizada para gerenciar clientes, produtos, pedidos, pagamentos e entregas.

## 🎯 Objetivos

- Desenvolver um modelo de dados robusto e escalável
- Aplicar conceitos de normalização de banco de dados
- Implementar relacionamentos adequados entre entidades
- Suportar diferentes tipos de clientes (Pessoa Física e Pessoa Jurídica)
- Gerenciar todo o ciclo de vida de um pedido

### 📊 Diagrama Entidade-Relacionamento:
<p align="center">
  <img src="docs/images/imagem_2025-09-06_162359811.png" alt="Diagrama ER" width="700">
</p>

O projeto utiliza as seguintes tabelas principais:

### 👥 **Clientes**
- **Cliente**: Tabela base com informações gerais
- **ClientePF**: Especialização para Pessoa Física (CPF, data de nascimento)
- **ClientePJ**: Especialização para Pessoa Jurídica (CNPJ, razão social)

### 🛒 **Pedidos e Produtos**
- **Produto**: Catálogo de produtos com preço e estoque
- **Pedido**: Informações do pedido (data, valor total, status)
- **ItemPedido**: Itens específicos de cada pedido com quantidade e preço

### 💳 **Pagamento e Entrega**
- **Pagamento**: Dados de pagamento associados ao pedido
- **Entrega**: Informações de entrega e rastreamento

## 🔧 Características Técnicas

### ✅ **Recursos Implementados**

- **Herança de Tabelas**: Implementação de especialização/generalização para tipos de cliente
- **Relacionamentos 1:N**: Entre Cliente-Pedido, Pedido-ItemPedido, etc.
- **Integridade Referencial**: Chaves estrangeiras garantindo consistência
- **Normalização**: Estrutura normalizada evitando redundâncias
- **Flexibilidade**: Suporte a múltiplos tipos de pagamento e status

### 📋 **Principais Entidades**

```sql
Cliente (Base)
├── ClientePF (Herança - Pessoa Física)
└── ClientePJ (Herança - Pessoa Jurídica)

Pedido
├── ItemPedido (Composição)
├── Pagamento (1:1)
└── Entrega (1:1)

Produto (Relaciona com ItemPedido)
```

## 🗂️ Estrutura de Arquivos

```
📁 Refinando-um-Projeto-Conceitual-de-Banco-de-Dados-E-COMMERCE/
├── 📄 README.md
├── 📄 eCommerce.dblm
└── 📁 docs/
    ├── 📁 images/
    │   ├── imagem_2025-09-06_162359811.png

```

## 🚀 Como Utilizar:

### Pré-requisitos
- Sistema de Gerenciamento de Banco de Dados (MySQL, PostgreSQL, SQL Server, etc.)
- Ferramenta de modelagem de dados (para visualizar o arquivo .dblm)

### Implementação
1. Clone este repositório
2. Abra o arquivo `eCommerce.dblm` em sua ferramenta de modelagem preferida
3. Gere o script SQL a partir do modelo
4. Execute o script em seu SGBD

## 📈 Possíveis Melhorias Futuras

- [ ] Implementar auditoria (logs de alterações)
- [ ] Adicionar tabela de Categorias para produtos
- [ ] Criar sistema de avaliações e comentários
- [ ] Implementar carrinho de compras temporário
- [ ] Adicionar suporte a cupons de desconto
- [ ] Criar tabela de endereços separada
- [ ] Implementar histórico de preços

## 🛠️ Tecnologias Utilizadas

- **Modelagem**: DBDesigner/dbdiagram.io
- **Padrões**: Modelo Entidade-Relacionamento
- **Conceitos**: Normalização, Herança, Relacionamentos

## 📚 Conceitos Aplicados

### Normalização
- **1FN**: Eliminação de valores multivalorados
- **2FN**: Eliminação de dependências parciais
- **3FN**: Eliminação de dependências transitivas

### Relacionamentos
- **1:1**: Pedido ↔ Pagamento, Pedido ↔ Entrega
- **1:N**: Cliente → Pedidos, Pedido → ItemPedido
- **Herança**: Cliente → ClientePF/ClientePJ

## 🤝 Contribuições

Este projeto foi desenvolvido como parte do bootcamp Database Experience da DIO. Contribuições e sugestões são bem-vindas!

### Como Contribuir
1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👨‍💻 Autor

Desenvolvido por Otávio Guedes durante o **Database Experience** da **[DIO](https://dio.me)**

---

### 📞 Contato

Para dúvidas ou sugestões sobre este projeto, sinta-se à vontade para abrir uma issue ou entrar em contato.

---

**⭐ Se este projeto foi útil para você, não esqueça de dar uma estrela!**
