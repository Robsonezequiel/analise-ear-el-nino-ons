# Análise de Risco Hídrico e El Niño (2025-2026)

## Sobre o Projeto
Este projeto tem como objetivo avaliar o impacto do fenômeno climático El Niño nos níveis de Energia Armazenada (EAR) do Operador Nacional do Sistema Elétrico (ONS), comparando os dados diários dos anos de 2025 e 2026.

## Problema de Negócio
O setor elétrico brasileiro é altamente dependente da hidrologia. Com a intensificação de eventos climáticos extremos, compreender como a variabilidade climática afeta o armazenamento de água nos reservatórios é fundamental para a segurança energética do país.

## Metodologia e Ferramentas
- **Linguagem:** Python 3.12
- **Ambiente:** VS Code com ambiente virtual (`.venv`)
- **Bibliotecas:** Pandas, Matplotlib, Seaborn, SciPy.
- **ETL:** Extração e união dos dados brutos (CSV) do ONS, tratamento de datas e criação de features (dia do ano).
- **Análise:** Estatística descritiva, Teste T de Student para validação de hipóteses.

## Principais Insights e Impacto do El Niño
A análise comparativa (2026 vs 2025) revela um comportamento heterogêneo entre os subsistemas, evidenciando como a variabilidade climática afeta o território de formas distintas:

- **Nordeste:** O salto expressivo de +17,23% no armazenamento médio sugere um regime de chuvas fora do padrão histórico em 2026. Este comportamento é consistente com eventos de El Niño, que frequentemente alteram a Zona de Convergência Intertropical (ZCIT), podendo provocar chuvas intensas na região.
- **Norte (-9,04%):** A maior retração relativa indica um ano de estiagem mais severa. O El Niño costuma inibir a formação de chuvas na Amazônia, o que se refletiu diretamente na queda de energia armazenada nas usinas da região.
- **Sudeste (-1,29%):** A estabilidade do principal subsistema do país sugere que as chuvas de verão ocorreram dentro da normalidade, amortecendo os efeitos do El Niño nos reservatórios centrais.
- **Sul (-5,67%):** Apesar de o Sul ser a região mais comumente afetada por chuvas extremas em anos de El Niño (inundações), a média de armazenamento em 2026 foi menor que em 2025. Isso indica que as chuvas podem ter sido torrenciais e pontuais (gerando picos), mas com baixo volume de retenção a longo prazo.

## Estrutura do Repositório
- `DATA/RAW/`: Arquivos CSV originais do ONS.
- `notebooks/`: Notebook com a análise exploratória, engenharia de atributos e testes estatísticos.
- `README.md`: Documentação do projeto.

## Como Executar
1. Clone o repositório.
2. Crie e ative um ambiente virtual: `python -m venv .venv` e `source .venv/bin/activate`.
3. Instale as dependências: `pip install pandas matplotlib seaborn scipy`.
4. Execute o notebook `01_exploracao_dados.ipynb`.