# Dashboard — Taxas de Juros Consignado Público

Comparativo de taxas de juros para **crédito pessoal consignado público prefixado — Pessoa Física**, com dados diários do Banco Central do Brasil.

## Como funciona

- **Fonte dos dados:** API OData do Bacen (`TaxasJurosDiariaPorInicioPeriodo`)
- **Atualização automática:** toda segunda-feira às 08h (horário de Brasília) via GitHub Actions
- **Publicação:** GitHub Pages — o `index.html` é gerado pelo script e publicado automaticamente

## Instituições monitoradas

| Instituição | Categoria |
|---|---|
| Nubank (NU Financeira) | Fintech |
| Sicredi | Cooperativa (à frente do Nubank) |
| Banco Arbi | Nicho (à frente do Nubank) |
| Banco Inter | Fintech (à frente do Nubank) |
| BancoSeguro | Nicho (à frente do Nubank) |
| Caixa Econômica Federal | Banco tradicional |
| Itaú Unibanco | Banco tradicional |
| Banco do Brasil | Banco tradicional |

## Estrutura do repositório

```
├── index.html              # Dashboard gerado automaticamente
├── update.py               # Script Python que busca dados e gera o HTML
├── .github/
│   └── workflows/
│       └── update.yml      # Workflow do GitHub Actions
└── README.md
```

## Como rodar localmente

```bash
python update.py
# Abre o index.html no navegador
```

Não há dependências externas — o script usa apenas a biblioteca padrão do Python 3.

## Atualização manual

Na aba **Actions** do repositório, clique em **"Atualizar dashboard de taxas"** → **"Run workflow"**.
