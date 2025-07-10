# Checklist de Regressão - EcoShop Mini E-commerce

## 🎯 Objetivo

Este checklist garante que as funcionalidades críticas do sistema permaneçam funcionais após cada nova entrega, correção de bugs ou atualização. Execute este checklist completo antes de qualquer release para produção.

## ⏱️ Tempo Estimado de Execução

**Total**: 2-3 horas para execução completa
- Smoke Test: 30 minutos
- Regressão Completa: 2-3 horas

## 🚀 Smoke Test (Funcionalidades Críticas - 30 min)

Execute primeiro este smoke test. Se algum item falhar, **PARE** e corrija antes de continuar.

### ✅ Checklist Crítico

| **ID** | **Funcionalidade** | **Status** | **Observações** |
|--------|-------------------|------------|----------------|
| **SM_01** | Site carrega sem erros | ⬜ | URL principal acessível |
| **SM_02** | Cadastro de novo usuário | ⬜ | Fluxo completo funcionando |
| **SM_03** | Login com credenciais válidas | ⬜ | Autenticação funcionando |
| **SM_04** | Adicionar produto ao carrinho | ⬜ | Carrinho operacional |
| **SM_05** | Finalizar compra completa | ⬜ | Checkout end-to-end |
| **SM_06** | Logout do sistema | ⬜ | Sessão encerrada corretamente |

**Critério de Parada**: Se qualquer item do Smoke Test falhar, pare a regressão e abra bug crítico.

---

## 🔐 Módulo: Autenticação

### 📋 Funcionalidades a Testar

| **ID** | **Funcionalidade** | **Verificar** | **Status** | **Bug ID** | **Notas** |
|--------|-------------------|---------------|------------|------------|-----------|
| **AUTH_01** | Cadastro com dados válidos | Usuário criado, email confirmação | ⬜ | | |
| **AUTH_02** | Cadastro com email duplicado | Erro: "Email já existe" | ⬜ | | |
| **AUTH_03** | Validação de senha fraca | Erro: critérios de senha | ⬜ | | |
| **AUTH_04** | Login com credenciais corretas | Acesso liberado, nome visível | ⬜ | | |
| **AUTH_05** | Login com credenciais incorretas | Erro: "Email ou senha incorretos" | ⬜ | | |
| **AUTH_06** | Recuperação de senha | Mensagem de confirmação | ⬜ | | |
| **AUTH_07** | Logout do sistema | Sessão encerrada, redirect | ⬜ | | |
| **AUTH_08** | Acesso sem autenticação | Redirect para login quando necessário | ⬜ | | |

### ✅ Critérios de Aceite
- [ ] Todos os fluxos de autenticação funcionando
- [ ] Validações de segurança ativas
- [ ] Mensagens de erro claras
- [ ] Sessões gerenciadas corretamente

---

## 🛍️ Módulo: Catálogo de Produtos

### 📋 Funcionalidades a Testar

| **ID** | **Funcionalidade** | **Verificar** | **Status** | **Bug ID** | **Notas** |
|--------|-------------------|---------------|------------|------------|-----------|
| **CAT_01** | Listagem de produtos | Produtos carregando, imagens visíveis | ⬜ | | |
| **CAT_02** | Busca por nome | Resultados relevantes exibidos | ⬜ | | |
| **CAT_03** | Busca sem resultados | Mensagem "Nenhum produto encontrado" | ⬜ | | |
| **CAT_04** | Filtro por categoria | Produtos filtrados corretamente | ⬜ | | |
| **CAT_05** | Detalhes do produto | Informações completas exibidas | ⬜ | | |
| **CAT_06** | Imagens do produto | Carregamento e zoom funcionando | ⬜ | | |
| **CAT_07** | Produtos em destaque | Seção especial funcionando | ⬜ | | |
| **CAT_08** | Paginação da lista | Navegação entre páginas | ⬜ | | |

