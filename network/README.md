
This file describes what the raw network data look like. 

There are 5 different network layers, they are all documented on the [CBS website](https://www.cbs.nl/nl-nl/onze-diensten/maatwerk-en-microdata/microdata-zelf-onderzoek-doen/catalogus-microdata/bevolking).
- classmates: [documentation for `klasgenotennetwerktab`](https://www.cbs.nl/nl-nl/onze-diensten/maatwerk-en-microdata/microdata-zelf-onderzoek-doen/microdatabestanden/klasgenotennetwerktab-klasgenotenrelaties)
- neighbors: [documentation for `burennetwerktab`](https://www.cbs.nl/nl-nl/onze-diensten/maatwerk-en-microdata/microdata-zelf-onderzoek-doen/microdatabestanden/burennetwerktab-buren-en-buurtgenotenrelaties)
- work colleagues: [documentation for `collegnetwerktab`](https://www.cbs.nl/nl-nl/onze-diensten/maatwerk-en-microdata/microdata-zelf-onderzoek-doen/microdatabestanden/colleganetwerktab-collegarelaties)
- family: [documentation for `familienetwerktab`](https://www.cbs.nl/nl-nl/onze-diensten/maatwerk-en-microdata/microdata-zelf-onderzoek-doen/microdatabestanden/familienetwerktab-familierelaties)
- household: [documentation for `huisgenotennetwerktab`](https://www.cbs.nl/nl-nl/onze-diensten/maatwerk-en-microdata/microdata-zelf-onderzoek-doen/microdatabestanden/huisgenotennetwerktab-huisgenotenrelaties)


In the documentation files, section 3. "Bestandsopbouw en toelichting" contains the variable names and a codebook.

There is one csv file for each year, starting in 2009.

Each file has the same structure. 
- the variables `RINPERSOONS` and `RINPERSOON` define the unique key of one person. 
- the variables `RINPERSOONRELATIE` and `RINPERSOONSRELATIE` define the unique key of the other person. 
- `RELATIE` is a numeric column indicating the type of the relation. The codebook has the unique values for each network.

Columns are separated by a semicolon. In 2009, files contain between 250 and 600 Mio rows. Graphs are undirected but edges may appear twice in the data because connection types can be heterogeneous (such as uncle/nephew relation) or not (such as work mates). 
However, for the example I checked, it seems also possible that there is only one edge for a connection.