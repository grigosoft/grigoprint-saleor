# Grigoprint-saleor
installa saleor tramite docker-compose: [Documentazione Saleor](https://docs.saleor.io/docs/developer/installation/()

mettiquesta cartella in saleor/saleor/plugins

installazione app: file: saleor/saleor/schema.py ... INSTALLED_APPS = [ ..., # grigprint "saleor.plugins.grigoprint", ] ... PLUGINS = [ ..., # grigprint "saleor.plugins.grigoprint.plugins.Grigoprint", ] aggancio graphql: file: saleor/saleor/graphql/api.py from ..plugins.grigoprint.graphql.schema import GrigoprintMutations, GrigoprintQueries ... class Query( ..., #grigoprint GrigoprintQueries, ): ... class Mutation( ..., #grigoprint GrigoprintMutations, ): ...


# File importanti StoreFront
## SCSS Style
In questi file si trovano le variabili e lo stile generico dello store front:

* saleor/saleor-storefront/src/globalStyles/
  * varibles.scss
  > Variabili generiche: Colori, tipografia, bottoni (solo dimensione, font e spazi), input, brekpoints
  * _utils.scss
  * _components.scss
  * index.scss
  > Utilizzo base delle variabili di stile, come il carattere, alcuni colore base, colori base delle tabelle e dei form
## HTML Importanti
Head: saleor/saleor-storefront/src/index.html
> File base html dove troviamo l'<head> base per tutto il sito
