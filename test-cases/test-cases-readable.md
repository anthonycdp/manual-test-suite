# 📋 Casos de Teste - Visualização Legível

Este documento apresenta os casos de teste em formato mais legível. Para importação em ferramentas de teste, use o arquivo `test-cases.csv`.

## 📑 Índice por Módulo

- [Autenticação](#autenticação)
- [Catálogo de Produtos](#catálogo-de-produtos)
- [Carrinho de Compras](#carrinho-de-compras)
- [Checkout](#checkout)
- [Gerenciamento de Pedidos](#gerenciamento-de-pedidos)

---

## 🔐 Autenticação

### TC_AUTH_001: Cadastro de usuário com dados válidos
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** Sistema acessível, página de cadastro carregada
- **Passos do Teste:**
  1. Acessar página de cadastro
  2. Preencher campo Nome: 'João Silva'
  3. Preencher campo Email: 'joao.silva@email.com'
  4. Preencher campo Senha: 'MinhaSenh@123'
  5. Confirmar senha: 'MinhaSenh@123'
  6. Aceitar termos de uso
  7. Clicar em 'Cadastrar'
- **Resultado Esperado:** Usuário cadastrado com sucesso, redirecionamento para página de login com mensagem de confirmação
- **Dados de Teste:** 
  - Nome: João Silva
  - Email: joao.silva@email.com
  - Senha: MinhaSenh@123
- **Observações:** Validar critérios de senha forte

### TC_AUTH_002: Cadastro com email já existente
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** Email 'maria.santos@teste.com' já cadastrado no sistema
- **Passos do Teste:**
  1. Acessar página de cadastro
  2. Preencher todos os campos com dados válidos
  3. Usar email existente: 'maria.santos@teste.com'
  4. Clicar em 'Cadastrar'
- **Resultado Esperado:** Mensagem de erro: 'Este email já está cadastrado'
- **Dados de Teste:**
  - Nome: Maria Santos
  - Email: maria.santos@teste.com (já cadastrado)
  - Senha: Segura#456
- **Observações:** Verificar se não há vazamento de informações

### TC_AUTH_003: Login com credenciais válidas
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** Usuário cadastrado no sistema
- **Passos do Teste:**
  1. Acessar página de login
  2. Inserir email: 'pedro.costa@example.org'
  3. Inserir senha: 'Forte$789'
  4. Clicar em 'Entrar'
- **Resultado Esperado:** Login bem-sucedido, redirecionamento para página inicial do usuário
- **Dados de Teste:**
  - Email: pedro.costa@example.org
  - Senha: Forte$789
- **Observações:** Verificar token de sessão

### TC_AUTH_004: Recuperação de senha
- **Prioridade:** P2 | **Severidade:** Média
- **Pré-condições:** Usuário com email válido cadastrado
- **Passos do Teste:**
  1. Clicar em 'Esqueci minha senha'
  2. Inserir email: 'ana.oliveira@demo.net'
  3. Clicar em 'Enviar email de recuperação'
  4. Acessar email e clicar no link
  5. Definir nova senha
  6. Confirmar nova senha
- **Resultado Esperado:** Email enviado, senha redefinida com sucesso
- **Dados de Teste:**
  - Email: ana.oliveira@demo.net
  - Nova senha: NovaSenh@123
- **Observações:** Validar expiração do link

### TC_AUTH_005: Logout do sistema
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** Usuário logado no sistema
- **Passos do Teste:**
  1. Clicar no menu do usuário
  2. Selecionar opção 'Sair'
  3. Confirmar logout
- **Resultado Esperado:** Sessão encerrada, redirecionamento para página inicial
- **Dados de Teste:** N/A
- **Observações:** Verificar limpeza de cookies/sessão

---

## 🛍️ Catálogo de Produtos

### TC_PROD_001: Busca de produtos por palavra-chave
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** Catálogo com produtos cadastrados
- **Passos do Teste:**
  1. Acessar barra de busca
  2. Digitar 'camiseta orgânica'
  3. Pressionar Enter ou clicar em buscar
- **Resultado Esperado:** Lista de produtos relacionados à busca exibida
- **Dados de Teste:** Palavra-chave: camiseta orgânica
- **Observações:** Verificar relevância dos resultados

### TC_PROD_002: Filtrar produtos por categoria
- **Prioridade:** P2 | **Severidade:** Média
- **Pré-condições:** Produtos organizados por categorias
- **Passos do Teste:**
  1. Acessar página de produtos
  2. Selecionar categoria 'Moda Sustentável'
  3. Aplicar filtro de preço: R$ 50-150
  4. Ordenar por 'Mais vendidos'
- **Resultado Esperado:** Produtos filtrados conforme critérios selecionados
- **Dados de Teste:**
  - Categoria: Moda Sustentável
  - Faixa de preço: R$ 50-150
- **Observações:** Validar contadores de produtos

### TC_PROD_003: Visualizar detalhes do produto
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** Produto disponível no catálogo
- **Passos do Teste:**
  1. Localizar produto 'Camiseta Eco Algodão'
  2. Clicar na imagem ou título
  3. Verificar informações exibidas
  4. Ampliar imagens do produto
- **Resultado Esperado:** Página de detalhes com todas informações do produto
- **Dados de Teste:** ID Produto: PROD_ECO_001
- **Observações:** Verificar carregamento de imagens

### TC_PROD_004: Avaliar produto comprado
- **Prioridade:** P3 | **Severidade:** Baixa
- **Pré-condições:** Usuário logado com compra realizada
- **Passos do Teste:**
  1. Acessar 'Meus Pedidos'
  2. Selecionar produto para avaliar
  3. Atribuir 5 estrelas
  4. Escrever comentário
  5. Adicionar foto (opcional)
  6. Submeter avaliação
- **Resultado Esperado:** Avaliação registrada e visível na página do produto
- **Dados de Teste:**
  - Nota: 5 estrelas
  - Comentário: "Produto excelente, recomendo!"
- **Observações:** Validar moderação de conteúdo

### TC_PROD_005: Verificar produtos indisponíveis
- **Prioridade:** P2 | **Severidade:** Média
- **Pré-condições:** Produto com estoque zerado
- **Passos do Teste:**
  1. Acessar produto sem estoque
  2. Verificar indicação visual
  3. Tentar adicionar ao carrinho
  4. Solicitar notificação de disponibilidade
- **Resultado Esperado:** Indicação clara de indisponibilidade, opção de notificação ativa
- **Dados de Teste:** ID Produto: PROD_OUT_001
- **Observações:** Verificar tratamento de erro

---

## 🛒 Carrinho de Compras

### TC_CART_001: Adicionar produto ao carrinho
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** Produto disponível em estoque
- **Passos do Teste:**
  1. Acessar página do produto
  2. Selecionar tamanho: 'M'
  3. Selecionar cor: 'Verde'
  4. Quantidade: 2
  5. Clicar em 'Adicionar ao Carrinho'
- **Resultado Esperado:** Produto adicionado, contador do carrinho atualizado
- **Dados de Teste:**
  - Produto: Camiseta Eco
  - Tamanho: M
  - Cor: Verde
  - Quantidade: 2
- **Observações:** Verificar persistência do carrinho

### TC_CART_002: Alterar quantidade no carrinho
- **Prioridade:** P2 | **Severidade:** Média
- **Pré-condições:** Produto já adicionado ao carrinho
- **Passos do Teste:**
  1. Acessar carrinho
  2. Localizar produto
  3. Alterar quantidade de 1 para 3
  4. Verificar atualização do valor
- **Resultado Esperado:** Quantidade e valor total atualizados corretamente
- **Dados de Teste:** Alterar quantidade para 3
- **Observações:** Validar cálculo de descontos

### TC_CART_003: Remover item do carrinho
- **Prioridade:** P2 | **Severidade:** Média
- **Pré-condições:** Carrinho com pelo menos um item
- **Passos do Teste:**
  1. Acessar carrinho
  2. Clicar em 'Remover' no item
  3. Confirmar remoção
- **Resultado Esperado:** Item removido, total recalculado
- **Dados de Teste:** N/A
- **Observações:** Opção de desfazer remoção

### TC_CART_004: Aplicar cupom de desconto
- **Prioridade:** P2 | **Severidade:** Média
- **Pré-condições:** Cupom válido disponível
- **Passos do Teste:**
  1. Acessar carrinho com produtos
  2. Inserir código: 'ECO10'
  3. Clicar em 'Aplicar'
  4. Verificar desconto aplicado
- **Resultado Esperado:** Desconto de 10% aplicado ao total
- **Dados de Teste:** Cupom: ECO10 (10% desconto)
- **Observações:** Validar regras do cupom

### TC_CART_005: Salvar carrinho para depois
- **Prioridade:** P3 | **Severidade:** Baixa
- **Pré-condições:** Usuário logado com itens no carrinho
- **Passos do Teste:**
  1. Adicionar produtos ao carrinho
  2. Clicar em 'Salvar para depois'
  3. Fazer logout
  4. Login novamente
  5. Verificar carrinho salvo
- **Resultado Esperado:** Carrinho restaurado após novo login
- **Dados de Teste:** N/A
- **Observações:** Verificar tempo de expiração

---

## 💳 Checkout

### TC_CHECKOUT_001: Finalizar compra com cartão de crédito
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** Carrinho com produtos, usuário logado
- **Passos do Teste:**
  1. Clicar em 'Finalizar Compra'
  2. Confirmar endereço de entrega
  3. Selecionar 'Cartão de Crédito'
  4. Inserir dados do cartão
  5. Revisar pedido
  6. Confirmar compra
- **Resultado Esperado:** Pedido confirmado, email de confirmação enviado
- **Dados de Teste:**
  - Cartão: 4111 1111 1111 1111
  - CVV: 123
  - Validade: 12/25
- **Observações:** Usar ambiente de teste

### TC_CHECKOUT_002: Calcular frete
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** CEP válido, produtos no carrinho
- **Passos do Teste:**
  1. No checkout, inserir CEP: 01310-100
  2. Clicar em 'Calcular'
  3. Selecionar opção de frete
- **Resultado Esperado:** Opções de frete com prazos e valores exibidos
- **Dados de Teste:** CEP: 01310-100
- **Observações:** Validar integração com correios

### TC_CHECKOUT_003: Adicionar novo endereço
- **Prioridade:** P2 | **Severidade:** Média
- **Pré-condições:** Usuário no processo de checkout
- **Passos do Teste:**
  1. Clicar em 'Adicionar novo endereço'
  2. Preencher formulário completo
  3. Marcar como endereço principal
  4. Salvar endereço
- **Resultado Esperado:** Endereço salvo e selecionado para entrega
- **Dados de Teste:**
  - Rua: Av. Paulista, 1000
  - CEP: 01310-100
  - Cidade: São Paulo
  - Estado: SP
- **Observações:** Validar campos obrigatórios

### TC_CHECKOUT_004: Pagamento com boleto
- **Prioridade:** P2 | **Severidade:** Média
- **Pré-condições:** Opção de boleto habilitada
- **Passos do Teste:**
  1. Selecionar 'Boleto Bancário'
  2. Confirmar dados
  3. Gerar boleto
  4. Verificar prazo de pagamento
- **Resultado Esperado:** Boleto gerado com código de barras válido
- **Dados de Teste:** N/A
- **Observações:** Verificar prazo de 3 dias úteis

### TC_CHECKOUT_005: Validação de estoque no checkout
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** Produto com estoque limitado
- **Passos do Teste:**
  1. Adicionar produto com pouco estoque
  2. Iniciar checkout
  3. Durante processo, estoque se esgota
  4. Tentar finalizar compra
- **Resultado Esperado:** Alerta sobre indisponibilidade, opção de remover item
- **Dados de Teste:** Produto com 1 unidade em estoque
- **Observações:** Tratamento de concorrência

---

## 📦 Gerenciamento de Pedidos

### TC_ORDER_001: Visualizar histórico de pedidos
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** Usuário com pedidos realizados
- **Passos do Teste:**
  1. Acessar 'Minha Conta'
  2. Clicar em 'Meus Pedidos'
  3. Verificar lista de pedidos
  4. Filtrar por período
- **Resultado Esperado:** Lista completa de pedidos com status atualizado
- **Dados de Teste:** N/A
- **Observações:** Verificar paginação

### TC_ORDER_002: Rastrear entrega
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** Pedido enviado com código de rastreio
- **Passos do Teste:**
  1. Acessar detalhes do pedido
  2. Clicar em 'Rastrear Entrega'
  3. Verificar status atualizado
- **Resultado Esperado:** Informações de rastreamento em tempo real
- **Dados de Teste:** Código: BR123456789
- **Observações:** Integração com transportadora

### TC_ORDER_003: Cancelar pedido
- **Prioridade:** P1 | **Severidade:** Alta
- **Pré-condições:** Pedido com status 'Processando'
- **Passos do Teste:**
  1. Acessar pedido recente
  2. Clicar em 'Cancelar Pedido'
  3. Selecionar motivo
  4. Confirmar cancelamento
- **Resultado Esperado:** Pedido cancelado, email de confirmação enviado
- **Dados de Teste:** Motivo: Compra duplicada
- **Observações:** Verificar política de cancelamento

### TC_ORDER_004: Solicitar troca ou devolução
- **Prioridade:** P2 | **Severidade:** Média
- **Pré-condições:** Pedido entregue há menos de 7 dias
- **Passos do Teste:**
  1. Selecionar pedido entregue
  2. Clicar em 'Trocar/Devolver'
  3. Selecionar produtos e motivo
  4. Escolher: Troca por outro tamanho
  5. Gerar código de postagem
- **Resultado Esperado:** Solicitação registrada, instruções de envio fornecidas
- **Dados de Teste:**
  - Motivo: Tamanho incorreto
  - Ação: Trocar por tamanho G
- **Observações:** Prazo de 7 dias

### TC_ORDER_005: Baixar nota fiscal
- **Prioridade:** P2 | **Severidade:** Média
- **Pré-condições:** Pedido com NF emitida
- **Passos do Teste:**
  1. Acessar pedido faturado
  2. Clicar em 'Baixar NF-e'
  3. Verificar PDF gerado
- **Resultado Esperado:** Download do PDF da nota fiscal
- **Dados de Teste:** N/A
- **Observações:** Validar dados fiscais

---

## 📊 Resumo dos Casos de Teste

| Módulo | Total | P1 | P2 | P3 |
|--------|-------|----|----|-----|
| Autenticação | 5 | 3 | 2 | 0 |
| Catálogo | 5 | 2 | 2 | 1 |
| Carrinho | 5 | 1 | 3 | 1 |
| Checkout | 5 | 3 | 2 | 0 |
| Pedidos | 5 | 3 | 2 | 0 |
| **TOTAL** | **25** | **12** | **11** | **2** |

## 🔗 Arquivos Relacionados

- **CSV Original:** [test-cases.csv](./test-cases.csv) - Para importação em ferramentas
- **Dados de Teste:** [sample-data.md](./test-data/sample-data.md) - Dados completos para execução
- **Guia de Uso:** [test-cases-readme.md](./test-cases-readme.md) - Instruções detalhadas