# Anonimização de Dados e LGPD

Este repositório contém um estudo completo sobre **anonimização de dados pessoais conforme a Lei Geral de Proteção de Dados (LGPD)** do Brasil.

## Descrição

Projeto educacional que demonstra como utilizar dados sensíveis em análise de dados, predições e classificações sem desrespeitar a LGPD, utilizando técnicas de anonimização e pseudonimização.

## Conteúdo

### Arquivos Principais
- **`Anonimizacao_Dados_LGPD.ipynb`**: Notebook Jupyter completo com teoria e implementação prática

### Material de Apoio
A pasta `material-apoio/` contém documentos referenciais:
- Guia para Técnicas Básicas de Anonimização de Dados (LGPD)
- Técnicas de Implementação de Anonimização de Dados (Worktec)
- Mitigação dos Riscos à Privacidade
- Data Privacy: De-identification Paper (ISSA)

## Pré-requisitos

### Bibliotecas Python Necessárias
```bash
pip install pandas numpy matplotlib
```

### Versão Python
Python 3.7 ou superior

## Como Usar

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/anonimizacao.git
cd anonimizacao
```

2. Abra o notebook no Jupyter:
```bash
jupyter notebook Anonimizacao_Dados_LGPD.ipynb
```

3. Execute as células do notebook para ver as técnicas em ação

## Técnicas Implementadas

### 1. Supressão e Pseudonimização
- Remove campos diretamente identificadores (nome, CPF, email, telefone)
- Substitui identidades por IDs únicos pseudonimizados
- Preserva valores exatos dos atributos para análise estatística

**Uso ideal**: Análise estatística que requer valores exatos mas sem identificação direta

### 2. Generalização e Mascaramento
- Converte valores específicos em categorias amplas (idade em faixas, salário em categorias)
- Mascara parte dos dados sensíveis (CPF, email)
- Generaliza localização geográfica (cidades para regiões)

**Uso ideal**: Análise categórica onde padrões são mais importantes que valores específicos

### 3. Hashing e Randomização
- Aplica funções hash criptográficas (SHA-256) para identidades
- Adiciona ruído aleatório aos dados numéricos (±3 anos para idade, ±5% para salário)
- Preserva integridade referencial enquanto protege privacidade

**Uso ideal**: Análises que precisam manter vínculos entre dados mas com proteção adicional

## Características do Dataset

O notebook cria e anonimiza um dataset com **100 registros** contendo:
- Dados identificadores: nome, CPF, email, telefone, data de nascimento
- Dados sensíveis: idade, salário, localização, gênero, informações de saúde
- Dados demográficos: cidade, estado, CEP

## Objetivos de Aprendizado

- Entender os requisitos da LGPD para anonimização de dados
- Aprender as principais técnicas de anonimização
- Implementar técnicas práticas em Python
- Avaliar trade-offs entre privacidade e utilidade dos dados
- Preservar análise estatística após anonimização

## Aspectos Legais da LGPD

### Artigos Relevantes
- **Art. 12**: Direito de acesso aos dados pessoais
- **Art. 18**: Direito de portabilidade e eliminação
- **Art. 46**: Anonimização como técnica de proteção
- **Art. 7**: Bases legais para tratamento de dados
- **Art. 13**: Informação ao titular sobre o tratamento

## Privacidade e Segurança

### Limitações e Cuidados
- K-Anonimidade com k=5 pode não ser suficiente contra adversários sofisticados
- Ataques de ligação podem reidentificar dados usando informações auxiliares
- Trade-off entre utilidade dos dados e nível de anonimização
- Reidentificação através de técnicas avançadas de machine learning
- Dados podem ser reidentificados quando novos datasets são publicados

### Boas Práticas
1. Escolha a técnica apropriada para o caso de uso
2. Teste K-Anonimidade com k≥5 para atributos quasi-identificadores
3. Combine múltiplas técnicas para maior proteção
4. Realize auditoria regular da eficácia da anonimização
5. Documente todas as técnicas aplicadas
6. Realize testes de reidentificação
7. Minimize coleta de dados - colete apenas o necessário

## Ferramentas Recomendadas

### Para Produção
1. **ARX**: Ferramenta de código aberto para anonimização de dados
2. **IBM Guardian**: Solução empresarial para proteção de dados
3. **Google TensorFlow Privacy**: Framework para privacidade diferencial

### Bibliotecas Python
- **anonymization-library**: Biblioteca Python para anonimização
- **text-anonymizer**: Específico para anonimização de texto
- **pandas**: Manipulação de dados
- **numpy**: Operações numéricas

## Casos de Uso

As técnicas apresentadas podem ser aplicadas em:
- Análise de dados de saúde
- Pesquisa acadêmica
- Marketing de dados agregados
- Machine Learning com dados sensíveis
- Relatórios de compliance
- Business Intelligence
- Analytics de clientes

## Estrutura do Notebook

1. **Introdução à LGPD**
   - Conceitos fundamentais
   - Diferença entre anonimização e pseudonimização

2. **Como Usar Dados Sensíveis**
   - Vantagens da anonimização
   - Abordagens principais

3. **Principais Técnicas de Anonimização**
   - Lista completa de 10 técnicas
   - Exemplos práticos

4. **Implementação Prática**
   - Criação de dataset com dados sensíveis
   - 3 técnicas implementadas com código
   - Comparação e análise

5. **Visualização e Análise**
   - Gráficos comparativos
   - Análise estatística preservada
   - Exportação de resultados

6. **Considerações Finais**
   - Benefícios e limitações
   - Boas práticas
   - Aspectos legais
   - Próximos passos