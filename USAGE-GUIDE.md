# Guia de Uso - Manual Test Suite

## 🎯 Como Usar Este Projeto

### 1. **Para Estudar QA (Iniciantes)**

#### **Sequência Recomendada:**
1. **README.md** - Entenda o projeto e sistema simulado
2. **docs/test-plan.md** - Aprenda estrutura de planos de teste
3. **test-cases/test-cases.csv** - Veja casos de teste bem escritos
4. **regression-checklist/regression-checklist.md** - Processo de regressão
5. **docs/requirements-traceability.md** - Rastreabilidade e cobertura

#### **Exercícios Práticos:**
- Importe `test-cases.csv` no Excel/Google Sheets
- Simule execução marcando status dos casos
- Pratique escrevendo novos casos seguindo o padrão
- Use o checklist para simular uma regressão

---

### 2. **Para Adaptar a Projetos Reais**

#### **Passo 1: Customizar Sistema**
```bash
# Substitua "EcoShop" pelo nome do seu projeto
# Atualize funcionalidades no test-plan.md
# Adapte casos de teste para suas funcionalidades
```

#### **Passo 2: Importar Casos de Teste**
```bash
# Opção 1: Excel/Google Sheets
1. Abra test-cases.csv no Excel
2. Adicione colunas: Status, Executado_Por, Data_Execucao
3. Use filtros para organizar por módulo/prioridade

# Opção 2: Ferramentas QA
1. TestRail: Importe via CSV
2. Zephyr: Use template fornecido
3. Azure DevOps: Adapte formato
```

#### **Passo 3: Configurar Processo**
```bash
# Adapte cronograma no test-plan.md
# Customize checklist de regressão
# Ajuste critérios de entrada/saída
# Configure dados de teste para seu ambiente
```

---

### 3. **Para Apresentar em Entrevistas**

#### **Prepare-se para Perguntas:**
- "Como você estrutura um plano de testes?"
- "Como garante cobertura de requisitos?"
- "Qual sua abordagem para regressão?"
- "Como prioriza casos de teste?"

#### **Demonstre Conhecimento:**
- Mostre matriz de rastreabilidade
- Explique critérios de severidade/prioridade
- Discuta estratégia de dados de teste
- Apresente template de relatório

---

### 4. **Para Ensinar QA**

#### **Material Didático:**
- Use casos reais do e-commerce
- Demonstre evolução de documentação
- Mostre boas práticas de escrita
- Exemplifique processo completo

#### **Exercícios para Alunos:**
1. Escrever novos casos de teste
2. Executar checklist de regressão
3. Criar relatório de bugs
4. Analisar gaps de cobertura

---

## 🛠️ Ferramentas Recomendadas

### **Para Uso Básico:**
- **Excel/Google Sheets**: Gestão simples de casos
- **Word/Google Docs**: Documentação e relatórios
- **GitHub**: Versionamento da documentação

### **Para Uso Profissional:**
- **TestRail**: Gestão completa de testes
- **Zephyr**: Integrado com Jira
- **Azure DevOps**: Processo completo
- **Notion**: Documentação colaborativa

---

## 📊 Personalizações Comuns

### **Adaptar para Diferentes Sistemas:**

#### **Sistema Web (SaaS):**
```bash
# Foque em: Autenticação, Painéis, Relatórios
# Adicione: Permissões, Multi-tenancy
# Remova: Carrinho, Checkout
```

#### **Sistema Mobile:**
```bash
# Adicione: Testes de gestos, Orientação
# Foque em: Responsividade, Performance
# Inclua: Notificações, Offline
```

#### **Sistema Enterprise:**
```bash
# Adicione: Integração, Workflow
# Foque em: Segurança, Auditoria
# Inclua: Relatórios, Configurações
```

### **Adaptar para Diferentes Metodologias:**

#### **Scrum/Agile:**
```bash
# Quebre casos por sprint
# Adicione Definition of Done
# Foque em testes de aceitação
```

#### **Waterfall:**
```bash
# Mantenha estrutura completa
# Adicione marcos de entrega
# Foque em documentação detalhada
```

---

## 🔄 Processo de Execução

### **Ciclo Completo:**

#### **Fase 1: Planejamento (1-2 dias)**
1. Revise test-plan.md
2. Atualize casos de teste
3. Prepare dados de teste
4. Configure ambiente

#### **Fase 2: Execução (1-2 semanas)**
1. Execute smoke test primeiro
2. Siga prioridades (P1 → P2 → P3)
3. Reporte bugs imediatamente
4. Atualize status dos casos

#### **Fase 3: Regressão (1-2 dias)**
1. Execute regression-checklist.md
2. Valide correções de bugs
3. Confirme funcionalidades críticas
4. Aprovação final

#### **Fase 4: Relatório (1 dia)**
1. Compile resultados
2. Use template em reports/
3. Analise métricas
4. Recomende ações

---

## 📈 Métricas de Sucesso

### **Durante Execução:**
- % de casos executados
- % de casos passando
- Número de bugs por severidade
- Tempo médio por caso

### **Ao Final:**
- Cobertura de requisitos
- Densidade de defeitos
- Eficiência da equipe
- Qualidade final do produto

---

## 🎓 Certificações Relacionadas

### **Use Este Projeto Para:**
- **ISTQB Foundation**: Demonstre conhecimento prático
- **ASTQB**: Aplique conceitos aprendidos
- **CTAL**: Mostre liderança em QA
- **Agile Testing**: Adapte para metodologias ágeis

---

## 🔧 Troubleshooting

### **Problemas Comuns:**

#### **"Casos muito genéricos"**
- Adicione mais detalhes nos passos
- Inclua dados específicos
- Crie variações para cenários complexos

#### **"Falta automação"**
- Este projeto foca em testes manuais
- Use como base para identificar casos automatizáveis
- Mantenha regressão manual para validações críticas

#### **"Documentação muito extensa"**
- Adapte o nível de detalhamento ao seu contexto
- Use templates como base, não como obrigação
- Foque no que agrega valor ao seu projeto

---

## 📞 Próximos Passos

### **Para Crescer na Carreira:**
1. **Automação**: Aprenda Selenium, Cypress
2. **Performance**: Estude JMeter, LoadRunner
3. **API Testing**: Pratique Postman, RestAssured
4. **CI/CD**: Integre testes em pipelines

### **Para Melhorar Este Projeto:**
1. Adicione testes de API
2. Inclua casos de performance
3. Crie automação básica
4. Implemente métricas avançadas

---

*Este projeto é um ponto de partida. Adapte conforme suas necessidades e continue evoluindo suas habilidades em QA!*