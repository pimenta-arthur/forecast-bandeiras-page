# Projeção de Bandeiras Tarifárias · página pública

Site estático com a projeção da bandeira tarifária mensal (probabilidade de cada cor de M+1 a M+6, GSF e
PLD gatilho nos cenários esperado, seco e úmido, histórico das rodadas e desempenho do modelo).

**Página:** https://pimenta-arthur.github.io/forecast-bandeiras-page/

Este repositório guarda só a página pronta (HTML, CSS e dados de resultado). Não tem código do modelo nem
dados brutos: ela é gerada pela aplicação Quant Energia e copiada para cá a cada rodada publicada.

## Atualizar depois de uma rodada nova

Na pasta da aplicação (`quant-energia-app`), depois de `qe forecast_bandeiras publicar`:

```bash
uv run qe forecast_bandeiras exportar --destino ../forecast-bandeiras-page
cd ../forecast-bandeiras-page
git add -A && git commit -m "Rodada de <data>" && git push
```

O GitHub Pages publica a versão nova em um ou dois minutos.

## Conteúdo

```
index.html              projeções (página principal)
metodologia.html        metodologia do modelo
padrao/                 padrão visual (base.css, painel.css)
dados/produto_dados.js  dados da última rodada publicada
```