### ✅ Critérios de Aceite
- [ ] Todos os produtos visíveis
- [ ] Busca e filtros operacionais
- [ ] Carregamento de imagens estável
- [ ] Performance aceitável na listagem

---

## 🛒 Módulo: Carrinho de Compras

### 📋 Funcionalidades a Testar

| **ID** | **Funcionalidade** | **Verificar** | **Status** | **Bug ID** | **Notas** |
|--------|-------------------|---------------|------------|------------|-----------|
| **CART_01** | Adicionar produto | Produto no carrinho, contador atualizado | ⬜ | | |
| **CART_02** | Alterar quantidade | Quantidade e preços recalculados | ⬜ | | |
| **CART_03** | Remover produto | Produto removido, total atualizado | ⬜ | | |
| **CART_04** | Carrinho vazio | Mensagem apropriada exibida | ⬜ | | |
| **CART_05** | Persistência do carrinho | Carrinho mantido entre sessões | ⬜ | | |
| **CART_06** | Cálculo de totais | Subtotal e total corretos | ⬜ | | |
| **CART_07** | Limite de estoque | Validação de quantidade disponível | ⬜ | | |
| **CART_08** | Produto indisponível | Tratamento de produto fora de linha | ⬜ | | |

### ✅ Critérios de Aceite
- [ ] Operações básicas funcionando
- [ ] Cálculos matemáticos corretos
- [ ] Validações de negócio ativas
- [ ] Experiência do usuário fluida

---

## 💳 Módulo: Checkout

### 📋 Funcionalidades a Testar

| **ID** | **Funcionalidade** | **Verificar** | **Status** | **Bug ID** | **Notas** |
|--------|-------------------|---------------|------------|------------|-----------|
| **CHECK_01** | Acesso ao checkout | Página carregada com produtos | ⬜ | | |
| **CHECK_02** | Dados de entrega | Formulário de endereço funcionando | ⬜ | | |
| **CHECK_03** | Validação de CEP | Validação e preenchimento automático | ⬜ | | |
| **CHECK_04** | Formas de pagamento | Opções disponíveis e selecionáveis | ⬜ | | |
| **CHECK_05** | Dados do cartão | Validação de campos do cartão | ⬜ | | |
| **CHECK_06** | Revisão do pedido | Resumo completo antes confirmação | ⬜ | | |
| **CHECK_07** | Finalização | Pedido criado com número | ⬜ | | |
| **CHECK_08** | Página de confirmação | Detalhes do pedido exibidos | ⬜ | | |

### ✅ Critérios de Aceite
- [ ] Fluxo completo sem interrupções
- [ ] Validações de dados funcionando
- [ ] Pedido gerado corretamente
- [ ] Página de confirmação informativa

---

## 📦 Módulo: Gestão de Pedidos

### 📋 Funcionalidades a Testar

| **ID** | **Funcionalidade** | **Verificar** | **Status** | **Bug ID** | **Notas** |
|--------|-------------------|---------------|------------|------------|-----------|
| **ORDER_01** | Lista de pedidos | Histórico visível na conta | ⬜ | | |
| **ORDER_02** | Detalhes do pedido | Informações completas acessíveis | ⬜ | | |
| **ORDER_03** | Status do pedido | Estados atualizados corretamente | ⬜ | | |
| **ORDER_04** | Cancelamento | Pedidos canceláveis conforme regra | ⬜ | | |
| **ORDER_05** | Busca de pedidos | Localização por número/data | ⬜ | | |
| **ORDER_06** | Download de comprovante | PDF ou recibo acessível | ⬜ | | |

### ✅ Critérios de Aceite
- [ ] Histórico completo e acessível
- [ ] Status atualizados em tempo real
- [ ] Políticas de cancelamento respeitadas

---

## 📱 Compatibilidade e Responsividade

### 📋 Dispositivos a Testar

