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
    
## Liste des logiciels libres développés par des personnes employées par des universités françaises 

* Voir [cette requête](https://query.wikidata.org/embed.html#SELECT%20DISTINCT%20%3Fitem%20%3FitemLabel%20%3Fdeveloper%20%3FdeveloperLabel%20WHERE%20%7B%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%2Cen%22.%20%7D%0A%20%20%3Fitem%20wdt%3AP31%2Fwdt%3AP279*%20wd%3AQ7397.%20%20%20%20%20%20%20%23%20Software...%0A%20%20%3Fitem%20wdt%3AP178%2Fwdt%3AP279*%20%3Fdeveloper.%20%20%20%20%23%20...developed%20by...%0A%20%20%7B%0A%20%20%20%20%3Fdeveloper%20wdt%3AP31%2Fwdt%3AP279*%20wd%3AQ31855.%20%23%20...a%20research%20institute%0A%20%20%20%20%3Fdeveloper%20wdt%3AP17%20wd%3AQ142.%20%20%20%20%20%20%20%20%20%20%20%20%20%23%20...in%20France.%0A%20%20%7D%20UNION%20%7B%0A%20%20%20%20%3Fdeveloper%20wdt%3AP749%20%3Fparent.%20%20%20%20%20%20%20%20%20%20%20%20%23%20...a%20child%20organisation%0A%20%20%20%20%3Fparent%20wdt%3AP31%2Fwdt%3AP279*%20wd%3AQ31855.%20%20%20%20%23%20...of%20a%20research%20institute%0A%20%20%20%20%3Fparent%20wdt%3AP17%20wd%3AQ142.%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%23%20...in%20France.%0A%20%20%7D%0A%20%20%0A%7D%0A) ou [celle-ci](https://query.wikidata.org/#SELECT%20%3Flogiciel%20%3FlogicielLabel%20%3Fdeveloppeur%20%3FdevelopeurLabel%20%3Femployeur%20%3FemployeurLabel%0AWHERE%20%7B%0A%20%20%3Flogiciel%20%28wdt%3AP31%2Fwdt%3AP279%2a%29%20wd%3AQ341.%0A%20%20%3Flogiciel%20wdt%3AP178%20%3Fdeveloppeur.%0A%20%20%3Fdeveloppeur%20wdt%3AP108%20%3Femployeur.%0A%20%20%3Femployeur%20wdt%3AP17%20wd%3AQ142.%0A%20%20%3Femployeur%20%28wdt%3AP31%2Fwdt%3AP279%2a%29%20wd%3AQ3551775%20.%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%2Cfr%22%20%7D%0A%7D).

    SELECT ?logiciel ?logicielLabel ?developpeur ?developeurLabel ?employeur ?employeurLabel
    WHERE {
        ?logiciel (wdt:P31/wdt:P279*) wd:Q341.
        ?logiciel wdt:P178 ?developpeur.
        ?developpeur wdt:P108 ?employeur.
        ?employeur wdt:P17 wd:Q142.
        ?employeur (wdt:P31/wdt:P279*) wd:Q3551775 .
         SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],fr" }
    }

## Droits et contributions	

Les documents contenus dans ce dépôt sont publiés sous [licence Ouverte 2.0](LICENSE.txt).

Pour toute contribution, merci d'ouvrir une =issue= ou de proposer une =Pull Request=.
