# Logiciels libres produits ou améliorés par des laboratoires ESR

| URL du logiciel libre                 | URL du labo contributeur principal |
|---------------------------------------|------------------------------------|
| <https://scikit-learn.org>            |                                    |
| <https://ocaml.org>                   |                                    |
| <https://coq.inria.fr/>               | <https://www.inria.fr/>            |
| <https://www.cgal.org/>               |                                    |
| <http://eigen.tuxfamily.org/>         |                                    |
| <https://www.scilab.org>              | <https://www.inria.fr/> (début)    |
| <https://github.com/valette/Wavemesh> |                                    |
| <https://projet.liris.cnrs.fr/dgtal/> | <https://liris.cnrs.fr/>           |
| <https://github.com/SimonRit/RTK>     |                                    |


# Sociétés de droits privés créant de la valeur autour de ces logiciels libres 

| URL de la société                                | Logiciels libres                           |
|--------------------------------------------------|--------------------------------------------|
| <https://www.fondation-inria.fr>                 | <https://scikit-learn.fondation-inria.fr/> |
| <https://www.fondation-inria.fr>                 | <https://www.softwareheritage.org/>        |
| <http://openrtk.org/RTK/project/consortium.html> | <http://openrtk.org>                       |
| <http://science-miner.com/>                      | <https://github.com/kermitt2/grobid>       |

# Noms de domaine des universités françaises

Liste des universités française : [CSV](universites-francaises.csv) ou [JSON](universites-francaises.json).

Construite à partir de cette requête SPARQL sur [Wikidata](https://query.wikidata.org/):

    SELECT ?item ?itemLabel ?url
    WHERE
    {
    ?item wdt:P31 wd:Q3551775 .
    ?item wdt:P856 ?url
    SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],fr" }
    }

# Noms de domaine des laboratoires de recherche français

À faire.

# Droits et contributions	

Les documents contenus dans ce dépôt sont publiés sous [licence Ouverte 2.0](LICENSE.txt).

Pour toute contribution, merci d'ouvrir une =issue= ou de proposer une
=Pull Request=.

