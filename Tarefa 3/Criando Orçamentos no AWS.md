# Criando Orçamentos no AWS Budgets Usando Modelos

O AWS Budgets oferece **modelos pré-configurados** para simplificar a criação de orçamentos. Esses modelos são ideais para quem deseja começar rapidamente com configurações recomendadas.

---

## O que são Modelos de Orçamento?
Os modelos de orçamento são configurações pré-definidas que ajudam a criar orçamentos de forma rápida e fácil. Eles são uma alternativa ao fluxo de trabalho avançado de 5 etapas, ideal para usuários que desejam começar com boas práticas.

---

## Tipos de Modelos Disponíveis
1. **Orçamento de Gastos Zero**:
   - Notifica você quando seus gastos excedem os limites do **AWS Free Tier**.
   - Ideal para monitorar o uso gratuito da AWS.

2. **Orçamento de Custo Mensal**:
   - Define um orçamento mensal e notifica se você exceder (ou previsão de exceder) o valor definido.
   - Exemplo: Definir um limite de $500 por mês.

3. **Orçamento de Cobertura dos Savings Plans Diários**:
   - Notifica quando a cobertura dos **Savings Plans** fica abaixo de um limite definido.
   - Ajuda a identificar gastos sob demanda e a considerar novos compromissos.

4. **Orçamento de Utilização de Instâncias Reservadas Diárias**:
   - Notifica quando a utilização das **Instâncias Reservadas (RIs)** fica abaixo de um limite definido.
   - Ajuda a identificar subutilização de RIs.

---

## Como Criar um Orçamento Usando um Modelo

### Passo a Passo:
1. **Acesse o Console do AWS Budgets**:
   - Abra o [Console de Faturamento e Gerenciamento de Custos](https://console.aws.amazon.com/cost-management/).

2. **Navegue até Orçamentos**:
   - No painel de navegação, escolha **Orçamentos**.

3. **Crie um Novo Orçamento**:
   - Clique em **Criar orçamento**.

4. **Escolha Usar um Modelo**:
   - Em **Configuração de orçamento**, selecione **Usar um modelo (simplificado)**.

5. **Selecione um Modelo**:
   - Escolha o modelo que melhor atende ao seu caso de uso:
     - **Orçamento de gasto zero**
     - **Orçamento de custo mensal**
     - **Orçamento de cobertura dos Savings Plans diários**
     - **Orçamento de utilização de reserva diária**

6. **Atualize as Configurações**:
   - Ajuste os detalhes do modelo, como valores, limites de notificação e destinatários de alertas.

7. **Crie o Orçamento**:
   - Clique em **Criar orçamento**.

---

## Personalizando um Modelo
- Após criar o orçamento, você pode **editar as configurações** no fluxo de trabalho avançado.
- Para fazer alterações, vá para **Configurações do modelo** e escolha **Personalizado**.
- Adicione filtros, contas vinculadas ou outras configurações conforme necessário.

---

## Vantagens dos Modelos de Orçamento
- **Simplicidade**: Fluxo de trabalho de uma única página.
- **Boas Práticas**: Configurações recomendadas para casos de uso comuns.
- **Flexibilidade**: Personalização posterior para atender a necessidades específicas.

---

Para mais detalhes, consulte a [documentação oficial do AWS Budgets](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets.html).
