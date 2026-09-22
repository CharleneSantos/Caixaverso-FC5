<h1> Campeonato Brasileiro – Análise de Dados</h1>

<p>Este projeto tem como objetivo explorar, analisar e visualizar dados históricos do <strong>Campeonato Brasileiro de Futebol</strong>, utilizando datasets públicos disponibilizados no Kaggle.</p>

<p>A aplicação carrega duas bases principais:</p>

<ul>
  <li><strong>campeonato-brasileiro-estatisticas-full.csv</strong> — Estatísticas detalhadas de partidas, jogadores e eventos.</li>
  <li><strong>campeonato-brasileiro-full.csv</strong> — Informações completas sobre jogos, rodadas, clubes e resultados.</li>
</ul>

<hr>

<h2> Estrutura do Projeto</h2>

<pre>
├── arquivos/
│   ├── campeonato-brasileiro-estatisticas-full.csv
│   └── campeonato-brasileiro-full.csv
├── notebooks/
│   └── analise_campeonato.ipynb
├── dicionario_dados.ipynb
├── README.md
└── requirements.txt
</pre>

<hr>

<h2> Dependências</h2>

<p>As principais bibliotecas utilizadas são:</p>

<ul>
  <li>pandas</li>
  <li>kagglehub</li>
  <li>numpy</li>
  <li>matplotlib.pyplot</li>
  <li>seaborn</li>
  <li>scipy.stats </li>
</ul>

<p>Instalação:</p>

<pre><code>pip install -r requirements.txt
</code></pre>

<hr>

<h2>Carregando os Dados</h2>

<p>O projeto utiliza o <code>kagglehub</code> para baixar automaticamente os datasets do Kaggle:</p>

<pre><code>estatisticas = "campeonato-brasileiro-estatisticas-full.csv"
full = "campeonato-brasileiro-full.csv"

df_estatisticas = kagglehub.dataset_load(
    KaggleDatasetAdapter.PANDAS,
    "adaoduque/campeonato-brasileiro-de-futebol",
    estatisticas,
)

df_full = kagglehub.dataset_load(
    KaggleDatasetAdapter.PANDAS,
    "adaoduque/campeonato-brasileiro-de-futebol",
    full,
)

pd.set_option('display.max_columns', None)
</code></pre>

<hr>

<h2> Objetivos da Análise</h2>

<h3> Responder àas perguntas:</h3>
<ul >
    <li>Qual é a eficiência ofensiva dos clubes?</li>
    <li>A eficiência ofensiva influencia no ganho de pontos?</li>
    <li>A formação tática influencia a eficiência ofensiva das equipes? Existe uma formação com mais vitórias?</li>
    <li>Os campeões brasileiros apresentam um perfil estatístico diferente das demais equipes?</li>
    <li>Qual time consegue produzir mais gols a cada 100 passes realizados?</li>
</ul>


<hr>

<h2> Resultados Esperados</h2>

<ul>
  <li>Gráficos de desempenho</li>
  <li>Tabelas comparativas</li>
  <li>Insights sobre desempenho</li>
  <li>Rankings por estatísticas</li>
</ul>

<hr>

<h2> Dataset Original</h2>

<p>Dados fornecidos por:<br>
<strong>Kaggle – adaoduque/campeonato-brasileiro-de-futebol</strong></p>





