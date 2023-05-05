# [InfiniteScrollingLocal] Infinite Scrolling tests, local instance

[Test instances]()

## Preparation
* [ ] Launch client and API, via scripts in aratiny-manual. TODO: add wiki links
* [ ] Go to localhost:8080. The UI works
* [ ] Type `a***` as search string. Counts are: *1321 documents and 220 genes*.

## Obtaining long list for the gene table
* [ ] The gene table shows with the first page (30/220 genes).
* [ ] As you scroll, more rows are added, up to 220. Each page addition takes about 1 sec
* [ ] BioProc filter selects 7 genes
* [ ] Adding Publication to BioProc selects only one gene (`AT3G16830`)
* [ ] Deselecting all filters shows 220 genes again. Scrolling works as before
* [ ] Select Publication only, scrolling works on 43 rows
* [ ] Revert button at the end of the legend removes all filters
* [ ] CellComp shows 7 rows and the infinite scrolling doesn't scroll anything


## Testing the evidence table
* [ ] While on the same search results, switch to the evidence table, it shows 413 evidences
* [ ] The scroll works here too
* [ ] Filter on Genes, 331 genes are filtered, as the icon shows
* [ ] Select Trait and ProteinDomain, 36 rows are filtered (as the numbers in the icons)
* [ ] Remove all filters, 413 evidences are shown again
* [ ] The reset button at the end of the legend has no effect when no filter is selected
* [ ] The reset button reset the filters when some are selected
* [ ] PlantOntologyTerm shows 9 rows and the infinite scrolling doesn't scroll anything (since
      the page size is 30)

## Testing gene table sorting
* [ ] Redo the search in preparation
* [ ] Genes are sorted by KnetScore/descending, as shown in the respective column, 
      with an upward arrow
* [ ] Clicking on the arrow, it becomes downwards and the genes are sorted in ascending order
* [ ] The other columns can be sorted too
* [ ] When filtering, the selected sorting criteria remain the same and work correctly
* [ ] When removing the filters, sorting criteria are reset to the initial ones said above


## Testing the evidence table sorting
* [ ] Redo the search in preparation
* [ ] Evidences should be sorted with the priorities: pvalues/asc, gene list/desc, genes/desc, node 
      label. Corresponding columns have arrows accordingly. In this case, they end up being sorted by
      genes and node label, since the other columns don't have values
* [ ] Arrows work as above
* [ ] The other columns can be sorted too
* [ ] When filtering, the selected sorting criteria remain the same and work correctly
* [ ] When removing the filters, sorting criteria are reset to the initial ones said above

## Testing the evidence table sorting, with p-values
* [ ] Select the example *Yield-related Ara. QTLs*. Replace the example keywords with `a***`, leave
      the gene list and chromosome region
* [ ] The evidence view has 52 rows, now there are actual values for p-value and Gene List and p-value
      dominate the sorting
* [ ] Sorting by Genes or Gene List works correctly
* [ ] When filtering, the selected sorting criteria remain the same and work correctly

## Headline for the test instances

Based on [this template][TPLREF]. 

**Please, always report a link to the template a UI test is about and also its ID in the title.** This is very useful to [find test instances][TPLINST] from the template. The best way to do that is copying this headline to every new instance.

Tests from the template that aren't mentioned hereby are intended as passed.

[TPLREF]: 
[TPLINST]: 
