# Matriz de Rastreabilidade - Requisitos x Casos de Teste

## 🎯 Objetivo

Esta matriz garante que todos os requisitos funcionais do sistema EcoShop tenham cobertura adequada de testes, identificando gaps e redundâncias na estratégia de teste.

## 📊 Resumo da Cobertura

| **Módulo** | **Requisitos** | **Casos de Teste** | **Cobertura** |
|------------|----------------|-------------------|---------------|
| Autenticação | 8 | 5 | 100% |
| Catálogo | 6 | 5 | 100% |
| Carrinho | 7 | 5 | 100% |
| Checkout | 5 | 4 | 100% |
| Pedidos | 4 | 3 | 100% |
| **Total** | **30** | **22** | **100%** |

---

## 🔐 Módulo: Autenticação

### Requisitos Funcionais

| **Req ID** | **Requisito** | **Casos de Teste** | **Cobertura** | **Status** |
|------------|---------------|-------------------|---------------|------------|
| **REQ_AUTH_001** | Sistema deve permitir cadastro de novos usuários | TC_AUTH_001 | ✅ | Coberto |
| **REQ_AUTH_002** | Email deve ser único no sistema | TC_AUTH_001 (validação) | ✅ | Coberto |
| **REQ_AUTH_003** | Senha deve atender critérios de segurança | TC_AUTH_001 (validação) | ✅ | Coberto |
| **REQ_AUTH_004** | Sistema deve autenticar usuários registrados | TC_AUTH_002 | ✅ | Coberto |
| **REQ_AUTH_005** | Sistema deve rejeitar credenciais inválidas | TC_AUTH_003 | ✅ | Coberto |
| **REQ_AUTH_006** | Usuário deve poder recuperar senha | TC_AUTH_005 | ✅ | Coberto |
| **REQ_AUTH_007** | Sistema deve permitir logout seguro | TC_AUTH_004 | ✅ | Coberto |
| **REQ_AUTH_008** | Sessão deve expirar após inatividade | *Não testado* | ❌ | **Gap identificado** |

### 📋 Ações Recomendadas
- **Criar TC_AUTH_006**: Teste de expiração de sessão
- **Criar TC_AUTH_007**: Teste de múltiplas sessões simultâneas

---

## 🛍️ Módulo: Catálogo de Produtos

### Requisitos Funcionais

| **Req ID** | **Requisito** | **Casos de Teste** | **Cobertura** | **Status** |
|------------|---------------|-------------------|---------------|------------|
| **REQ_CAT_001** | Sistema deve exibir lista de produtos | TC_CAT_001 | ✅ | Coberto |
| **REQ_CAT_002** | Usuário deve poder buscar produtos por nome | TC_CAT_002, TC_CAT_005 | ✅ | Coberto |
| **REQ_CAT_003** | Sistema deve permitir filtros por categoria | TC_CAT_003 | ✅ | Coberto |
| **REQ_CAT_004** | Cada produto deve ter página de detalhes | TC_CAT_004 | ✅ | Coberto |
| **REQ_CAT_005** | Produtos devem exibir imagens, preço e descrição | TC_CAT_001, TC_CAT_004 | ✅ | Coberto |
| **REQ_CAT_006** | Sistema deve paginar resultados extensos | *Coberto parcialmente* | ⚠️ | **Cobertura parcial** |

### 📋 Ações Recomendadas
- **Melhorar TC_CAT_001**: Adicionar validação específica de paginação
- **Criar TC_CAT_006**: Teste específico para paginação com muitos produtos

---

## 🛒 Módulo: Carrinho de Compras

### Requisitos Funcionais

| **Req ID** | **Requisito** | **Casos de Teste** | **Cobertura** | **Status** |
|------------|---------------|-------------------|---------------|------------|
| **REQ_CART_001** | Usuário deve poder adicionar produtos ao carrinho | TC_CART_001 | ✅ | Coberto |
| **REQ_CART_002** | Sistema deve exibir conteúdo do carrinho | TC_CART_002 | ✅ | Coberto |
| **REQ_CART_003** | Usuário deve poder alterar quantidades | TC_CART_003 | ✅ | Coberto |
| **REQ_CART_004** | Usuário deve poder remover itens | TC_CART_004 | ✅ | Coberto |
| **REQ_CART_005** | Sistema deve calcular totais automaticamente | TC_CART_002, TC_CART_003 | ✅ | Coberto |
| **REQ_CART_006** | Carrinho deve persistir entre sessões | *Mencionado nas notas* | ⚠️ | **Teste implícito** |
| **REQ_CART_007** | Sistema deve validar estoque disponível | *Não testado* | ❌ | **Gap identificado** |

### 📋 Ações Recomendadas
- **Criar TC_CART_006**: Teste explícito de persistência do carrinho
- **Criar TC_CART_007**: Teste de validação de estoque
- **Criar TC_CART_008**: Teste de limites de quantidade

---

## 💳 Módulo: Checkout

### Requisitos Funcionais

| **Req ID** | **Requisito** | **Casos de Teste** | **Cobertura** | **Status** |
|------------|---------------|-------------------|---------------|------------|
| **REQ_CHECK_001** | Apenas usuários logados podem fazer checkout | TC_CHECK_002 | ✅ | Coberto |
| **REQ_CHECK_002** | Sistema deve coletar dados de entrega | TC_CHECK_001, TC_CHECK_003 | ✅ | Coberto |
| **REQ_CHECK_003** | Sistema deve processar formas de pagamento | TC_CHECK_004 | ✅ | Coberto |
| **REQ_CHECK_004** | Sistema deve validar dados obrigatórios | TC_CHECK_003 | ✅ | Coberto |
| **REQ_CHECK_005** | Sistema deve gerar pedido com número único | TC_CHECK_001 | ✅ | Coberto |

