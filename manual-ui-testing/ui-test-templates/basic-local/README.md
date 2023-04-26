# Basic tests, local instance

## Preparation
* [ ] Launch client and API, via scripts in aratiny-manual. TODO: add wiki links
* Go to localhost:8080

## Initial loading
* [ ] The initial screenshot loads correctly, including the "share your feedback banner"
* [ ] The Javascript console doesn't show errors
* [ ] Check the `Release Notes Icon`
* [ ] Check the other links on the top: tutorial, cite us. For sign-in, sign-up, verify the inital 
      forms appears. There is another test TODO about interacting with knetspace

## Examples

### Click on "FLC gene expression"
* [ ] `Keywords` field is populated with: `flowering FLC FT`
* [ ] Under keywords, it shows: `18 documents and 14 genes will be found with this query`
* [ ] The other fields are empty
* Click on `Search`
* [ ] 14 genes are shown in the gene table. Check it matches [this](flc-genes.png)
* [ ] TODO: evidence view (buggy at the moment)
* [ ] Click on the map view, check it matches [this](flc-chr.png) (we're aware of the 
      graphic glitch on the bottom
* [ ] Go back to the gene view, select the first 3 genes, `3 genes selected` should appear 
      click on `Create network view`. Check it matches [this](flc-net.png)
* Check net view functionality
* [ ] Clicking and dragging on a blank point. the graph moves
* [ ] Right-click on a node, the options wheel appears
* [ ] From the option wheels, it's possible to show the info box on the right, this seems fine
* [ ] The info box works for other nodes and edges
* [ ] Other option wheels options work
* [ ] The info box can be closed
* [ ] The info box can be opened/closed with the top icon. We're aware it's initially empty
* [ ] In the legend, double click on CellComp (or other node). New nodes should show up
* [ ] Click on the redraw icon, it should redraw and reposition newly added nodes
* Check other net view options
  [ ] At least one different layout
  [ ] `Labels:`
  [ ] `Label Size`
* [ ] At the end, check the Javascript console for errors
* [ ] At the bottomo of the search form, check that `Clear Search Fiekds` work and that you can use the    
      cleared form again


### Select the example Yield-related Ara
* [ ] Check it matches [this](qtl-search-form.png)
* [ ] In the Chromosome Region section, check that changing chromosome changes count
* [ ] Check add/remove chromosome regions
* Search with the initial region
* [ ] Check [the gene view](qtl-genes.png)
* [ ] Check the [evidence view](qtl-evidence.png), check it has p-values, downloadable genes, 
      gene list (click and verify links)
* [ ] Check the chromosome view, the chromosome 1 should be plenty of entries
* [ ] Check the chromosome view: resize, redraw, auto-labels, genes number, save, advanced options
* [ ] Select a few genes on the chromosome view, click on the net view icon on the top left, verify 
      a net view appears
* [ ] At the end, check the Javascript console
      
## Switching specie
* [ ] The specie selector on the top left switches between species, changing examples correctly
      (1 ex for Triticum, 2 for Zea)
* [ ] Do similar tests to the above, verifying the examples work for the other species too

## Misc UI tests
* [ ] In the gene view, clicking on a single gene shows its network view
* [ ] In the `Keyowprds`, when you start typing, the counter down the text box changes
* [ ] The concept selector on the end of `Keyowrds` works fine (including +/-)
* [ ] The concept selector is blanked when the `Keywords` box is emptied
* [ ] In evidence view -> `Genes`, click on a row, the copy and donwload buttons work fine.
      Paste some list in the search box
* [ ] In the evidence view, clicking on `Gene list` show the network view for those user genes

      
  




