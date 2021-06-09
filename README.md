# Grigoprint-saleor
installa saleor tramite docker-compose: [Documentazione Saleor](https://docs.saleor.io/docs/developer/installation/()

mettiquesta cartella in saleor/saleor/plugins

installazione app: file: saleor/saleor/schema.py ... INSTALLED_APPS = [ ..., # grigprint "saleor.plugins.grigoprint", ] ... PLUGINS = [ ..., # grigprint "saleor.plugins.grigoprint.plugins.Grigoprint", ] aggancio graphql: file: saleor/saleor/graphql/api.py from ..plugins.grigoprint.graphql.schema import GrigoprintMutations, GrigoprintQueries ... class Query( ..., #grigoprint GrigoprintQueries, ): ... class Mutation( ..., #grigoprint GrigoprintMutations, ): ...
