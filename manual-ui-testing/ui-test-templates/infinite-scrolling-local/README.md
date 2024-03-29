# [InfiniteScrollingLocal] Infinite Scrolling tests, local instance

[Test instances][TPLINST]

## Preparation
* [ ] Launch client and API, via scripts in aratiny-manual. TODO: add wiki links
* [ ] Go to localhost:8080. The UI works
* [ ] Type `a***` as search string. Counts are: *1321 documents and 220 genes*. Hit on 'Search'.

## Testing long list for the gene table and type filters
* [ ] The gene table shows with the first page (30/220 genes).
* [ ] As you scroll, more rows are added, up to 220. Each page addition takes about 0.5 sec
* [ ] BioProc filter selects 7 genes
* [ ] Adding Publication to BioProc selects only one gene (`AT3G16830`)
* [ ] Deselecting all filters shows 220 genes again. Scrolling works as before
* [ ] Select Publication only, scrolling works on 43 rows
* [ ] Revert button at the end of the legend removes all filters
* [ ] CellComp shows 7 rows and the infinite scrolling doesn't scroll anything

## Testing the score filter
* [ ] Do the 'Preparation' above again
* [ ] Select the score filter (funnel next to the 'KnetScore' column), a slider with min/max score opens
* [ ] Select a max score of about 10 and apply, only rows with score <= 10 are shown
* [ ] Select the filter again, set the 5-10 interval and verify it works
* [ ] Click on filter reset button, verify all the original rows are restored

## Testing the score filter
* [ ] Repeat the steps above, using the graph distance filter (next to the 'Evidence' column). Verify that with distance = 1, 207 rows are selected
* [ ] With distance = 2, 217 rows are selected
* [ ] With distance = 4, all the rows are selected again
* [ ] As above, when distance filter is active, the reset filter button correctly cancels the filter

## Testing the evidence table
* [ ] While on the same search results, switch to the evidence table, it shows 413 evidences
* [ ] The scroll works here too
* [ ] Scroll to the bottom, the table should update to add new rows
* [ ] Scroll to absolute bottom, make sure it reads "Showing 413 of 413" and the table doesn't duplicate itself
* [ ] Filter on Genes, 331 genes are filtered, as the icon shows
* [ ] Select Trait and ProteinDomain, 36 rows are filtered (as the numbers in the icons)
* [ ] Remove all filters, 413 evidences are shown again
* [ ] The reset button at the end of the legend has no effect when no filter is selected (apart from showing again 30 rows only)
* [ ] The reset button reset the filters when some are selected
* [ ] PlantOntologyTerm shows 9 rows and the infinite scrolling doesn't scroll anything (since the page size is 30)

## Testing gene table sorting
* [ ] Redo the search in preparation
* [ ] The gene table is sorted by KnetScore.
* [ ] When filtering, the selected sorting criteria remain the same and work correctly

Note: In 2023-05-15, we have removed the possibility to select the sorted colum, due to various issues.

## Testing the evidence table sorting
* [ ] Redo the search in preparation
* [ ] Evidences should be sorted with the priorities: pvalues/asc, gene list/desc, genes/desc, node label. In this case, they end up being sorted by genes and node label, since the other columns don't have values.
* [ ] When filtering, the selected sorting criteria remain the same and work correctly

As said above, user can't decide the sorting column anymore.

## Testing the evidence table sorting, with p-values
* [ ] Select the example *Yield-related Ara. QTLs*. Replace the example keywords with `a***`, leave the gene list and chromosome region
* [ ] The evidence view has 52 rows, now there are actual values for p-value and Gene List and p-value dominate the sorting


## Headline for the test instances

**Please, report this Markdown code at the beginning of every GH ticket that represents a report on running the test described in the hereby template**:

```Markdown
*This is a manual UI test based on [this template][TPLREF]. Other instances of this test are [here][TPLINST]. Tests from the template that aren't mentioned hereby are intended as passed.*

[TPLREF]: https://github.com/Rothamsted/knetminer-testing/blob/v2.1/manual-ui-testing/ui-test-templates/infinite-scrolling-local/README.md
[TPLINST]: https://github.com/Rothamsted/knetminer/issues?q=InfiniteScrollingLocal
```

**Please, when opening an issue about this test, always use this format**:

```
[InfiniteScrollingLocal UI Test] <description>
```

This is useful to [find test instances][TPLINST] from the template.

[TPLREF]: https://github.com/Rothamsted/knetminer-testing/blob/v2.1/manual-ui-testing/ui-test-templates/infinite-scrolling-local/README.md
[TPLINST]: https://github.com/Rothamsted/knetminer/issues?q=InfiniteScrollingLocal

