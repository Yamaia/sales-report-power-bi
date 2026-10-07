# 📈 Sales Report com Power BI

Relatório de vendas em Power BI, desenvolvido a partir dos arquivos de exemplo do desafio: modelo de dados, medidas DAX, visuais interativos e publicação no Power BI Service.

Desenvolvido como desafio de projeto da [DIO](https://www.dio.me/).

## 🎯 Objetivo

Analisar os arquivos de exemplo (`Exemplo.pbix` e `Sales Report.pbix`), replicar o relatório e evoluí-lo com novos indicadores, visuais e interações.

## 🗂️ Estrutura do repositório

```
├── arquivos-originais/
│   ├── Exemplo.pbix
│   └── Sales Report.pbix
├── relatorio/
│   └── sales-report-yamaia.pbix     # Versão desenvolvida por mim
├── imagens/
│   ├── pagina-1.png
│   └── pagina-2.png
└── README.md
```

## 🛠️ Etapas do projeto

1. **Análise dos arquivos de exemplo:** abrir os `.pbix` no Power BI Desktop e estudar o modelo, as medidas e os visuais
2. **Replicação:** reproduzir as páginas do relatório de exemplo
3. **Evolução:** adicionar melhorias próprias (novos indicadores, filtros, navegação)
4. **Revisão:** nomear visuais, organizar o layout e revisar as dicas de ferramenta
5. **Publicação:** publicar no Power BI Service

## 📊 Conteúdo do relatório

| Elemento | Descrição |
|---|---|
| Cartões | Total de Vendas, Lucro, Quantidade, Margem % |
| Gráficos de colunas e linhas | Vendas por período |
| Gráficos de barras | Vendas por produto, categoria ou região |
| Mapa | Vendas por país/estado |
| Segmentadores | Ano, Categoria, Região |
| Navegação | Botões entre páginas |

> Ajuste a tabela para refletir exatamente o que está no relatório entregue.

## 🧮 Medidas DAX

```DAX
Total Vendas = SUM(Vendas[Valor])

Quantidade Vendida = SUM(Vendas[Quantidade])

Lucro = SUM(Vendas[Valor]) - SUM(Vendas[Custo])

Margem % = DIVIDE([Lucro], [Total Vendas])

Vendas Ano Anterior =
CALCULATE([Total Vendas], SAMEPERIODLASTYEAR('Calendário'[Date]))

Variação % = DIVIDE([Total Vendas] - [Vendas Ano Anterior], [Vendas Ano Anterior])
```

> Troque `Vendas[...]` pelos nomes reais de tabelas e colunas do modelo.

## 🖼️ Prints

![Página 1](imagens/pagina-1.png)
![Página 2](imagens/pagina-2.png)

## 🌐 Relatório publicado

🔗 [Acessar no Power BI Service](COLE_AQUI_O_LINK)

## 💡 Aprendizados

- Leitura e engenharia reversa de relatórios existentes
- Organização de modelo, medidas e layout
- Criação de visuais interativos e navegação
- Publicação e compartilhamento no Power BI Service

## 👤 Autor

**Yamaia** — desenvolvedor focado em backend, cloud e arquitetura de soluções.

[GitHub](https://github.com/SEU_USUARIO) · [LinkedIn](https://linkedin.com/in/SEU_PERFIL)
