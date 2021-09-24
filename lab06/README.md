# Lab06 - Artigo de Dataset Público

Estrutura de pastas:

~~~
├── README.md  <- arquivo apresentando a tarefa
│
└── images     <- arquivos de imagem usados na tarefa (se houver)
~~~

# Aluno
* 231551: Antonio Gabriel da Silva Fernandes

# Análise do Artigo "Três Datasets criados a partir de um banco de Canções Populares Brasileiras de Sucesso e Não-Sucesso de 2014 a 2019."

| campo | valor |
|------------|----------------------------------------|
| referência | Bertoni, A. A. e Lemos, R. P. (2021). Três Datasets criados a partir de um banco de Canções Populares Brasileiras de Sucesso e Não-Sucesso de 2014 a 2019.|
| link       | [PDF do artigo](https://drive.google.com/file/d/1-uZG7J4yafFAHvM7QlZDoWoemMTq3VQB/view) |
| dataset | [Repositório no Github](https://github.com/tocaestudio/SBBD-2021) |
| formato | CSV |

## Resumo
O trabalho tem como objetivo a criação de datasets com dados de canções brasileiras de sucesso e não-sucesso entre os anos de 2014 a 2019. Sâo selecionadas as canções mais tocadas em rádios nesses anos, constituindo o conjunto de músicas de sucesso, e depois são selecionadas aleatoriamente canções que, embora sejam dos mesmos artistas, não estão entre as mais tocadas, consituindo o conjunto de músicas de não-sucesso. É feita uma análise para determinar qual trecho das músicas deve ser analisado para minimizar repetição desnecessária, chegando a conclusão de que é preciso levar em consideração em média os primeiros 90 segundos. Dessa forma, os 90 segundos iniciais dessas canções são submetidos a programas de análise de áudio para a extração de informações, que são tratadas e organizadas em uma tabela, sendo esse o primeiro dataset do trabalho.

Depois, esses trechos das canções são analisados de forma a extrair a melodia da voz principal ao longo do tempo, gerando um gráfico de frequência por tempo. Essas sequências temporais de frequências, para cada canção, constituem o segundo dataset. 

A partir dos dados do segundo dataset, os autores aplicam conceitos de teoria musical para reduzir as melodias a frases melódicas caracterizadas por sequências de notas consecutivas. Com isso, é feita a contabilização da frequência com a qual determinadas frases ocorrem nas músicas, e isso foi organizado na tabela que é o último dataset.

## Perguntas de pesquisa/análises

Os autores sugerem ao fim do artigo que, em trabalhos futuros, pretendem refinar as informações contidas no banco analisando a harmonia das canções em conjunto com a melodia.

Há diversas análises que podem ser feitas inspiradas no que foi feito para a geração do terceiro dataset. No trabalho dos autores, não foram levados em consideração, por exemplo, aspectos rítmicos das frases melódicas, que são registradas apenas como sequências de notas. Além disso, foram consideradas iguais apenas as frases melódicas com as mesmas exatas sequências de notas, mas é mais útil e musicalmente faz mais sentido comparar as frases em termos de intervalos e graus dentro de um campo harmônico.

Também é valido utilizar o terceiro dataset para análise de quais ideias musicais acontecem com maior frequência em músicas de sucesso, de forma a tentar prever quais músicas farão sucesso no futuro.

## Trabalhos relacionados

O artigo menciona alguns datasets de música, como:
* Bertin-Mahieux, T., Ellis, D. P., Whitman, B., and Lamere, P. (2011). The million song dataset.
* Olteanu, A. (2020). Gtzan dataset - music genre classification.
* Ay, Y. E. (2018). Spotify dataset 1921-2020, 160k+ tracks.

No entanto, os autores ressaltam que esses datasets são compostos majoritariamente por canções internacionais, de forma que se faz necessária a criação de datasets sobre música brasileira, demanda essa que os autores buscam suprir com o trabalho.