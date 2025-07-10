# Dados de Teste - EcoShop Mini E-commerce

## 🎯 Objetivo

Este arquivo contém todos os dados necessários para execução dos casos de teste, garantindo consistência e facilitando a preparação dos ambientes de teste.

---

## 👥 Usuários de Teste

### Usuários Válidos

| **ID** | **Nome** | **Email** | **Senha** | **Uso** |
|--------|----------|-----------|-----------|---------|
| **USER_01** | João Silva | joao.silva@email.com | MinhaSenh@123 | Testes básicos |
| **USER_02** | Maria Santos | maria.santos@teste.com | Segura#456 | Fluxo completo |
| **USER_03** | Pedro Costa | pedro.costa@example.org | Forte$789 | Múltiplos pedidos |
| **USER_04** | Ana Oliveira | ana.oliveira@demo.net | Complex!012 | Casos específicos |
| **USER_05** | Carlos Lima | carlos.lima@test.br | Valid&345 | Testes de carrinho |

### Usuários para Cenários Específicos

| **Cenário** | **Email** | **Senha** | **Descrição** |
|-------------|-----------|-----------|---------------|
| **Primeiro acesso** | novo.usuario@email.com | Primeira#123 | Usuário sem histórico |
| **Usuário ativo** | ativo@email.com | Ativo@456 | Com pedidos anteriores |
| **Carrinho abandonado** | abandonado@email.com | Abandon$789 | Carrinho com produtos |

---

## 🛍️ Produtos de Teste

### Produtos Principais

| **ID** | **Nome** | **Categoria** | **Preço** | **Estoque** | **Descrição** |
|--------|----------|---------------|-----------|-------------|---------------|
| **PROD_01** | Camiseta Orgânica | Roupas | R$ 49,90 | 50 | Camiseta 100% algodão orgânico |
| **PROD_02** | Garrafa Reutilizável | Acessórios | R$ 29,90 | 100 | Garrafa de aço inoxidável 500ml |
| **PROD_03** | Sabonete Natural | Higiene | R$ 12,50 | 200 | Sabonete artesanal de lavanda |
| **PROD_04** | Mochila Eco | Acessórios | R$ 89,90 | 25 | Mochila feita com material reciclado |
| **PROD_05** | Shampoo Sólido | Higiene | R$ 18,90 | 80 | Shampoo sólido sem sulfato |

### Produtos para Cenários Específicos

| **Cenário** | **Produto** | **Preço** | **Estoque** | **Observação** |
|-------------|-------------|-----------|-------------|----------------|
| **Produto em falta** | Sapato Vegano | R$ 159,90 | 0 | Para teste de indisponibilidade |
| **Produto promocional** | Kit Sustentável | R$ 79,90 | 10 | Produto em oferta |
| **Produto premium** | Jaqueta Reciclada | R$ 299,90 | 5 | Valor alto para testes |
| **Produto pesquisável** | Copo Bambu | R$ 15,90 | 75 | Para testes de busca |

---

## 📦 Dados de Carrinho

### Cenários de Carrinho

| **Cenário** | **Produtos** | **Quantidades** | **Valor Total** |
|-------------|--------------|-----------------|-----------------|
| **Carrinho simples** | PROD_01 | 1 | R$ 49,90 |
| **Carrinho múltiplo** | PROD_01, PROD_02 | 2, 1 | R$ 129,70 |
| **Carrinho completo** | PROD_01, PROD_02, PROD_03 | 1, 2, 3 | R$ 147,20 |
| **Carrinho grande** | PROD_01, PROD_04, PROD_05 | 3, 1, 2 | R$ 277,50 |

### Cálculos de Teste

```
Carrinho Múltiplo:
- Camiseta Orgânica: R$ 49,90 x 2 = R$ 99,80
- Garrafa Reutilizável: R$ 29,90 x 1 = R$ 29,90
- Subtotal: R$ 129,70
- Frete: R$ 0,00 (Grátis)
- Total: R$ 129,70
```

---

## 🏠 Endereços de Entrega

### Endereços Válidos

