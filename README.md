
Overview
--------

netrankr is an R package that is tailored for centrality analyses of networks without (necessarily) relying on indices. It can, however, also be used in other context to analyze partial rankings.

Install
-------

Main Usage
----------

The main function is `rank_analysis` which performs a complete analysis of a given partial ranking. This includes:

-   Number of possible linear extensions (rankings).
-   Rank probabilities: Prob(rk(u)=k) for all nodes and ranks.
-   Relative rank probabilities Prob(rk(u)&lt;rk(v)) for all nodes.
-   Expected ranks of nodes.

`neighborhood_inclusion` and `positional_dominance` can be used to construct partial orders on a network. While `neighborhood_inclusion` is very specific (undirected, unweighted networks), `positional_dominance` can be used with any kind of input network. If cost variables (e.g. distances) are used, set `benefit=F`. If actor identities don't matter set `map=TRUE`. Consult the vignettes for more detailed explanations.

Caveats
-------

Finding/Enumerating all linear extension of a partial order is \#P-complete, so be careful with bigger inputs, since your Computer might explode(literally!!)

There exist some approximate methods found with `approx_` that work brilliantly even on huge networks.
