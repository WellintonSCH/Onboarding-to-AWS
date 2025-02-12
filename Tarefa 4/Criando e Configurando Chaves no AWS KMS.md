# Criando e Configurando Chaves no AWS KMS

O **AWS Key Management Service (KMS)** permite criar e gerenciar chaves de criptografia para proteger seus dados. Este guia explica como criar chaves KMS, escolher o tipo de chave e configurar suas propriedades.

---

## Como Criar uma Chave KMS

### Métodos de Criação:
1. **AWS Management Console**:  
   - Interface gráfica para criar e gerenciar chaves.
2. **API `CreateKey`**:  
   - Usando a API do AWS KMS para criar chaves programaticamente.
3. **AWS CloudFormation**:  
   - Usando o recurso `AWS::KMS::Key` para criar chaves como parte de uma infraestrutura como código.

---

## Propriedades das Chaves KMS

### 1. **Tipo de Chave**
- **Chaves Simétricas (AES-256)**:  
  - Usadas para criptografia e descriptografia de dados.
  - Recomendadas para a maioria dos casos de uso.
- **Chaves Assimétricas (RSA, ECC, SM2)**:  
  - Usadas para criptografia, assinatura e verificação.
  - Úteis para cenários que exigem compartilhamento de chaves públicas.
- **Chaves HMAC**:  
  - Usadas para gerar e verificar códigos de autenticação de mensagens (HMAC).

### 2. **Uso da Chave**
- Define as operações que a chave pode realizar:
  - **ENCRYPT_DECRYPT**: Para criptografia e descriptografia.
  - **SIGN_VERIFY**: Para assinar e verificar mensagens.
  - **GENERATE_VERIFY_MAC**: Para operações HMAC.
  - **KEY_AGREEMENT**: Para derivação de segredos compartilhados.

### 3. **Especificação da Chave (Key Spec)**
- Define a configuração criptográfica da chave:
  - **SYMMETRIC_DEFAULT**: Chave simétrica AES-256 (padrão).
  - **RSA_2048**, **ECC_NIST_P256**, etc.: Para chaves assimétricas.
  - **HMAC_256**: Para chaves HMAC.

### 4. **Origem do Material da Chave**
- Define de onde o material da chave é gerado:
  - **AWS_KMS**: Material gerado pelo AWS KMS (padrão).
  - **EXTERNAL**: Material de chave importado por você.
  - **AWS_CLOUDHSM**: Material gerado em um HSM do AWS CloudHSM.
  - **EXTERNAL_KEY_STORE**: Material armazenado em um repositório externo.

---

## Passo a Passo para Criar uma Chave KMS

### 1. **Defina a Política de Chave**
- A política de chave controla quem pode gerenciar e usar a chave.
- Você pode definir a política durante a criação ou alterá-la posteriormente.

### 2. **Escolha o Tipo de Chave**
- Selecione o tipo de chave com base no seu caso de uso:
  - **Simétrica**: Para criptografia geral.
  - **Assimétrica**: Para assinatura ou criptografia com chave pública.
  - **HMAC**: Para autenticação de mensagens.

### 3. **Configure o Uso da Chave**
- Escolha o uso da chave (ex: `ENCRYPT_DECRYPT`, `SIGN_VERIFY`).

### 4. **Defina a Especificação da Chave**
- Escolha a especificação da chave (ex: `SYMMETRIC_DEFAULT`, `RSA_2048`).

### 5. **Escolha a Origem do Material da Chave**
- Decida se o material da chave será gerado pelo AWS KMS, importado ou armazenado externamente.

### 6. **Crie a Chave**
- No Console, API ou CloudFormation, finalize a criação da chave.

---

## Permissões Necessárias
Para criar uma chave KMS, você precisa das seguintes permissões:
- **kms:CreateKey**: Para criar a chave.
- **kms:CreateAlias**: Para criar um alias (opcional, mas recomendado).
- **kms:TagResource**: Para adicionar tags à chave.
- **kms:PutKeyPolicy**: Para definir a política de chave inicial.

---

## Considerações Importantes
- **Imutabilidade**:  
  - Após a criação, o tipo de chave, uso e origem do material **não podem ser alterados**.
- **Custos**:  
  - Chaves gerenciadas pelo cliente têm uma **taxa mensal** e custos por uso.
  - Chaves gerenciadas pela AWS e de propriedade da AWS são **gratuitas** (exceto por custos de uso em alguns casos).
- **Auditoria**:  
  - Use o **AWS CloudTrail** para auditar o uso das chaves.

---

## Casos de Uso Comuns

### 1. **Criptografia de Dados**
- Use chaves simétricas para criptografar dados em repouso ou em trânsito.
- Exemplo: Criptografia de volumes EBS ou objetos S3.

### 2. **Assinatura e Verificação**
- Use chaves assimétricas para assinar e verificar mensagens.
- Exemplo: Assinatura de certificados digitais.

### 3. **Autenticação de Mensagens (HMAC)**
- Use chaves HMAC para gerar e verificar códigos de autenticação.
- Exemplo: Validação de integridade de dados.

### 4. **Derivação de Segredos Compartilhados**
- Use chaves de curva elíptica para derivar segredos compartilhados.
- Exemplo: Estabelecimento de chaves simétricas entre duas partes.

---

**Nota:** Escolha o tipo de chave e as configurações com base nos requisitos de segurança e uso do seu projeto.