| **ID** | **Nome** | **CEP** | **Endereço** | **Cidade** | **Estado** |
|--------|----------|---------|--------------|-----------|------------|
| **END_01** | João Silva | 01310-100 | Av. Paulista, 123 | São Paulo | SP |
| **END_02** | Maria Santos | 22071-900 | Rua das Flores, 456 | Rio de Janeiro | RJ |
| **END_03** | Pedro Costa | 30112-000 | Rua da Paz, 789 | Belo Horizonte | MG |
| **END_04** | Ana Oliveira | 80010-000 | Av. Central, 321 | Curitiba | PR |
| **END_05** | Carlos Lima | 40070-110 | Rua do Comércio, 654 | Salvador | BA |

### Endereços para Cenários Específicos

| **Cenário** | **CEP** | **Observação** |
|-------------|---------|----------------|
| **CEP inválido** | 00000-000 | Para teste de validação |
| **CEP inexistente** | 99999-999 | Para teste de erro |
| **Formato incorreto** | 12345678 | Sem máscara |
| **Caracteres inválidos** | ABCDE-FGH | Com letras |

---

## 💳 Dados de Pagamento

### Cartões de Teste

| **Bandeira** | **Número** | **Validade** | **CVV** | **Nome** | **Resultado** |
|--------------|------------|--------------|---------|----------|---------------|
| **Visa** | 4111 1111 1111 1111 | 12/28 | 123 | João Silva | Aprovado |
| **Mastercard** | 5555 5555 5555 4444 | 10/27 | 456 | Maria Santos | Aprovado |
| **Elo** | 6362 9700 0000 0005 | 06/29 | 789 | Pedro Costa | Aprovado |
| **Visa (Recusado)** | 4000 0000 0000 0002 | 12/26 | 321 | Ana Oliveira | Recusado |

### Cenários de Pagamento

| **Cenário** | **Tipo** | **Dados** | **Resultado Esperado** |
|-------------|----------|-----------|------------------------|
| **Pagamento aprovado** | Cartão Visa | 4111 1111 1111 1111 | Pedido confirmado |
| **Cartão expirado** | Cartão vencido | 01/20 | Erro de validação |
| **CVV inválido** | CVV incorreto | 000 | Erro de segurança |
| **Cartão bloqueado** | Cartão recusado | 4000 0000 0000 0002 | Transação negada |

---

## 🔍 Dados de Busca

### Termos de Busca Válidos

| **Termo** | **Resultados Esperados** | **Quantidade** |
|-----------|--------------------------|----------------|
| **"camiseta"** | Produtos de roupas | 3-5 itens |
| **"garrafa"** | Acessórios para bebidas | 2-3 itens |
| **"sustentável"** | Produtos eco-friendly | 5+ itens |
| **"orgânico"** | Produtos naturais | 4-6 itens |
| **"R$ 29"** | Busca por preço | 1-2 itens |

### Termos de Busca Inválidos

| **Termo** | **Resultado Esperado** |
|-----------|------------------------|
| **"xyzabc123"** | Nenhum resultado encontrado |
| **"@#$%"** | Nenhum resultado encontrado |
| **""** (vazio) | Todos os produtos |
| **"   "** (espaços) | Todos os produtos ou erro |

---

## 📊 Filtros de Teste

### Filtros por Categoria

| **Categoria** | **Produtos Esperados** | **Quantidade** |
|---------------|-------------------------|----------------|
| **Roupas** | Camisetas, calças, casacos | 8-12 itens |
| **Acessórios** | Garrafas, mochilas, bolsas | 6-10 itens |
| **Higiene** | Sabonetes, shampoos | 4-8 itens |
| **Todos** | Sem filtro aplicado | 20+ itens |

### Filtros por Preço

| **Faixa** | **Critério** | **Produtos Esperados** |
|-----------|--------------|------------------------|
| **Até R$ 20** | ≤ R$ 20,00 | Produtos básicos |
| **R$ 20 - R$ 50** | R$ 20,01 - R$ 50,00 | Produtos médios |
| **R$ 50 - R$ 100** | R$ 50,01 - R$ 100,00 | Produtos premium |
| **Acima de R$ 100** | > R$ 100,00 | Produtos especiais |

