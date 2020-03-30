# ferramentas_raspagem
## Descrição

Estre script foi criado para raspar notcias do site G1, usando queries diversas. Seu teste de carga pegou 30 mil notícias sobre os mais variados temas. 

### Instalação

Para usar o script basta fazer download e abri-lo dentro do RStudio/R.
Pacotes necessários: rvest, lubridate,plyr,dplyr e xlsx


### Realizando a busca
Cada paginação retorna 15 resultados. EX: n_pagination = 10 retorna 150 notícias de 1 termo
``` r
test1 <- search(term = c("bolsonaro"), n_pagination =  10)
test2 <- search(term = c("virus","bolsonaro","rodrigo maia"), n_pagination =  3)
```


### Resultado
``` r
glimpse(test2)
Rows: 133
Columns: 6
$ Title       <chr> "Dezenas saem em carreata pelas ruas de Mogi pedindo reabertura de comércios fechados por causa do c…
$ Description <chr> "Moradores de Mogi das Cruzes realizam carreata pela reabertura dos comércios\nNo fim da manhã desta…
$ Newspaper   <chr> "G1", "G1", "G1", "G1", "G1", "G1", "G1", "G1", "G1", "G1", "G1", "Jornal Hoje", "G1", "Meio Dia Par…
$ Timestamp   <dttm> 2020-03-30 16:39:16, 2020-03-30 16:35:16, 2020-03-30 16:31:16, 2020-03-30 15:57:16, 2020-03-30 15:5…
$ URL         <chr> "g1.globo.com/busca/click?q=virus&p=24&r=1585608958287&u=https%3A%2F%2Fg1.globo.com%2Fsp%2Fmogi-das-…
$ Term        <chr> "virus", "bolsonaro", "bolsonaro", "bolsonaro", "virus", "virus", "virus", "virus", "bolsonaro", "vi…
```
