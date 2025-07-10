<div align="center">

# 🛒 Manual Test Suite - EcoShop E-commerce

![Static Badge](https://img.shields.io/badge/QA-Manual%20Testing-blue)
![Static Badge](https://img.shields.io/badge/Documentation-Markdown-green)
![Static Badge](https://img.shields.io/badge/Test%20Cases-CSV-orange)
![Static Badge](https://img.shields.io/badge/Status-Complete-brightgreen)

*Um conjunto abrangente de testes manuais demonstrando processos tradicionais de QA para um sistema de e-commerce*

</div>

---

## 📋 Índice

- [Sobre o Projeto](#-sobre-o-projeto)
- [Visão Geral do Sistema](#-visão-geral-do-sistema)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Começando](#-começando)
- [Documentação](#-documentação)
- [Execução de Testes](#-execução-de-testes)
- [Ferramentas e Tecnologias](#️-ferramentas-e-tecnologias)
- [Exemplos de Uso](#-exemplos-de-uso)
- [Métricas do Projeto](#-métricas-do-projeto)
- [Resultados de Aprendizagem](#-resultados-de-aprendizagem)
- [Contribuindo](#-contribuindo)
- [Suporte](#-suporte)
- [Agradecimentos](#-agradecimentos)
- [Licença](#-licença)

---

## 🎯 Sobre o Projeto

Este projeto apresenta um conjunto completo de testes manuais para o **EcoShop**, uma plataforma simulada de e-commerce sustentável. Ele demonstra práticas profissionais de QA incluindo planejamento de testes, design de casos, rastreamento de execução e relatórios.

### Principais Características

- ✅ **25 Casos de Teste Estruturados** cobrindo todos os módulos principais
- 📋 **Plano de Teste Abrangente** com cronogramas e alocação de recursos
- 🔄 **Checklist de Teste de Regressão** para validação de releases
- 📊 **Matriz de Rastreabilidade de Requisitos** garantindo cobertura completa
- 📈 **Templates de Relatório de Execução** para comunicação com stakeholders
- 🎭 **Gestão de Dados de Teste** com personas e cenários

---

## 🏪 Visão Geral do Sistema

**EcoShop** é uma plataforma de e-commerce sustentável com os seguintes recursos:

| Módulo | Funcionalidade |
|--------|----------------|
| 🔐 **Autenticação** | Registro de usuário, login, recuperação de senha |
| 🛍️ **Catálogo de Produtos** | Listagem de produtos, busca, filtros, detalhes |
| 🛒 **Carrinho de Compras** | Adicionar/remover itens, gerenciamento de quantidade |
| 💳 **Checkout** | Processamento de pedidos, pagamento, entrega |
| 📦 **Gerenciamento de Pedidos** | Histórico de pedidos, rastreamento, cancelamento |

---

## 📁 Estrutura do Projeto

```
manual-test-suite/
├── 📄 README.md                         # Documentação do projeto
├── 📄 USAGE-GUIDE.md                    # Instruções detalhadas de uso
├── 📄 .gitignore                        # Regras do Git ignore
├── 📂 docs/
│   ├── 📄 test-plan.md                  # Estratégia completa de teste
│   └── 📄 requirements-traceability.md  # Cobertura de requisitos
├── 📂 test-cases/
│   ├── 📄 test-cases.csv                # Casos de teste estruturados
│   ├── 📄 test-cases-readme.md          # Guia de casos de teste
│   └── 📂 test-data/
│       └── 📄 sample-data.md            # Conjuntos de dados de teste
├── 📂 regression-checklist/
│   └── 📄 regression-checklist.md       # Validação de release
└── 📂 reports/
    └── 📄 test-execution-template.md    # Template de relatório de execução
```

---

## 🚀 Começando

### Pré-requisitos

- Editor de texto ou IDE
- Aplicativo de planilhas (Excel, Google Sheets)
- Navegador web para testes
- Git para controle de versão

### Instalação

1. **Clone o repositório**
   ```bash
   git clone https://github.com/anthonycdp/manual-test-suite.git
   cd manual-test-suite
   ```

2. **Explore a documentação**
   ```bash
   # Comece com o README principal
   open README.md
   
   # Revise o plano de teste
   open docs/test-plan.md
   ```

3. **Importe os casos de teste**
   ```bash
   # Abra test-cases.csv no Excel ou Google Sheets
   # Adicione colunas de execução: Status, Executado_Por, Data, Observações
   ```

---

## 📚 Documentação

### Documentos Principais

| Documento | Propósito | Público-alvo |
|-----------|-----------|---------------|
| **Plano de Teste** | Estratégia, escopo, cronograma | Gerentes de projeto, stakeholders |
| **Casos de Teste** | Cenários detalhados de teste | Engenheiros de QA, testadores |
| **Checklist de Regressão** | Validação de release | Líderes de QA, gerentes de release |
| **Matriz de Rastreabilidade** | Análise de cobertura | Líderes de QA, analistas de negócios |
| **Template de Execução** | Relatório de resultados | Stakeholders, gerência |

### Métricas de Qualidade

- **Cobertura de Teste**: 100% dos requisitos identificados
- **Distribuição de Prioridade**: 60% P1, 32% P2, 8% P3
- **Tempo de Execução**: ~2-3 horas para regressão completa
- **Padrões de Documentação**: Conformidade com IEEE 829

---

## 🧪 Execução de Testes

### Início Rápido de Testes

1. **Teste de Fumaça** (30 minutos)
   ```bash
   # Execute cenários de caminho crítico
   # Foco em: Login → Adicionar ao Carrinho → Checkout
   ```

2. **Regressão Completa** (2-3 horas)
   ```bash
   # Execute todos os casos de teste por prioridade
   # Sequência P1 → P2 → P3
   ```

3. **Compatibilidade de Navegadores** (1 hora)
   ```bash
   # Teste em Chrome, Firefox, Safari, Edge
   # Verifique design responsivo
   ```

### Uso de Dados de Teste

- **Usuários**: 5 contas de teste pré-definidas
- **Produtos**: 20+ produtos de amostra em várias categorias
- **Cenários**: Combinações de carrinho de compras e casos extremos
- **Endereços**: Dados de endereço válidos/inválidos para testes

---

## 🛠️ Ferramentas e Tecnologias

<div align="center">

![Markdown](https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white)
![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)

</div>

### Ferramentas de QA Recomendadas

- **Gestão de Testes**: TestRail, Zephyr, qTest
- **Rastreamento de Bugs**: Jira, Azure DevOps, Bugzilla
- **Documentação**: Confluence, Notion, GitHub Wiki
- **Colaboração**: Slack, Microsoft Teams

---

## 💡 Exemplos de Uso

### Para Aprendizado de QA

```bash
# Estude a abordagem de planejamento de teste
cat docs/test-plan.md | grep -A 5 "Objetivos"

# Analise a estrutura dos casos de teste
head -5 test-cases/test-cases.csv

# Pratique com o checklist de regressão
open regression-checklist/regression-checklist.md
```

### Para Adaptação do Projeto

```bash
# Personalize para seu projeto
sed 's/EcoShop/SeuProjeto/g' README.md > novo-readme.md

# Importe casos de teste para sua ferramenta
# Use test-cases.csv como template
```

### Para Apresentação de Portfólio

```bash
# Destaque competências-chave
# - Planejamento e estratégia de teste
# - Rastreabilidade de requisitos
# - Padrões de design de casos de teste
# - Abordagem de teste de regressão
```

---

## 📊 Métricas do Projeto

| Métrica | Valor | Status |
|---------|-------|--------|
| **Casos de Teste** | 25 | ✅ Completo |
| **Módulos Cobertos** | 6 | ✅ Completo |
| **Páginas de Documentação** | 8 | ✅ Completo |
| **Cobertura de Requisitos** | 100% | ✅ Completo |
| **Conjuntos de Dados de Teste** | 50+ | ✅ Completo |

---

## 🎯 Resultados de Aprendizagem

Ao explorar este projeto, você entenderá:

- ✅ **Planejamento de Teste**: Como estruturar planos de teste abrangentes
- ✅ **Design de Teste**: Escrever casos de teste eficazes e manuteníveis
- ✅ **Rastreabilidade**: Garantir cobertura completa de requisitos
- ✅ **Teste de Regressão**: Abordagem sistemática para validação de release
- ✅ **Documentação**: Padrões profissionais de documentação de QA
- ✅ **Gestão de Processos**: Fluxos de trabalho de teste de ponta a ponta

---

## 🤝 Contribuindo

Contribuições são bem-vindas! Veja como você pode ajudar:

1. **Fork** o repositório
2. **Crie** um branch de feature (`git checkout -b feature/nova-funcionalidade`)
3. **Commit** suas mudanças (`git commit -m 'feat: adiciona nova funcionalidade'`)
4. **Push** para o branch (`git push origin feature/nova-funcionalidade`)
5. **Abra** um Pull Request

### Diretrizes de Contribuição

- Siga a estrutura de documentação existente
- Use mensagens de commit claras e descritivas
- Adicione casos de teste para novas funcionalidades
- Atualize a matriz de rastreabilidade para novos requisitos

---

## 📞 Suporte

Precisa de ajuda ou tem perguntas?

- 📧 **Email**: Crie uma issue neste repositório
- 📝 **Documentação**: Consulte o [USAGE-GUIDE.md](USAGE-GUIDE.md)
- 🐛 **Relatórios de Bug**: Use as issues do GitHub
- 💡 **Solicitações de Recursos**: Abra uma discussão

---

## 🏆 Agradecimentos

Este projeto demonstra:

- Padrões profissionais de documentação de QA
- Melhores práticas da indústria para testes manuais
- Abordagens abrangentes de planejamento de teste
- Padrões eficazes de design de casos de teste
- Metodologias de rastreabilidade de requisitos

Perfeito para profissionais de QA, estudantes e qualquer pessoa interessada em garantia de qualidade de software.

---

## 📄 Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

---

<div align="center">

**⭐ Dê uma estrela neste repositório se ele ajudou você a aprender sobre processos de QA!**

Feito com ❤️ para a comunidade QA

</div>