---

## 🚫 Dados Inválidos para Testes Negativos

### Dados de Cadastro Inválidos

| **Campo** | **Valor Inválido** | **Erro Esperado** |
|-----------|-------------------|-------------------|
| **Email** | email_sem_arroba | "Email inválido" |
| **Email** | @dominio.com | "Email inválido" |
| **Senha** | 123 | "Senha muito fraca" |
| **Senha** | senhasemcaractereespecial | "Senha deve conter símbolos" |
| **Nome** | "" | "Nome é obrigatório" |

### Dados de Checkout Inválidos

| **Campo** | **Valor Inválido** | **Erro Esperado** |
|-----------|-------------------|-------------------|
| **CEP** | 12345 | "CEP deve ter 8 dígitos" |
| **Número cartão** | 1234 | "Número inválido" |
| **CVV** | 12 | "CVV deve ter 3 dígitos" |
| **Validade** | 13/25 | "Mês inválido" |

---

## 🎭 Personas de Teste

### Persona 1: Usuário Novo
- **Nome**: João Silva
- **Email**: joao.silva@email.com
- **Comportamento**: Primeiro acesso, explora catálogo
- **Jornada**: Cadastro → Busca → Carrinho → Checkout

### Persona 2: Cliente Frequente
- **Nome**: Maria Santos
- **Email**: maria.santos@teste.com
- **Comportamento**: Conhece sistema, compra rápida
- **Jornada**: Login → Produto específico → Checkout

### Persona 3: Usuário Indeciso
- **Nome**: Pedro Costa
- **Email**: pedro.costa@example.org
- **Comportamento**: Adiciona/remove produtos, abandona carrinho
- **Jornada**: Busca → Carrinho → Abandono → Retorno

---

## 📱 Dados para Testes Mobile

### Resoluções de Teste

| **Dispositivo** | **Resolução** | **Orientação** |
|-----------------|---------------|----------------|
| **iPhone 12** | 390x844 | Retrato/Paisagem |
| **Samsung Galaxy** | 360x800 | Retrato/Paisagem |
| **iPad** | 768x1024 | Retrato/Paisagem |
| **Tablet Android** | 800x1280 | Retrato/Paisagem |

### Cenários Mobile Específicos

- **Zoom**: Testar com zoom 150%, 200%
- **Orientação**: Rotação durante uso
- **Touch**: Gestos de toque e deslize
- **Teclado**: Entrada de dados no mobile

---

## 🔧 Scripts de Preparação

### SQL para Ambiente de Teste

```sql
-- Usuários de teste
INSERT INTO users (name, email, password) VALUES 
('João Silva', 'joao.silva@email.com', 'hashed_password_1'),
('Maria Santos', 'maria.santos@teste.com', 'hashed_password_2');

-- Produtos de teste
INSERT INTO products (name, category, price, stock) VALUES 
('Camiseta Orgânica', 'Roupas', 49.90, 50),
('Garrafa Reutilizável', 'Acessórios', 29.90, 100);
```

### JSON para APIs

```json
{
  "user": {
    "name": "João Silva",
    "email": "joao.silva@email.com",
    "password": "MinhaSenh@123"
  },
  "product": {
    "id": 1,
    "quantity": 2
  }
}
```

---

## 📋 Checklist de Preparação

### Antes dos Testes
- [ ] Usuários de teste criados
- [ ] Produtos cadastrados
- [ ] Estoque configurado
- [ ] Categorias definidas
- [ ] Endereços válidos preparados

### Durante os Testes
- [ ] Dados atualizados conforme necessário
- [ ] Carrinho limpo entre testes
- [ ] Sessões encerradas adequadamente
- [ ] Cache limpo quando necessário

### Após os Testes
- [ ] Dados de teste removidos (se necessário)
- [ ] Relatórios de uso dos dados
- [ ] Atualizações necessárias documentadas

---

*Última atualização: 09/07/2025*
*Responsável: QA Team*