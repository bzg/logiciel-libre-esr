# Pourquoi faire ?

Le **but principal** de ce dépôt est de faire un tour d'horizon des
structures de droit privé créant de la valeur autour de logiciels
libres produits par des laboratoires de recherche publique.  « Créer
de valeur » peut s'entendre comme « créer de l'emploi ».

Le **but accessoire** est de créer une liste (non exhaustive) des
logiciels produits par ces laboratoires de recherche publique.

## Ce n'est pas

- Un doublon du projet [PLUME](https://projet-plume.org), surtout dédié à la création de fiches sur des logiciels libres utilisés dans l'ESR.
- Un doublon du projet [Software Heritage](https://www.softwareheritage.org) qui a pour ambition de construire une archive universelle des logiciels.

## Et après ?

Deux suites possibles autour de cet effort de collection de ressouces:

- **réunir** les personnes intéressées pour enrichir [Wikidata](https://www.wikidata.org) et permettre de collecter toutes les informations à partir d'une requête ;
- **détailler** des cas de valorisation de logiciels libres issus de
  la recherche publique par des structures de droit privé.

## Comment contribuer ?

- Vous pouvez [ajouter](https://github.com/bzg/logiciel-libre-esr/issues/new?assignees=&labels=&template=ajout-logiciel-libre-esr.md&title=) des logiciels libres issues de la recherche publique en proposant d'enrichir [cette liste](liste-ll-produits-esr.md).

- Vous pouvez [ajouter](https://github.com/bzg/logiciel-libre-esr/issues/new?assignees=&labels=&template=ajout-structure-privee.md&title=) des sociétés de droit privé valorisant la recherche publique en proposant d'enrichir [cette liste](liste-ll-produits-esr.md).

- Vous pouvez [ajouter](https://github.com/bzg/logiciel-libre-esr/issues/new?assignees=&labels=&template=ajout-etude-de-cas.md&title=) des [études de cas](etudes-de-cas.md) légères montrant comment s'est faite et/ou se fait la valorisation autour de ces logiciels libres.

# Ressources

## Sociétés de droits privés créant de la valeur autour de ces logiciels libres 

Voir [la liste](ecosysteme-valorisation-ll-esr.md).

## Logiciels libres produits ou améliorés par des laboratoires ESR

Voir [la liste](liste-ll-produits-esr.md).

## Noms de domaine des laboratoires de recherche français

- [ ] Proposer une requête Wikidata

## Noms de domaine des universités françaises

- [Requête Wikidata](https://query.wikidata.org/#SELECT%20%3Fitem%20%3FitemLabel%20%3Furl%0AWHERE%0A%20%20%20%20%7B%0A%20%20%20%20%3Fitem%20wdt%3AP31%20wd%3AQ3551775%20.%0A%20%20%20%20%3Fitem%20wdt%3AP856%20%3Furl%0A%20%20%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%2Cfr%22%20%7D%0A%20%20%20%20%7D%0A)

Liste des universités française : [CSV](universites-francaises.csv) ou [JSON](universites-francaises.json).

## Liste des logiciels libres développés par des personnes employées par des universités françaises

* [Première requête Wikidata](https://query.wikidata.org/embed.html#SELECT%20DISTINCT%20%3Fitem%20%3FitemLabel%20%3Fdeveloper%20%3FdeveloperLabel%20WHERE%20%7B%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%2Cen%22.%20%7D%0A%20%20%3Fitem%20wdt%3AP31%2Fwdt%3AP279*%20wd%3AQ7397.%20%20%20%20%20%20%20%23%20Software...%0A%20%20%3Fitem%20wdt%3AP178%2Fwdt%3AP279*%20%3Fdeveloper.%20%20%20%20%23%20...developed%20by...%0A%20%20%7B%0A%20%20%20%20%3Fdeveloper%20wdt%3AP31%2Fwdt%3AP279*%20wd%3AQ31855.%20%23%20...a%20research%20institute%0A%20%20%20%20%3Fdeveloper%20wdt%3AP17%20wd%3AQ142.%20%20%20%20%20%20%20%20%20%20%20%20%20%23%20...in%20France.%0A%20%20%7D%20UNION%20%7B%0A%20%20%20%20%3Fdeveloper%20wdt%3AP749%20%3Fparent.%20%20%20%20%20%20%20%20%20%20%20%20%23%20...a%20child%20organisation%0A%20%20%20%20%3Fparent%20wdt%3AP31%2Fwdt%3AP279*%20wd%3AQ31855.%20%20%20%20%23%20...of%20a%20research%20institute%0A%20%20%20%20%3Fparent%20wdt%3AP17%20wd%3AQ142.%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%23%20...in%20France.%0A%20%20%7D%0A%20%20%0A%7D%0A)
- [Deuxième requête Wikidata](https://query.wikidata.org/#SELECT%20%3Flogiciel%20%3FlogicielLabel%20%3Fdeveloppeur%20%3FdevelopeurLabel%20%3Femployeur%20%3FemployeurLabel%0AWHERE%20%7B%0A%20%20%3Flogiciel%20%28wdt%3AP31%2Fwdt%3AP279%2a%29%20wd%3AQ341.%0A%20%20%3Flogiciel%20wdt%3AP178%20%3Fdeveloppeur.%0A%20%20%3Fdeveloppeur%20wdt%3AP108%20%3Femployeur.%0A%20%20%3Femployeur%20wdt%3AP17%20wd%3AQ142.%0A%20%20%3Femployeur%20%28wdt%3AP31%2Fwdt%3AP279%2a%29%20wd%3AQ3551775%20.%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%2Cfr%22%20%7D%0A%7D)

## Droits et contributions

Les documents contenus dans ce dépôt sont publiés sous [licence Ouverte 2.0](LICENSE.txt).

Les contributions sont les bienvenues : merci d'ouvrir une =issue= ou de proposer une `Pull Request`.
