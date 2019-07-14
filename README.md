# meuParlamento.pt open data
This repository is a dump from our oficial database. It contains all proposals and its preprocessed metadata. 

## Requirements

The proposals.json file is a plain json file exported from our mongodb instance. In order to import it to a local mongodb database just use `mongoimport`.

```sh
mongoimport --db meuParlamento --collection proposals --file proposals.json
```

## Schema example

| #Attribute     | #Type  | #Description                     | #Example                                                                                                                                          |
|----------------|--------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| title          | String | Proposal title.                  |  Recomenda ao Governo que os serviços clínicos e valências actualmente disponíveis no Centro Hospitalar do Baixo Vouga continuem em funcionamento |
| BID            | Int32  | Unique proposal ID               | 38525                                                                                                                                             |
| comissoes      | Array  | Comissions                       | Comissão de Saúde                                                                                                                                 |
| votos          | Object | Votos dos partidos               | contra:Array, afavor:Array, abstencao:Array                                                                                                       |
| anoVotacao     | Int    | Ano da votação                   | 2014                                                                                                                                              |
| proposedBy     | String | Partido autor da proposta        | CDS-PP                                                                                                                                            |
| resultadoFinal | String | Resultado da votação em plenário | Aprovado                                                                                                                                          |
| dataVotacao    | Int64  | Timestamp da data da votação     | 1401408000000                                                                                                                                     |
## Meta

Team [@meuparlamento](https://twitter.com/meuparlamento) – dev@meuparlamento.pt
[https://github.com/meuparlamento](https://github.com/meuparlamento/)
