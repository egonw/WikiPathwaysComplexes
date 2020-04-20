# WikiPathways Complexes

Reference drawings of complexes in [WikiPathways](https://wikipathways.org/) and matching
expectations of biological interactions to be captured in the resulting RDF. The approach
is modelled after [work by Ryan Miller et al.](https://github.com/RyAMiller/WikiPathwaysInteractions)
and based on countless discussions in the BiGCaT research group (involving at least Ryan, Chris,
Denise, and Tina).

## Expections

Each GPML file gets converted into RDF (see Waagmeester et al.), and SPARQL queries can be used
to see of the GPML content gets represented in the RDF correctly. Example expectations look like:

```
dataNodeCount = 5
interactionCount = 3
binding = a,b
downstream = y,x
```

The first two expectations, `dataNodeCount` and `interactionCount` refer to the number of
`wp:DataNode` and `wp:Interaction` resources in the RDF. The number of `binding`s are
counted as binding interactions. The `downstream` expectation checks is there is
a unidirectional `wp:DirectionInteraction` path that links (in this case) `y` and `x`,
where the `y` data node is downstream of `x`.

Now, head over to [Complexes.md](Complexes.md) to see the reference examples.
