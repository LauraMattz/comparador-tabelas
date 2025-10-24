# 🔍 Comparador Profissional de Tabelas

## 📋 Descrição

Sistema completo para comparação inteligente de duas tabelas/datasets, identificando automaticamente:
- ✅ Registros novos (INSERT)
- 🔄 Registros alterados (UPDATE) 
- ❌ Registros removidos (DELETE)
- 📊 Análise detalhada campo por campo
- 📈 Visualizações e relatórios automáticos

  * Todos os dados aqui são FAKES!

## 🚀 Funcionalidades

### 1. Identificação Automática
- Detecta novos registros baseado em chave primária
- Identifica registros removidos
- Compara registros comuns campo por campo

### 2. Análise Detalhada
- Mostra valor antigo vs valor novo
- Conta mudanças por campo
- Identifica registros mais alterados
- Calcula taxa de mudança

### 3. Visualizações
- 📊 Gráfico de mudanças por campo
- 🥧 Distribuição geral (novos/alterados/removidos)
- 📈 Top 10 registros mais alterados
- 📋 Dashboard de estatísticas

### 4. Exportação
- CSV com novos registros
- CSV com todas as mudanças detectadas
- CSV com registros removidos
- Gráficos em alta resolução (PNG)
- Relatórios com timestamp

## 📁 Estrutura do Projeto

```
comparador_tabelas/
│
├── dados_originais.csv          # Tabela original (versão antiga)
├── dados_atualizados.csv        # Tabela atualizada (versão nova)
├── comparador_tabelas.ipynb     # Notebook principal
├── POST_LINKEDIN.md             # 4 versões de post para LinkedIn
├── README.md                    # Este arquivo
│
└── [Gerados automaticamente]
    ├── registros_novos_*.csv
    ├── mudancas_detectadas_*.csv
    ├── registros_removidos_*.csv
    └── comparacao_tabelas.png
```

## 🛠️ Tecnologias Utilizadas

- **Python 3.8+**
- **Pandas**: Manipulação de dados
- **NumPy**: Operações numéricas
- **Matplotlib**: Visualizações
- **Seaborn**: Gráficos estatísticos
- **Jupyter Notebook**: Ambiente interativo

## 📦 Instalação

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/comparador-tabelas.git
cd comparador-tabelas

# Instale as dependências
pip install pandas numpy matplotlib seaborn jupyter

# Inicie o Jupyter
jupyter notebook comparador_tabelas.ipynb
```

## 🎮 Como Usar

### Passo 1: Preparar seus dados
Coloque seus arquivos CSV na pasta:
- `dados_originais.csv` (versão antiga)
- `dados_atualizados.csv` (versão nova)

### Passo 2: Executar o notebook
1. Abra `comparador_tabelas.ipynb`
2. Execute todas as células (Run All)
3. Aguarde a análise completa

### Passo 3: Revisar resultados
- Veja o resumo executivo no final
- Analise os gráficos gerados
- Revise o relatório detalhado

### Passo 4: Exportar dados
Os resultados são salvos automaticamente:
- CSVs com timestamp
- Gráficos em PNG
- Prontos para compartilhar!

## 📊 Exemplo de Uso

### Entrada
```
dados_originais.csv: 15 registros
dados_atualizados.csv: 17 registros
```

### Saída
```
🟢 Novos registros: 2
🔄 Registros alterados: 6
❌ Registros removidos: 0
📊 Total de mudanças: 11 campos
```

### Mudanças Detectadas
| ID | Nome | Campo | Valor Antigo | Valor Novo |
|----|------|-------|--------------|------------|
| 1 | Ana Silva | cargo | Analista de Dados | Analista Sênior de Dados |
| 1 | Ana Silva | salario | R$ 8.500,00 | R$ 9.500,00 |
| 4 | Daniel Oliveira | cargo | Cientista de Dados | Cientista de Dados Sênior |
| 4 | Daniel Oliveira | salario | R$ 14.000,00 | R$ 16.500,00 |

## 📈 Métricas e Estatísticas

O notebook gera automaticamente:
- **Taxa de mudança**: % de campos alterados
- **Campo mais alterado**: Qual coluna sofreu mais mudanças
- **Registros mais afetados**: Top 10 com mais alterações
- **Distribuição de mudanças**: Visualização da proporção de cada tipo

## 🔒 Boas Práticas

1. **Sempre faça backup** antes de aplicar mudanças
2. **Revise o relatório** antes de executar UPDATEs
3. **Mantenha consistência** na chave primária
4. **Documente** as razões das mudanças
5. **Versione** suas tabelas com timestamp

## 🐛 Troubleshooting

### Erro: "Chave primária não encontrada"
**Solução**: Verifique se ambas as tabelas têm a coluna especificada em `chave_primaria`

### Erro: "Colunas incompatíveis"
**Solução**: Garanta que ambas as tabelas tenham as mesmas colunas (ou ajuste o código para lidar com colunas diferentes)

### Muitas mudanças detectadas
**Solução**: Verifique se há problemas de formatação (espaços, maiúsculas) nos dados

## 📚 Recursos Adicionais

- [Documentação Pandas](https://pandas.pydata.org/docs/)
- [Guia Matplotlib](https://matplotlib.org/stable/tutorials/index.html)
- [Exemplos Seaborn](https://seaborn.pydata.org/examples/index.html)

## 🤝 Contribuindo

Contribuições são bem-vindas! Para contribuir:

1. Fork o projeto
2. Crie uma branch (`git checkout -b feature/MinhaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona MinhaFeature'`)
4. Push para a branch (`git push origin feature/MinhaFeature`)
5. Abra um Pull Request

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
