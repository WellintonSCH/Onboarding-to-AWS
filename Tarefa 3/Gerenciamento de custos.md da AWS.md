# Usando o AWS Budgets para Monitorar Custos e Uso na AWS

O **AWS Budgets** é uma ferramenta poderosa para monitorar e gerenciar seus custos e uso na AWS. Ele permite definir limites personalizados e receber alertas quando esses limites são excedidos ou quando há previsão de excedê-los.

---

## O que é o AWS Budgets?
O AWS Budgets permite:
- **Monitorar custos e uso** em sua conta AWS.
- **Definir orçamentos** para custos, uso, utilização de Instâncias Reservadas (RIs) e Savings Plans.
- **Receber alertas** por e-mail ou Amazon SNS quando os limites são excedidos ou quando há previsão de excedê-los.

---

## Tipos de Orçamentos Suportados
Você pode criar os seguintes tipos de orçamentos:

1. **Orçamentos de Custos**:
   - Planeje quanto deseja gastar em um serviço.
   - Exemplo: Definir um orçamento mensal de $1.000 para todos os serviços da AWS.

2. **Orçamentos de Uso**:
   - Planeje o quanto deseja usar um ou mais serviços.
   - Exemplo: Definir um limite de uso para o Amazon S3.

3. **Orçamentos de Utilização de RIs**:
   - Defina um limite de utilização para Instâncias Reservadas.
   - Exemplo: Receber alertas se a utilização de RIs cair abaixo de 80%.

4. **Orçamentos de Cobertura de RIs**:
   - Defina um limite de cobertura para Instâncias Reservadas.
   - Exemplo: Receber alertas se a cobertura de RIs cair abaixo de um limite definido.

5. **Orçamentos de Utilização de Savings Plans**:
   - Defina um limite de utilização para Savings Plans.
   - Exemplo: Receber alertas se a utilização de Savings Plans cair abaixo de 80%.

6. **Orçamentos de Cobertura de Savings Plans**:
   - Defina um limite de cobertura para Savings Plans.
   - Exemplo: Receber alertas se a cobertura de Savings Plans cair abaixo de um limite definido.

---

## Como Funcionam as Notificações?
- **Alertas de Custo e Uso**:  
   - Receba notificações quando os custos ou uso excederem (ou previsão de exceder) o valor definido.
   - As notificações podem ser enviadas por e-mail ou para um tópico do **Amazon SNS**.

- **Alertas de Utilização e Cobertura**:  
   - Receba notificações quando a utilização ou cobertura de RIs ou Savings Plans ficar abaixo do limite definido.

---

## Configuração de Orçamentos
1. **Acesse o Console do AWS Budgets**:
   - No Console da AWS, procure por **Budgets**.

2. **Crie um Novo Orçamento**:
   - Escolha o tipo de orçamento (custo, uso, utilização de RIs, etc.).
   - Defina o valor do orçamento e os limites de notificação.

3. **Configure Notificações**:
   - Adicione endereços de e-mail ou um tópico do Amazon SNS para receber alertas.

4. **Aplique Ações Automáticas (Opcional)**:
   - Por exemplo, aplicar uma política do IAM para negar a criação de novos recursos se o orçamento for excedido.

---

## Melhores Práticas
- **Monitoramento Proativo**:  
   - Configure alertas para custos reais e previstos para evitar surpresas.
- **Uso de RIs e Savings Plans**:  
   - Monitore a utilização e cobertura para garantir que você está aproveitando ao máximo seus compromissos financeiros.
- **Consolidação de Contas**:  
   - Se usar o **faturamento consolidado** com AWS Organizations, gerencie orçamentos na conta de gerenciamento e controle o acesso das contas membros.

---

## Considerações Importantes
- **Atualizações de Dados**:  
   - As informações do AWS Budgets são atualizadas até **três vezes por dia**.
   - Pode haver um atraso entre o uso de um recurso e a cobrança refletida no orçamento.

- **Acesso e Visibilidade**:  
   - Orçamentos são visíveis apenas para usuários com acesso à conta que os criou.
   - Use políticas do IAM para controlar permissões de criação e edição de orçamentos.

---

**Nota:** O AWS Budgets é uma ferramenta essencial para otimizar custos e garantir que você esteja dentro dos limites planejados. Use-a para evitar surpresas na fatura da AWS!