| **ID** | **Dispositivo/Browser** | **Funcionalidades Principais** | **Status** | **Bug ID** | **Notas** |
|--------|------------------------|--------------------------------|------------|------------|-----------|
| **COMP_01** | Chrome Desktop | Fluxo completo de compra | ⬜ | | |
| **COMP_02** | Firefox Desktop | Fluxo completo de compra | ⬜ | | |
| **COMP_03** | Safari Desktop | Fluxo completo de compra | ⬜ | | |
| **RESP_01** | Tablet (768-1024px) | Layout e usabilidade | ⬜ | | |
| **RESP_02** | Mobile (<768px) | Menu mobile, carrinho | ⬜ | | |
| **RESP_03** | Mobile Landscape | Rotação de tela | ⬜ | | |

### ✅ Critérios de Aceite
- [ ] Compatibilidade com principais browsers
- [ ] Layout responsivo funcionando
- [ ] Usabilidade mantida em todos os dispositivos

---

## 🔒 Segurança Básica

### 📋 Pontos de Verificação

| **ID** | **Item de Segurança** | **Verificar** | **Status** | **Bug ID** | **Notas** |
|--------|----------------------|---------------|------------|------------|-----------|
| **SEC_01** | HTTPS ativo | URL com certificado válido | ⬜ | | |
| **SEC_02** | Validação de entrada | Campos protegidos contra XSS | ⬜ | | |
| **SEC_03** | Autenticação | Sessões seguras e expiração | ⬜ | | |
| **SEC_04** | Dados sensíveis | Senhas mascaradas, dados criptografados | ⬜ | | |
| **SEC_05** | Erro de sistema | Mensagens não revelam detalhes técnicos | ⬜ | | |

### ✅ Critérios de Aceite
- [ ] Certificado SSL válido
- [ ] Validações de entrada ativas
- [ ] Dados sensíveis protegidos

---

## 📊 Critérios de Aprovação Final

### ✅ Checklist de Aprovação

- [ ] **100%** dos itens de Smoke Test aprovados
- [ ] **95%** dos itens de regressão aprovados
- [ ] **Zero** bugs críticos em aberto
- [ ] **Máximo 2** bugs de alta severidade em aberto
- [ ] Compatibilidade testada nos principais browsers
- [ ] Responsividade validada

### 📈 Métricas de Qualidade

| **Métrica** | **Meta** | **Atual** | **Status** |
|-------------|----------|-----------|------------|
| Taxa de Sucesso | ≥95% | ___% | ⬜ |
| Bugs Críticos | 0 | ___ | ⬜ |
| Bugs Altos | ≤2 | ___ | ⬜ |
| Cobertura de Testes | 100% | ___% | ⬜ |

### 🚦 Decisão de Release

**✅ APROVADO PARA RELEASE**
- Todos os critérios atendidos
- Qualidade dentro dos padrões
- Riscos mitigados

**❌ REPROVADO PARA RELEASE**
- Critérios não atendidos
- Bugs críticos pendentes
- Riscos não aceitáveis

**⚠️ APROVADO COM RESSALVAS**
- Pequenos desvios documentados
- Plano de correção pós-release
- Monitoramento intensivo

---

## 📝 Instruções de Execução

### Antes de Iniciar
1. Ambiente de teste disponível
2. Dados de teste preparados
3. Browsers atualizados
4. Acesso às ferramentas necessárias

### Durante a Execução
1. Execute na ordem sugerida
2. Marque status após cada verificação
3. Registre bugs imediatamente
4. Documente observações importantes

### Após a Execução
1. Compile relatório de status
2. Calcule métricas de qualidade
3. Tome decisão de release
4. Comunique resultados à equipe

---

**Data da Execução**: ___________
**Executado por**: ___________
**Ambiente**: ___________
**Versão Testada**: ___________
**Decisão Final**: ___________

*Documento controlado - Versão 1.0 - Todas as alterações devem ser aprovadas pelo QA Lead*