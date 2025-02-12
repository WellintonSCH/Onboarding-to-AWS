
# Tutorial: Habilitar o IAM Identity Center na AWS

Este guia explica como habilitar o **IAM Identity Center** na AWS, uma ferramenta para gerenciar acesso centralizado a múltiplas contas e aplicativos.

---

## O que é o IAM Identity Center?
O IAM Identity Center (antigo AWS SSO) permite gerenciar permissões e atribuições de aplicativos em várias contas da AWS. Ele oferece dois tipos de instâncias:

1. **Instância de Organização** (recomendado):  
   - Usada para gerenciar permissões em várias contas da organização AWS.
   - Disponível apenas na **conta de gerenciamento** da organização.

2. **Instância de Conta**:  
   - Usada para gerenciar permissões em uma única conta (membro ou autônoma).

---

## Pré-requisitos
- Uma conta da AWS.
- Se usar uma **instância de organização**, a conta deve ser a **conta de gerenciamento** da organização.
- Permissões administrativas na conta.

---

## Passo a Passo para Habilitar o IAM Identity Center

### 1. Escolha o Tipo de Instância
- **Instância de Organização** (recomendado):  
  - Use se você gerencia múltiplas contas na organização AWS.
- **Instância de Conta**:  
  - Use se você gerencia apenas uma conta.

### 2. Faça Login no Console da AWS
- **Novo na AWS**: Entre como **usuário root** usando o e-mail e senha da conta.
- **Conta Autônoma**: Entre com credenciais IAM com permissões administrativas.
- **Organização AWS**: Entre com credenciais da **conta de gerenciamento**.

### 3. Acesse o Console do IAM Identity Center
- No Console da AWS, procure por **IAM Identity Center**.
- Clique em **Habilitar**.

### 4. Revise e Confirme
- Na página **Habilitar IAM Identity Center com Organizações da AWS**, revise as informações.
- Clique em **Habilitar** para concluir.

---

## Observações Importantes
- O IAM Identity Center só pode ser habilitado em **uma região da AWS** por organização.
- Para mudar a região, você precisará **excluir a instância atual** e criar uma nova na região desejada.

---

## Configurações Adicionais
Após habilitar, recomendamos:
1. **Confirmar a Fonte de Identidade**:  
   - Use uma fonte de identidade existente (ex: AWS Identity Store ou Microsoft Active Directory).
2. **Registrar um Administrador Delegado**:  
   - Delegue a administração para uma conta de membro da organização.
3. **Configurar Firewalls e Gateways**:  
   - Permita o acesso ao portal do IAM Identity Center em firewalls ou gateways.

---

## Próximos Passos
- Configure usuários e grupos no IAM Identity Center.
- Atribua permissões a contas e aplicativos.

Para mais detalhes, consulte a [documentação oficial da AWS](https://docs.aws.amazon.com/singlesignon/latest/userguide/).

---

**Nota:** Este tutorial é baseado nas melhores práticas da AWS e pode ser atualizado conforme novas funcionalidades são lançadas.
