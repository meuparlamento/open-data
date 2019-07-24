# meuParlamento.pt open data
This repository is a dump from our oficial database. It contains all proposals and its preprocessed metadata. 

## Requirements

The proposals.json file is a plain json file exported from our mongodb instance. You can import it to your local mongodb database using `mongoimport`.

```sh
mongoimport --db meuParlamento --collection proposals --file proposals.json
```

## Schema

| #Attribute     | #Type  | #Description                     | #Example                                                                                                                                          |
|----------------|--------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| title          | String | Proposal title.                  | Recomenda ao Governo que os serviços clínicos e valências actualmente disponíveis no Centro Hospitalar do Baixo Vouga ... |
| BID            | Int32  | Unique proposal ID               | 38525                                                                                                                                             |
| comissoes      | Array  | Comissions                       | Comissão de Saúde                                                                                                                                 |
| votos          | Object | Votos dos partidos               | contra:Array, afavor:Array, abstencao:Array                                                                                                       |
| anoVotacao     | Int    | Ano da votação                   | 2014                                                                                                                                              |
| proposedBy     | String | Partido autor da proposta        | CDS-PP                                                                                                                                            |
| resultadoFinal | String | Resultado da votação em plenário | Aprovado                                                                                                                                          |
| dataVotacao    | Int64  | Timestamp da data da votação     | 1401408000000                                                                                                                                     |                                  |
## Meta

Team [@meuparlamento](https://twitter.com/meuparlamento) – dev@meuparlamento.pt

## License
This work is licensed under the Creative Commons Attribution-ShareAlike 2.5 Generic License. To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/2.5/ or send a letter to Creative Commons, PO Box 1866, Mountain View, CA 94042, USA.
