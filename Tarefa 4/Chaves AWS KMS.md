# Tipos de Chaves no AWS KMS

O **AWS Key Management Service (KMS)** permite criar e gerenciar chaves de criptografia para proteger seus dados. Existem três tipos principais de chaves no KMS, cada uma com diferentes níveis de controle, custos e casos de uso.

---

## Tipos de Chaves no AWS KMS

### 1. **Chaves Gerenciadas pelo Cliente**
- **O que são?**  
  Chaves criadas e gerenciadas por você na sua conta AWS.
- **Controle:**  
  - Total controle sobre o ciclo de vida da chave (criação, rotação, exclusão).
  - Pode definir políticas de chave, políticas do IAM e grants.
- **Uso:**  
  - Para aplicativos criptográficos próprios.
  - Integração com serviços da AWS que suportam chaves gerenciadas pelo cliente.
- **Custos:**  
  - Taxa mensal pela existência da chave (prorrateada por hora).
  - Taxa por uso (operações criptográficas).
- **Auditoria:**  
  - Uso da chave pode ser auditado via AWS CloudTrail.
- **Recomendação:**  
  - Use quando precisar de controle total sobre a chave.

---

### 2. **Chaves Gerenciadas pela AWS**
- **O que são?**  
  Chaves criadas e gerenciadas pela AWS em sua conta, mas usadas apenas por serviços específicos da AWS.
- **Controle:**  
  - Visualização de metadados e políticas da chave.
  - **Sem controle** sobre rotação, exclusão ou políticas da chave.
- **Uso:**  
  - Apenas para serviços da AWS associados (ex: EBS, RDS).
  - Não pode ser usada diretamente por você.
- **Custos:**  
  - **Sem taxa mensal**.
  - Taxa por uso (alguns serviços cobrem esse custo).
- **Auditoria:**  
  - Uso da chave pode ser auditado via AWS CloudTrail.
- **Recomendação:**  
  - Use quando quiser criptografia gerenciada pela AWS sem custos mensais.

---

### 3. **Chaves de Propriedade da AWS**
- **O que são?**  
  Chaves criadas e gerenciadas pela AWS em uma conta da AWS, usadas para criptografar dados em várias contas.
- **Controle:**  
  - **Sem controle** sobre a chave (não é possível visualizar ou gerenciar).
  - Gerenciada totalmente pela AWS.
- **Uso:**  
  - Para criptografia padrão em serviços da AWS (ex: S3, DynamoDB).
  - Permite compartilhamento de dados entre contas e regiões.
- **Custos:**  
  - **Sem custos** para o cliente (não há taxas mensais ou por uso).
- **Auditoria:**  
  - **Sem auditoria** disponível para o cliente.
- **Recomendação:**  
  - Use quando a conveniência e a facilidade de uso forem mais importantes que o controle.

---

## Comparação entre os Tipos de Chaves

| Característica               | Chaves Gerenciadas pelo Cliente | Chaves Gerenciadas pela AWS | Chaves de Propriedade da AWS |
|------------------------------|---------------------------------|-----------------------------|------------------------------|
| **Controle sobre a chave**    | Total                           | Visualização apenas         | Nenhum                       |
| **Custos**                   | Taxa mensal + uso               | Sem taxa mensal, apenas uso | Sem custos                   |
| **Auditoria**                | Via CloudTrail                  | Via CloudTrail              | Não disponível               |
| **Rotação**                  | Opcional (configurável)         | Automática (anual)          | Gerenciada pelo serviço AWS  |
| **Compartilhamento entre contas** | Não                           | Não                         | Sim                          |

---

## Quando Usar Cada Tipo de Chave?

- **Chaves Gerenciadas pelo Cliente:**  
  - Quando você precisa de controle total sobre a chave.
  - Para cenários de conformidade ou auditoria rigorosa.

- **Chaves Gerenciadas pela AWS:**  
  - Quando você deseja criptografia gerenciada pela AWS sem custos mensais.
  - Para serviços específicos da AWS (ex: EBS, RDS).

- **Chaves de Propriedade da AWS:**  
  - Quando a conveniência e a facilidade de uso são prioridades.
  - Para criptografia padrão em serviços como S3 e DynamoDB.

---

## Próximos Passos
- **Crie uma Chave Gerenciada pelo Cliente:**  
  - Acesse o Console do AWS KMS e comece a gerenciar suas chaves.
- **Explore Serviços Integrados:**  
  - Verifique quais serviços da AWS suportam cada tipo de chave.
- **Consulte a Documentação Oficial:**  
  - Para mais detalhes, consulte a [documentação do AWS KMS](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html).

---

**Nota:** Escolha o tipo de chave com base no nível de controle, custos e requisitos de conformidade do seu projeto.
