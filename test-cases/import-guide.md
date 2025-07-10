# 📊 Guia de Importação - test-cases.csv

Este guia mostra como importar corretamente o arquivo `test-cases.csv` em diferentes aplicações de planilhas.

## 🟦 Microsoft Excel

### Método 1: Abertura Direta
1. **Clique com botão direito** no arquivo `test-cases.csv`
2. Selecione **"Abrir com"** → **Microsoft Excel**
3. O Excel detectará automaticamente as configurações

### Método 2: Importação via Excel
1. Abra o **Microsoft Excel**
2. Vá em **Dados** → **Obter Dados** → **De Arquivo** → **De Texto/CSV**
3. Navegue até o arquivo `test-cases.csv` e selecione-o
4. Na janela de preview:
   - **Delimitador**: Vírgula
   - **Codificação**: UTF-8
   - **Detecção de tipo de dados**: Automático
5. Clique em **Carregar**

### Formatação Recomendada no Excel
Após importar, ajuste as colunas:
1. Selecione todas as células (Ctrl+A)
2. Vá em **Página Inicial** → **Formatar** → **AutoAjustar Largura da Coluna**
3. Para melhor visualização dos passos de teste:
   - Selecione a coluna **Test_Steps**
   - Clique com botão direito → **Formatar Células**
   - Aba **Alinhamento** → Marque **Quebrar texto automaticamente**
   - Faça o mesmo para **Expected_Result** e **Test_Data**

---

## 🟩 Google Sheets

### Método 1: Upload Direto
1. Acesse [Google Sheets](https://sheets.google.com)
2. Clique no **ícone de pasta** para abrir arquivo
3. Vá na aba **Upload**
4. Arraste o arquivo `test-cases.csv` ou clique em **Selecionar arquivo**
5. O Google Sheets importará automaticamente

### Método 2: Importação em Planilha Existente
1. Em uma planilha aberta, vá em **Arquivo** → **Importar**
2. Selecione **Upload** e escolha o arquivo
3. Configure as opções:
   - **Tipo de importação**: Criar nova planilha
   - **Separador**: Detectar automaticamente
4. Clique em **Importar dados**

### Formatação Recomendada no Google Sheets
1. **Ajustar largura das colunas**:
   - Selecione todas as colunas
   - Clique na borda entre colunas e arraste
   - Ou: Clique direito → **Redimensionar colunas** → **Ajustar aos dados**

2. **Quebra de texto**:
   - Selecione colunas Test_Steps, Expected_Result e Test_Data
   - **Formatar** → **Quebra de texto** → **Quebrar**

3. **Congelar cabeçalho**:
   - **Visualizar** → **Congelar** → **1 linha**

---

## 🟨 LibreOffice Calc

### Importação
1. Abra o **LibreOffice Calc**
2. **Arquivo** → **Abrir**
3. Selecione o arquivo `test-cases.csv`
4. Na janela de importação:
   - **Conjunto de caracteres**: UTF-8
   - **Separado por**: Vírgula
   - **Delimitador de texto**: " (aspas)
5. Clique em **OK**

---

## 🔧 Configurações Importantes

### Problemas Comuns e Soluções

#### 1. Caracteres Especiais Aparecem Incorretos
**Solução**: Certifique-se de selecionar **UTF-8** como codificação durante a importação

#### 2. Quebras de Linha nos Campos
O arquivo contém quebras de linha dentro dos campos (especialmente em Test_Steps). Isso é normal e esperado:
- **Excel/Google Sheets**: Geralmente lidam bem automaticamente
- **Se houver problemas**: Use a opção "Delimitador de texto" com aspas (")

#### 3. Colunas Desalinhadas
**Solução**: Verifique se o delimitador está configurado como **vírgula** (,)

---

## 📋 Estrutura das Colunas

Após importar, você verá as seguintes colunas:

| Coluna | Descrição | Tipo de Conteúdo |
|--------|-----------|------------------|
| **Test_ID** | Identificador único | Texto (TC_XXX_000) |
| **Module** | Módulo do sistema | Texto |
| **Test_Title** | Título do caso de teste | Texto |
| **Priority** | Prioridade (P1, P2, P3) | Texto |
| **Severity** | Severidade (Critical, High, Medium, Low) | Texto |
| **Preconditions** | Pré-condições necessárias | Texto |
| **Test_Steps** | Passos numerados | Texto com quebras |
| **Expected_Result** | Resultado esperado | Texto |
| **Test_Data** | Dados para execução | Texto com quebras |
| **Notes** | Observações adicionais | Texto |

---

## 🎯 Dicas para Uso Eficiente

### 1. Adicionar Colunas de Execução
Após importar, adicione estas colunas para rastreamento:
- **Status** (Passou/Falhou/Bloqueado/Não Executado)
- **Executado_Por** (Nome do testador)
- **Data_Execução** (Data do teste)
- **Defeitos** (IDs de bugs encontrados)
- **Observações_Execução** (Notas durante o teste)

### 2. Usar Filtros
- **Excel**: Dados → Filtro
- **Google Sheets**: Dados → Criar um filtro
- **LibreOffice**: Dados → AutoFiltro

Filtros úteis:
- Por **Module** para testar áreas específicas
- Por **Priority** para testes de regressão
- Por **Status** para acompanhar progresso

### 3. Formatação Condicional
Configure cores para facilitar visualização:
- **Vermelho**: Status = Falhou
- **Verde**: Status = Passou
- **Amarelo**: Status = Bloqueado
- **Cinza**: Status = Não Executado

### 4. Criar Dashboards
Use recursos de tabela dinâmica para criar resumos:
- Total de casos por módulo
- Taxa de aprovação/falha
- Progresso de execução
- Defeitos por severidade

---

## 💡 Exemplo de Uso

### Cenário: Executar Teste de Regressão P1

1. **Filtrar** por Priority = P1
2. **Ordenar** por Module
3. **Adicionar** data de hoje na coluna Data_Execução
4. **Executar** cada caso seguindo os passos
5. **Marcar** Status conforme resultado
6. **Registrar** IDs de defeitos se houver falhas
7. **Exportar** relatório filtrado para compartilhar

---

## 📤 Exportação e Compartilhamento

### Excel
- **Arquivo** → **Salvar Como** → Escolher formato (.xlsx, .pdf, etc.)

### Google Sheets
- **Arquivo** → **Download** → Escolher formato
- **Arquivo** → **Compartilhar** para colaboração em tempo real

### LibreOffice
- **Arquivo** → **Exportar como PDF** para relatórios
- **Arquivo** → **Salvar Como** para outros formatos

---

## 🆘 Suporte

Se encontrar problemas na importação:
1. Verifique se o arquivo não foi corrompido
2. Tente abrir primeiro em um editor de texto para verificar a estrutura
3. Use a versão legível em `test-cases-readable.md` como referência
4. Crie uma issue no repositório para obter ajuda