# AWS Cost Explorer

O **AWS Cost Explorer** é uma ferramenta poderosa para visualizar, analisar e prever seus custos e uso na AWS. Ele oferece insights detalhados sobre seus gastos e ajuda a identificar tendências e oportunidades de otimização.

---

## Principais Funcionalidades
1. **Visualização de Custos e Uso**:
   - Gráficos e relatórios interativos.
   - Dados dos últimos **13 meses** e previsões para os próximos **12 meses**.

2. **Recomendações de Instâncias Reservadas (RIs)**:
   - Sugestões personalizadas para compra de RIs com base no seu uso.

3. **Relatórios Pré-configurados**:
   - Visualizações rápidas de tendências de custos.
   - Personalização de relatórios para atender às suas necessidades.

4. **Acesso Programático**:
   - Use a **API do Cost Explorer** para acessar dados de custos programaticamente.
   - Custo de **$0,01 por solicitação paginada**.

---

## Como Funciona o Cost Explorer?
- **Preparação dos Dados**:
   - Quando você se inscreve, a AWS prepara dados do mês atual, dos últimos 13 meses e uma previsão para os próximos 12 meses.
   - Dados do mês atual ficam disponíveis em **24 horas**; o restante pode levar alguns dias.

- **Atualizações**:
   - Os dados são atualizados pelo menos **uma vez a cada 24 horas**.
   - Depende dos dados upstream dos aplicativos de cobrança.

- **Interface do Usuário**:
   - Gráficos interativos e relatórios detalhados.
   - Exportação de dados em formato **CSV** para análise offline.

---

## Como Usar o Cost Explorer

### Passo a Passo:
1. **Acesse o Console do Cost Explorer**:
   - No Console da AWS, procure por **Cost Explorer**.

2. **Explore os Dados**:
   - Use o gráfico principal para visualizar tendências de custos.
   - Acesse relatórios pré-configurados ou crie visualizações personalizadas.

3. **Analise Recomendações de RIs**:
   - Verifique as sugestões de compra de Instâncias Reservadas para reduzir custos.

4. **Exporte Dados**:
   - Baixe relatórios em formato CSV para análise detalhada.

5. **Use a API (Opcional)**:
   - Integre o Cost Explorer com suas ferramentas internas usando a API.

---

## Vantagens do Cost Explorer
- **Gratuito para Uso na Interface do Usuário**:  
   - Visualização de custos e uso sem custo adicional.
- **Previsões de Custos**:  
   - Planeje seus gastos futuros com base em previsões precisas.
- **Identificação de Tendências**:  
   - Detecte padrões de uso e áreas para otimização.
- **Integração com Outras Ferramentas**:  
   - Use a API para automatizar análises de custos.

---

## Considerações Importantes
- **Não Pode Ser Desabilitado**:  
   - Uma vez habilitado, o Cost Explorer não pode ser desativado.
- **Atraso nos Dados**:  
   - Pode haver um atraso de até 24 horas na atualização dos dados.
- **Custo da API**:  
   - Cada solicitação paginada da API custa **$0,01**.

---

Para mais detalhes, consulte a [documentação oficial do AWS Cost Explorer](https://docs.aws.amazon.com/cost-management/latest/userguide/ce-what-is.html).
