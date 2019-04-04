Le premier principal de ce dépôt est de faire un tour d'horizon des
structures de droit privé créant de la valeur autour de logiciels
libres produits par des laboratoires de recherche publique.  « Créer
de valeur » peut s'entendre comme « créer de l'emploi ».

Le but accessoire est de créer une liste (non exhaustive) des
logiciels produits par ces laboratoires de recherche publique.

## Sociétés de droits privés créant de la valeur autour de ces logiciels libres 

Voir [la liste](ecosysteme-valorisation-ll-esr.md).

## Logiciels libres produits ou améliorés par des laboratoires ESR

Voir [la liste](liste-ll-produits-esr.md).

## Noms de domaine des laboratoires de recherche français

À faire.

## Noms de domaine des universités françaises

Liste des universités française : [CSV](universites-francaises.csv) ou [JSON](universites-francaises.json).

Construite à partir de cette requête SPARQL sur [Wikidata](https://query.wikidata.org/):

    SELECT ?item ?itemLabel ?url
    WHERE
    {
    ?item wdt:P31 wd:Q3551775 .
    ?item wdt:P856 ?url
    SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],fr" }
    }

## Droits et contributions	

Les documents contenus dans ce dépôt sont publiés sous [licence Ouverte 2.0](LICENSE.txt).

Pour toute contribution, merci d'ouvrir une =issue= ou de proposer une =Pull Request=.
