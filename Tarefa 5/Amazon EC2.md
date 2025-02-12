# Amazon EC2: Computação Escalável na Nuvem AWS

O **Amazon Elastic Compute Cloud (Amazon EC2)** é um serviço da AWS que fornece capacidade de computação escalável e sob demanda na nuvem. Com o EC2, você pode reduzir custos de hardware, implantar aplicativos rapidamente e gerenciar servidores virtuais de forma flexível.

---

## **O que é o Amazon EC2?**

O EC2 permite criar e gerenciar **instâncias** (servidores virtuais) na nuvem AWS. Você pode escalar a capacidade conforme necessário, adicionando ou removendo instâncias para lidar com picos de tráfego ou tarefas de computação intensiva.

---

## **Principais Recursos do EC2**

### 1. **Instâncias**
   - Servidores virtuais com diferentes configurações de CPU, memória, armazenamento e rede.
   - Escolha entre diversos **tipos de instância** para atender às suas necessidades.

### 2. **AMIs (Amazon Machine Images)**
   - Modelos pré-configurados com sistema operacional e software para inicializar instâncias.

### 3. **Armazenamento**
   - **Amazon EBS**: Volumes de armazenamento persistentes para dados.
   - **Armazenamento de Instância**: Armazenamento temporário excluído ao parar a instância.

### 4. **Segurança**
   - **Pares de Chaves**: Credenciais seguras para acessar instâncias.
   - **Grupos de Segurança**: Firewalls virtuais para controlar o tráfego de rede.

### 5. **Integração com Outros Serviços**
   - **Auto Scaling**: Ajuste automático do número de instâncias com base na demanda.
   - **Elastic Load Balancing**: Distribuição de tráfego entre várias instâncias.
   - **Amazon CloudWatch**: Monitoramento de desempenho e uso de instâncias.

---

## **Casos de Uso Comuns**

1. **Hospedagem de Aplicativos Web**:
   - Use instâncias EC2 para hospedar sites e aplicativos web.

2. **Processamento de Dados**:
   - Execute tarefas de computação intensiva, como análise de big data.

3. **Ambientes de Desenvolvimento e Testes**:
   - Crie ambientes temporários para desenvolvimento e testes.

4. **Backup e Recuperação de Desastres**:
   - Use instâncias EC2 para backups e planos de recuperação.

---

##  **Serviços Relacionados**

- **Amazon Lightsail**: Para projetos simples com custo previsível.
- **Amazon ECS/EKS**: Para execução de aplicativos em contêineres.
- **AWS Backup**: Para automatizar backups de instâncias EC2.

---

## **Como Começar**

1. **Crie uma Instância EC2**:
   - No Console da AWS, acesse **EC2** > **Launch Instance**.
   - Escolha uma AMI e um tipo de instância.
   - Configure segurança, armazenamento e rede.

2. **Conecte-se à Instância**:
   - Use um par de chaves SSH para acessar sua instância.

3. **Monitore e Escale**:
   - Use **Auto Scaling** e **CloudWatch** para gerenciar o desempenho.

---

Este repositório é para fins educacionais. Consulte a [documentação oficial da AWS](https://docs.aws.amazon.com/ec2/) para mais detalhes.

---

**Desenvolvido por Wellinton Schweitzer como parte da disciplina de Introdução ao Big Data e Data Analysis.**
