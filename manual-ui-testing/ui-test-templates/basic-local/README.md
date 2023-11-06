# [BasicLocal] Basic tests, local instance

[Test instances][TPLINST]

## Preparation
* [ ] Launch client and API, via scripts in aratiny-manual. TODO: add wiki links
* Go to localhost:8080

## Initial loading
* [ ] The initial screenshot loads correctly, including the "share your feedback banner"
* [ ] The Javascript console doesn't show errors
* [ ] Check the `Release Notes Icon`
* [ ] Check the other links on the top: tutorial, cite us. For sign-in, sign-up, verify the inital forms appears. There is another test TODO about interacting with knetspace.

## Testing the Examples

### Click on "FLC gene expression"
* [ ] `Keywords` field is populated with: `flowering FLC FT`
* [ ] Under keywords, it shows: `18 documents and 14 genes will be found with this query`
* [ ] The other fields are empty
* Click on `Search`
* [ ] 14 genes are shown in the gene table. Check it matches [this](flc-genes.png)
* [ ] Switch to the evidence view. It matches [this](flc-evidence.png)
* [ ] Click on the map view, check it matches [this](flc-chr.png) (we're aware of the 
      graphic glitch on the bottom
* [ ] Go back to the gene view, select the first 3 genes, `3 genes selected` should appear 
      click on `Create network view`. Check it matches [this](flc-net.png)
* Check net view functionality
* [ ] Clicking and dragging on a blank point. the graph moves
* [ ] Right-click on a node, the options wheel appears
* [ ] From the option wheels, it's possible to show the info box on the right, this seems fine
* [ ] The info box works for other nodes and edges
* [ ] Other option wheels options work
* [ ] The info box can be closed (we're aware that sometimes you need the enlarged view for this)
* [ ] The info box can be opened/closed with the top icon. We're aware it's initially empty and it's only emptied on second click, not closed.
* [ ] In the legend, click on CellComp (or other node). New nodes should show up. Double click on the same icon, the corresponding nodes should disappear.
* [ ] Click on the redraw icon, it should redraw and reposition newly added nodes
* Check other net view options
  * [ ] At least one different layout
  * [ ] `Labels:`
  * [ ] `Label Size`
* [ ] At the end, check the Javascript console for errors
* [ ] At the bottom of the search form, check that `Clear Search Fields` work and that you can use the cleared form again


### Select the example Yield-related Ara
* [ ] Check it matches [this](qtl-search-form.png)
* [ ] In the Chromosome Region section, check that changing chromosome changes count
* [ ] Check add/remove chromosome regions
* Search with the initial region
* [ ] Check [the gene view](qtl-genes.png)
* [ ] Check the [evidence view](qtl-evidence.png), check it has p-values, downloadable genes, gene list (click and verify links)
* [ ] Check the chromosome view, the chromosome 1 should be plenty of entries
* [ ] Check the chromosome view: resize, redraw, auto-labels, genes number, save, advanced options
* [ ] Select a few genes on the chromosome view, click on the net view icon on the top left, verify a net view appears
* [ ] At the end, check the Javascript console
      
## Switching specie
* [ ] The specie selector on the top left switches between species, changing examples correctly (1 ex for Triticum, 2 for Zea)
* [ ] Do similar tests to the above, verifying the examples work for the other species too

## Concept Suggestion
* [ ] Reset the search form, the concept suggestion button (at the end of the kewords box) is white and disabled
* [ ] Type "seed". The suggestion button becomes active
* [ ] Click on the suggestion button. [this appears](suggester.png)
* [ ] You can switch between the types on the right of the suggested concept box
* [ ] When clicking on '+' on a concept, `ConceptID:NNNN` is added to the search box and the concept selector changes with the filtered concept
* [ ] When clicking on '-', `NOT ConceptID:NNNN` is added to the search box
* [ ] When clicking on the 'replace' circle, after +/-, the current token in the text search box (shown on the top of the concept selector box) is replaced by the corresponding concept ID 
* [ ] Click on the suggester again, it works correctly and 'Search' performs the search with the chosen concept IDs.

## Misc UI tests
* [ ] In the gene view, clicking on a single gene shows its network view
* [ ] In the `Keyowords`, when you start typing, the counter down the text box changes
* [ ] The concept selector on the end of `Keyowrds` works fine (including +/-)
* [ ] The concept selector is blanked when the `Keywords` box is emptied
* [ ] In evidence view -> `Genes`, click on a row, the copy and donwload buttons work fine.
      Paste some list in the search box
* [ ] In the evidence view, clicking on `Gene list` show the network view for those user genes

## URL-related tests
* [ ] Go to go to http://localhost:8080/?taxId=4565
      The UI opens with *Triticum Aestivum* selected
* [ ] Go to this [/genome URL](http://localhost:9090/ws/aratiny/genome?keyword=flowering%20FLC%20FT&list=TRP*,BRA*). A correct reply is given.
* [ ] Go to this [/genome URL](http://localhost:9090/ws/aratiny/genome?keyword=flowering%20FLC%20FT&list=TRP*,BRA*), which omits the data source ID from the URL. A correct reply is given.

## Gene page test
* [ ] This [gene page URL](http://localhost:8080/html/genepage.jsp?keywords=flowering%20FLC%20FT&list=TRP*,AT1G*)  works correctly.



## Headline for the test instances

**Please, report this Markdown code at the beginning of every GH ticket that represents a report on running the test described in the hereby template**:

```Markdown
*This is a manual UI test based on [this template][TPLREF]. Other instances of this test are [here][TPLINST]. Tests from the template that aren't mentioned hereby are intended as passed.*

[TPLREF]: https://github.com/Rothamsted/knetminer-testing/blob/v3.0/manual-ui-testing/ui-test-templates/basic-local/README.md
[TPLINST]: https://github.com/Rothamsted/knetminer/issues?q=BasicLocal
```

**Please, when opening an issue about this test, always use this format**:

```
[BasicLocal UI Test] <description>
```

This is useful to [find test instances][TPLINST] from the template.

[TPLREF]: https://github.com/Rothamsted/knetminer-testing/blob/v3.0/manual-ui-testing/ui-test-templates/basic-local/README.md
[TPLINST]: https://github.com/Rothamsted/knetminer/issues?q=BasicLocal
