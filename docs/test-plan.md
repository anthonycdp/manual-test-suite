# Plano de Testes - EcoShop Mini E-commerce

## 1. Informações Gerais

| **Campo** | **Informação** |
|-----------|----------------|
| **Projeto** | EcoShop - Mini E-commerce Sustentável |
| **Versão** | 1.0 |
| **Data de Criação** | 09/07/2025 |
| **Responsável QA** | Equipe de Qualidade |
| **Aprovação** | Product Owner / Tech Lead |

## 2. Objetivos

### 2.1 Objetivo Geral
Garantir a qualidade funcional e usabilidade do sistema EcoShop através de testes manuais abrangentes, validando todas as funcionalidades principais antes do lançamento.

### 2.2 Objetivos Específicos
- Validar fluxos críticos de negócio (cadastro, login, compra)
- Verificar integridade dos dados em todas as transações
- Confirmar usabilidade e experiência do usuário
- Validar segurança básica do sistema
- Garantir compatibilidade com diferentes navegadores

## 3. Escopo dos Testes

### 3.1 Funcionalidades Incluídas
#### 📋 Módulo de Autenticação
- Cadastro de novos usuários
- Login/Logout
- Recuperação de senha
- Validação de campos obrigatórios

#### 🛍️ Módulo de Catálogo
- Listagem de produtos
- Busca e filtros
- Detalhes do produto
- Categorização

#### 🛒 Módulo de Carrinho
- Adicionar/remover produtos
- Alterar quantidades
- Cálculo de totais
- Persistência do carrinho

#### 💳 Módulo de Checkout
- Dados de entrega
- Seleção de forma de pagamento
- Confirmação do pedido
- Geração de pedido

#### 📦 Módulo de Pedidos
- Histórico de pedidos
- Status do pedido
- Cancelamento de pedidos

### 3.2 Funcionalidades Excluídas
- Integração com gateway de pagamento real
- Envio de emails transacionais
- Relatórios administrativos
- APIs externas (CEP, frete)

### 3.3 Tipos de Teste
- ✅ **Funcional**: Validação de todas as funcionalidades
- ✅ **Usabilidade**: Experiência do usuário
- ✅ **Compatibilidade**: Chrome, Firefox, Safari, Edge
- ✅ **Responsividade**: Desktop, tablet, mobile
- ❌ **Performance**: Não incluído nesta versão
- ❌ **Segurança**: Apenas validações básicas
- ❌ **Acessibilidade**: Não incluído nesta versão

## 4. Critérios de Entrada

### 4.1 Pré-requisitos para Início dos Testes
- [ ] Ambiente de teste configurado e estável
- [ ] Versão do sistema deployada no ambiente de teste
- [ ] Massa de dados de teste criada
- [ ] Casos de teste revisados e aprovados
- [ ] Acesso aos ambientes liberado para equipe QA

### 4.2 Documentação Necessária
- [ ] Especificações funcionais
- [ ] Protótipos/mockups das telas
- [ ] Regras de negócio documentadas
- [ ] Arquitetura do sistema (básica)

## 5. Critérios de Saída

### 5.1 Critérios de Aceite
- [ ] 100% dos casos de teste críticos executados com sucesso
- [ ] 95% dos casos de teste de alta prioridade executados com sucesso
- [ ] Máximo de 2 defeitos abertos de severidade alta
- [ ] Nenhum defeito crítico em aberto
- [ ] Fluxos principais funcionando sem bloqueios

### 5.2 Entregáveis
- [ ] Relatório de execução de testes
- [ ] Lista de defeitos encontrados
- [ ] Matriz de rastreabilidade atualizada
- [ ] Recomendações de melhoria
- [ ] Sign-off da equipe QA

## 6. Recursos Necessários

### 6.1 Recursos Humanos
| **Papel** | **Quantidade** | **Responsabilidades** |
|-----------|----------------|----------------------|
| QA Lead | 1 | Coordenação, planejamento, aprovações |
| QA Analyst | 2 | Execução de testes, reporte de bugs |
| Developer | 1 | Suporte para dúvidas técnicas |
| Product Owner | 1 | Validação de critérios de negócio |

