# AWS config

O **AWS Config** é um serviço que fornece uma visão detalhada da configuração dos recursos da AWS em sua conta. Ele permite monitorar como os recursos estão configurados, como se relacionam entre si e como suas configurações mudam ao longo do tempo.

---

## O que é o AWS Config?

- **Monitoramento de Recursos**:  
  - Rastreia a configuração de recursos da AWS, como instâncias EC2, volumes EBS, grupos de segurança, VPCs, etc.
- **Histórico de Configurações**:  
  - Mantém um histórico das configurações dos recursos, permitindo ver como eles mudaram ao longo do tempo.
- **Relacionamentos entre Recursos**:  
  - Mostra como os recursos estão interconectados, ajudando a entender o impacto de mudanças.

---

## Principais Funcionalidades

### 1. **Gerenciamento de Recursos**
   - **Visibilidade**:  
     - Veja quais recursos existem e como estão configurados.
   - **Notificações**:  
     - Receba alertas quando recursos são criados, modificados ou excluídos.
   - **Snapshots e Histórico**:  
     - Armazene snapshots e histórico de configurações em um bucket do Amazon S3.

### 2. **Regras e Conformidade**
   - **Avaliação de Conformidade**:  
     - Use regras do AWS Config para avaliar se os recursos estão em conformidade com políticas internas ou melhores práticas.
   - **Pacotes de Conformidade**:  
     - Implemente e monitore coleções de regras como uma única entidade.

### 3. **Análise de Segurança**
   - **Auditoria de Permissões**:  
     - Veja as políticas do IAM atribuídas a usuários, grupos ou roles em um determinado momento.
   - **Regras de Grupos de Segurança**:  
     - Analise as regras de grupos de segurança do EC2 para identificar possíveis vulnerabilidades.

### 4. **Agregação de Dados**
   - **Visão Centralizada**:  
     - Use agregadores para consolidar dados de configuração e conformidade de várias contas e regiões da AWS em um único local.

### 5. **Consultas Avançadas**
   - **Consultas Personalizadas**:  
     - Use consultas predefinidas ou crie suas próprias consultas para analisar o estado atual dos recursos.

---

## Casos de Uso Comuns

### 1. **Governança de Recursos**
   - Monitore mudanças na configuração de recursos para garantir conformidade com políticas internas.

### 2. **Auditoria e Conformidade**
   - Acesse histórico de configurações para demonstrar conformidade com regulamentações e melhores práticas.

### 3. **Gerenciamento de Mudanças**
   - Avalie o impacto de mudanças de configuração em recursos relacionados.

### 4. **Análise de Segurança**
   - Identifique possíveis vulnerabilidades analisando configurações históricas de recursos.

### 5. **Solução de Problemas**
   - Use o histórico de configurações para restaurar a última configuração conhecida de um recurso problemático.

---

## Como Configurar o AWS Config

### Pré-requisitos
1. **Conta AWS Ativa**:  
   - Necessária para acessar e configurar o AWS Config.
2. **Bucket do Amazon S3**:  
   - Para armazenar snapshots e histórico de configurações.
3. **Tópico do Amazon SNS**:  
   - Para receber notificações sobre mudanças de configuração.
4. **Role do IAM**:  
   - Para conceder permissões necessárias ao AWS Config.

### Passo a Passo
1. **Habilite o AWS Config**:  
   - No Console da AWS, acesse o AWS Config e habilite a gravação de recursos.
2. **Escolha Tipos de Recursos**:  
   - Selecione os tipos de recursos que deseja monitorar.
3. **Configure Notificações**:  
   - Defina um tópico do SNS para receber alertas.
4. **Crie Regras de Conformidade**:  
   - Defina regras para avaliar a conformidade dos recursos.
5. **Revise Dados e Relatórios**:  
   - Use o Console ou APIs para acessar snapshots, histórico e relatórios de conformidade.

---

## Benefícios do AWS Config

1. **Visibilidade Completa**:  
   - Tenha uma visão detalhada de todos os recursos e suas configurações.
2. **Conformidade Simplificada**:  
   - Facilite a auditoria e a demonstração de conformidade.
3. **Segurança Aprimorada**:  
   - Identifique e corrija vulnerabilidades rapidamente.
4. **Gerenciamento Eficiente**:  
   - Monitore e gerencie mudanças de configuração de forma proativa.

---

## Próximos Passos
- **Habilite o AWS Config**:  
  - Acesse o Console da AWS e comece a monitorar seus recursos.
- **Explore a Documentação Oficial**:  
  - Para mais detalhes, consulte a [documentação do AWS Config](https://docs.aws.amazon.com/config/latest/developerguide/).

---

**Resumo:** O AWS Config é uma ferramenta poderosa para monitorar, auditar e gerenciar a configuração de recursos na AWS. Use-o para garantir conformidade, segurança e governança eficiente dos seus recursos na nuvem! 😊
