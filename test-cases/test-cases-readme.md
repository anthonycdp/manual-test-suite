# Casos de Teste - EcoShop Mini E-commerce

## 📋 Informações Importantes

**Arquivo Principal**: `test-cases.csv` - Importe este arquivo no Excel ou Google Sheets para melhor visualização e gestão.

**Visualização Legível**: `test-cases-readable.md` - Versão formatada em Markdown para fácil leitura dos casos de teste.

**Total de Casos**: 25 casos de teste cobrindo todos os módulos principais.

## 🎯 Distribuição por Módulo

| **Módulo** | **Quantidade** | **Casos Críticos** |
|------------|----------------|---------------------|
| Autenticação | 5 | 2 |
| Catálogo | 5 | 2 |
| Carrinho | 5 | 3 |
| Checkout | 4 | 2 |
| Pedidos | 3 | 0 |
| Responsividade | 2 | 0 |
| Compatibilidade | 3 | 1 |

## 📊 Distribuição por Prioridade

- **P1 (Crítico/Alto)**: 15 casos - Fluxos principais que impedem uso do sistema
- **P2 (Médio)**: 8 casos - Funcionalidades importantes mas não bloqueantes
- **P3 (Baixo)**: 2 casos - Melhorias de usabilidade

## 🚨 Distribuição por Severidade

- **Critical**: 1 caso - Checkout completo
- **High**: 12 casos - Funcionalidades principais
- **Medium**: 10 casos - Funcionalidades secundárias
- **Low**: 2 casos - Usabilidade

## 🔍 Como Usar

### 1. **Importação para Excel/Sheets**
```
1. Abra Excel ou Google Sheets
2. Importe o arquivo test-cases.csv
3. Configure as colunas para melhor visualização
4. Use filtros para organizar por módulo/prioridade
```

### 2. **Estrutura dos Casos de Teste**
Cada caso contém:
- **Test_ID**: Identificador único
- **Module**: Módulo do sistema
- **Test_Title**: Título descritivo
- **Priority**: P1, P2, P3
- **Severity**: Critical, High, Medium, Low
- **Preconditions**: Condições necessárias
- **Test_Steps**: Passos numerados para execução
- **Expected_Result**: Resultado esperado
- **Test_Data**: Dados específicos para o teste
- **Notes**: Observações adicionais

### 3. **Execução Recomendada**

#### **Primeira Rodada (P1 - Críticos)**
```
TC_AUTH_001, TC_AUTH_002, TC_AUTH_004
TC_CAT_001, TC_CAT_002, TC_CAT_004
TC_CART_001, TC_CART_002, TC_CART_003
TC_CHECK_001, TC_CHECK_004
TC_COMP_001
```

#### **Segunda Rodada (P2 - Médios)**
```
TC_AUTH_003, TC_AUTH_005
TC_CAT_003, TC_CAT_005
TC_CART_004
TC_CHECK_002, TC_CHECK_003
TC_ORDER_001, TC_ORDER_002
TC_RESP_001, TC_RESP_002
TC_COMP_002, TC_COMP_003
```

#### **Terceira Rodada (P3 - Baixos)**
```
TC_CART_005
TC_ORDER_003
```

## 📝 Controle de Execução

Adicione estas colunas ao planilha para controle:

| **Campo** | **Tipo** | **Valores** |
|-----------|----------|-------------|
| **Status** | Lista | Not Executed, Passed, Failed, Blocked |
| **Executed_By** | Texto | Nome do testador |
| **Execution_Date** | Data | Data da execução |
| **Bug_ID** | Texto | ID do bug (se houver) |
| **Comments** | Texto | Observações da execução |

## 🐛 Gestão de Defeitos

### Critérios de Classificação

**Severidade Critical:**
- Sistema inutilizável
- Perda de dados
- Falhas de segurança

**Severidade High:**
- Funcionalidade principal não funciona
- Impacto significativo no negócio
- Bloqueio de fluxos críticos

**Severidade Medium:**
- Funcionalidade secundária afetada
- Workaround disponível
- Impacto moderado na usabilidade

**Severidade Low:**
- Problemas cosméticos
- Pequenas melhorias de UX
- Documentação/texto

## 📈 Métricas Recomendadas

### Durante Execução
- % de casos executados
- % de casos passando
- Número de bugs por severidade
- Taxa de bloqueios

### Ao Final
- Cobertura de testes por módulo
- Densidade de defeitos
- Eficiência da execução
- Qualidade geral do produto

## ⚙️ Ferramentas Sugeridas

**Para Gestão Completa:**
- **TestRail**: Gestão profissional de casos
- **Zephyr**: Integrado com Jira
- **qTest**: Plataforma completa de QA

**Para Uso Simples:**
- **Google Sheets**: Colaboração em tempo real
- **Excel**: Funcionalidades avançadas
- **Notion**: Documentação integrada

## 🔄 Processo de Atualização

1. **Novos Requisitos**: Criar novos casos com ID sequencial
2. **Mudanças**: Atualizar casos existentes mantendo histórico
3. **Depreciação**: Marcar casos obsoletos mas manter para auditoria
4. **Revisão**: Revisar casos trimestralmente

---

*Última atualização: 09/07/2025*
*Responsável: Equipe QA*