### 6.2 Recursos Técnicos
- **Ambiente de Teste**: URL dedicada para testes
- **Navegadores**: Chrome, Firefox, Safari, Edge (últimas versões)
- **Dispositivos**: Desktop, tablet, smartphone
- **Ferramentas**: Planilha para controle, ferramenta de bug tracking

### 6.3 Dados de Teste
- 20 usuários fictícios (diferentes perfis)
- 50 produtos de diferentes categorias
- Cenários de carrinho com diferentes quantidades
- Dados de endereço válidos e inválidos

## 7. Cronograma

| **Fase** | **Atividade** | **Duração** | **Responsável** |
|----------|---------------|-------------|-----------------|
| **Semana 1** | Preparação do ambiente e dados | 2 dias | Dev Team + QA |
| | Revisão e ajuste dos casos de teste | 1 dia | QA Team |
| | Execução - Módulo Autenticação | 2 dias | QA Analyst |
| **Semana 2** | Execução - Módulo Catálogo | 2 dias | QA Analyst |
| | Execução - Módulo Carrinho | 1 dia | QA Analyst |
| | Execução - Módulo Checkout | 2 dias | QA Analyst |
| **Semana 3** | Execução - Módulo Pedidos | 1 dia | QA Analyst |
| | Testes de Compatibilidade | 2 dias | QA Team |
| | Testes de Responsividade | 1 dia | QA Analyst |
| | Regressão completa | 1 dia | QA Team |
| **Semana 4** | Correção de bugs críticos | 2 dias | Dev Team |
| | Re-teste de correções | 1 dia | QA Analyst |
| | Relatórios finais e sign-off | 2 dias | QA Lead |

## 8. Estratégia de Testes

### 8.1 Priorização
1. **Críticos (P1)**: Fluxos que impedem uso básico do sistema
2. **Altos (P2)**: Funcionalidades principais do e-commerce
3. **Médios (P3)**: Funcionalidades complementares
4. **Baixos (P4)**: Melhorias de usabilidade

### 8.2 Abordagem de Execução
- **Primeira Rodada**: Execução de todos os casos críticos e altos
- **Segunda Rodada**: Execução de casos médios e baixos
- **Terceira Rodada**: Regressão completa após correções

### 8.3 Gestão de Defeitos
- **Crítico**: Sistema inutilizável, dados corrompidos
- **Alto**: Funcionalidade principal não funciona
- **Médio**: Funcionalidade secundária com problemas
- **Baixo**: Problemas menores de usabilidade

## 9. Riscos e Mitigações

| **Risco** | **Probabilidade** | **Impacto** | **Mitigação** |
|-----------|-------------------|-------------|---------------|
| Ambiente instável | Média | Alto | Monitoramento contínuo, backup de ambiente |
| Mudanças de escopo | Alta | Médio | Processo formal de change request |
| Recursos insuficientes | Baixa | Alto | Planejamento antecipado, recursos backup |
| Dados de teste inadequados | Média | Médio | Validação prévia dos dados, scripts automatizados |

## 10. Comunicação

### 10.1 Reuniões
- **Daily Standup**: Status diário de execução (15 min)
- **Weekly Status**: Reunião semanal de progresso (30 min)
- **Bug Triage**: Reunião para priorização de bugs (45 min)

### 10.2 Relatórios
- **Diário**: Status dashboard atualizado
- **Semanal**: Relatório de progresso executivo
- **Final**: Relatório completo de qualidade

## 11. Aprovações

| **Papel** | **Nome** | **Data** | **Assinatura** |
|-----------|----------|----------|----------------|
| QA Lead | [Nome] | [Data] | [Assinatura] |
| Product Owner | [Nome] | [Data] | [Assinatura] |
| Tech Lead | [Nome] | [Data] | [Assinatura] |

---

*Documento controlado - Versão 1.0 - Todas as alterações devem ser aprovadas pelo QA Lead*