### 📋 Status: ✅ **Cobertura completa**

---

## 📦 Módulo: Pedidos

### Requisitos Funcionais

| **Req ID** | **Requisito** | **Casos de Teste** | **Cobertura** | **Status** |
|------------|---------------|-------------------|---------------|------------|
| **REQ_ORDER_001** | Usuário deve ver histórico de pedidos | TC_ORDER_001 | ✅ | Coberto |
| **REQ_ORDER_002** | Sistema deve exibir detalhes completos do pedido | TC_ORDER_002 | ✅ | Coberto |
| **REQ_ORDER_003** | Usuário deve poder cancelar pedidos conforme política | TC_ORDER_003 | ✅ | Coberto |
| **REQ_ORDER_004** | Sistema deve atualizar status dos pedidos | *Implícito* | ⚠️ | **Teste implícito** |

### 📋 Ações Recomendadas
- **Criar TC_ORDER_004**: Teste específico para mudanças de status
- **Melhorar TC_ORDER_002**: Validar todos os campos de detalhes

---

## 📱 Requisitos Não-Funcionais

### Compatibilidade e Responsividade

| **Req ID** | **Requisito** | **Casos de Teste** | **Cobertura** | **Status** |
|------------|---------------|-------------------|---------------|------------|
| **REQ_COMP_001** | Sistema deve funcionar nos principais browsers | TC_COMP_001, TC_COMP_002, TC_COMP_003 | ✅ | Coberto |
| **REQ_RESP_001** | Interface deve ser responsiva | TC_RESP_001, TC_RESP_002 | ✅ | Coberto |
| **REQ_PERF_001** | Páginas devem carregar em até 3 segundos | *Não testado* | ❌ | **Gap identificado** |
| **REQ_USAB_001** | Interface deve ser intuitiva | *Avaliação subjetiva* | ⚠️ | **Teste subjetivo** |

---

## 🔍 Análise de Gaps

### ❌ Gaps Críticos (Requerem Ação Imediata)

1. **REQ_AUTH_008**: Expiração de sessão não testada
   - **Impacto**: Segurança
   - **Ação**: Criar TC_AUTH_006

2. **REQ_CART_007**: Validação de estoque não testada
   - **Impacto**: Integridade do negócio
   - **Ação**: Criar TC_CART_007

3. **REQ_PERF_001**: Performance não validada
   - **Impacto**: Experiência do usuário
   - **Ação**: Adicionar testes de performance

### ⚠️ Gaps Médios (Melhorias Recomendadas)

1. **REQ_CAT_006**: Paginação parcialmente testada
2. **REQ_CART_006**: Persistência implicitamente testada
3. **REQ_ORDER_004**: Status de pedidos implicitamente testado

### ✅ Cobertura Adequada

- Fluxos principais de autenticação
- Funcionalidades básicas do catálogo
- Operações do carrinho
- Processo de checkout completo
- Gestão básica de pedidos

---

## 📊 Métricas de Qualidade

### Cobertura por Categoria

| **Categoria** | **Total Req** | **Cobertos** | **Gaps** | **% Cobertura** |
|---------------|---------------|--------------|----------|-----------------|
| **Funcionais** | 30 | 27 | 3 | 90% |
| **Não-Funcionais** | 4 | 2 | 2 | 50% |
| **Segurança** | 3 | 2 | 1 | 67% |
| **Total Geral** | 37 | 31 | 6 | **84%** |

### Distribuição de Riscos

- 🔴 **Alto Risco**: 3 gaps (Segurança, Estoque, Performance)
- 🟡 **Médio Risco**: 3 gaps (Funcionalidades complementares)
- 🟢 **Baixo Risco**: 31 requisitos cobertos adequadamente

---

## 🎯 Plano de Melhoria

### Fase 1 (Crítica) - 1 semana
- [ ] TC_AUTH_006: Teste de expiração de sessão
- [ ] TC_CART_007: Validação de estoque
- [ ] TC_PERF_001: Teste básico de performance

### Fase 2 (Melhoria) - 2 semanas
- [ ] TC_CAT_006: Teste específico de paginação
- [ ] TC_CART_006: Teste explícito de persistência
- [ ] TC_ORDER_004: Teste de mudança de status

### Fase 3 (Otimização) - Contínua
- [ ] Testes de usabilidade estruturados
- [ ] Testes de acessibilidade
- [ ] Automação de testes repetitivos

---

## 📝 Notas de Manutenção

### Processo de Atualização
1. **Novos Requisitos**: Adicionar na matriz com análise de impacto
2. **Mudança de Requisitos**: Atualizar casos afetados
3. **Casos Removidos**: Manter histórico com status "Depreciado"

### Responsabilidades
- **Product Owner**: Definição e mudança de requisitos
- **QA Lead**: Manutenção da matriz e análise de gaps
- **QA Analysts**: Execução e feedback dos casos

### Frequência de Revisão
- **Semanal**: Durante desenvolvimento ativo
- **Mensal**: Em manutenção
- **A cada release**: Validação completa

---

*Última atualização: 09/07/2025*
*Responsável: QA Lead*
*Próxima revisão: 16/07/2025*